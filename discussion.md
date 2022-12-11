# Discussion
I analyzed the Disney datasets in this final project and tried to figure out:

1. Which type of movie had the highest gross box office?
2. Which director had the highest gross box office from 1973 to 2016?
3. Whether the same director has the highest inflation-adjusted gross?


When looking into the type of the movies, i felt interesting to see that even though Disney produced 162 Comedy movies, the Adventure type took the highest total gross box office with 119 films. From the top_5_movies_gross dataset, we can tell that the top five movies with the highest total gross are all Adventure type. I also explored how many films were produced in each year and 1995 ranks the top year with 32 films.

I used the following python codes to rank the top 5 movies.

```python
top_5_movies_gross = gross_directors.sort_values(by='total_gross', ascending=False).reset_index().loc[0:4].drop(columns=['index'])
```

```python
top_5_movies_inflat = gross_directors.sort_values(by='inflation_adjusted_gross', ascending=False).reset_index().drop(columns=['index']).loc[0:4]
```

I grouped the movie by genre and calculated the sum of the total gross of each group in order to find out the top 5 gross movies by genre. Below is the sum equation. 


```{math}
:label: sum_label2
x_{1} + x_{2} + x_{3} +\dots + x_{n}=\sum_{n=1}^{10}n
```

Equation {eq}`sum_label2` is to calculate the sum of all values.

I also calcultated how many movies fewer the Adventure produced than the Comedy.


$162$$-119$ = $43$

```{math}
:label: subtract_label3
a-b = c
```
Equation {eq}`subtract_label3` is to calculate the difference between two values.


As I mentioned above, considering the inflation rates, the highest-ranking grossing movies might be different if they were adjusted for inflation. My analysis seems to approve of the differences. The top five films with the highest gross box office are completed separately from the top five movies with the inflation-adjusted gross box office. The Lion King, directed by Roger Allers, took first place in the total gross group, and Snow White and the Seven Dwarfs, directed by David Hand, was the top one in the inflation-adjusted group. 

```{margin} Did you know?
Which movies ranked the top among the two groups?
```

```{note}
Here are the movie posters!
```

:::{figure-md} markdown-fig
<img src="https://upload.wikimedia.org/wikipedia/en/3/3d/The_Lion_King_poster.jpg" width="300px"></image>

The Lion King Poster
:::


:::{figure-md} markdown-fig2
<img src="https://upload.wikimedia.org/wikipedia/en/4/49/Snow_White_1937_poster.png" width="300px"></image>

Snow White and the Seven Dwarfs Poster
:::

`````{admonition} The images are from...
:class: tip
Wikimedia
`````


