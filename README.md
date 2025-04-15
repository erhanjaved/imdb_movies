# IMDb Movie Ratings Dashboard (Power BI)

<p align="center">
  <img src="images/demo.gif" alt="Dashboard Demo" width="900"/>
</p>

An interactive Power BI dashboard project that explores what factors influence IMDb ratings for top movies. Created as part of COMM 335 at UBC Sauder School of Business.

## Project Overview

Our dashboard analyzes the key attributes contributing to a movie’s IMDb rating, including:

- Genre
- Runtime
- Number of Votes
- Gross Revenue
- Certificate Type
- Director & Lead Stars

The dashboard supports dynamic filtering and visual storytelling, helping users uncover meaningful trends and correlations through an intuitive interface.

## Research Question

**What factors affect a movie’s IMDb rating?**

## Methodology

We used the [IMDB Movies Dataset](https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows) from Kaggle. This dataset includes runtime, genres, cast, rating scores, and financial performance metrics.

### Preprocessing & Data Transformation

- Added missing release year for *Apollo 13* (1995)
- Converted `Runtime` from text (e.g., "142 min") to numeric
- Cleaned numeric fields (IMDb rating, metascore, gross)
- Replaced missing `Gross` values with `-1`
- Removed non-essential fields: `Overview`, `Star 3`, `Star 4`
- Reformatted `Poster Link` as an Image URL

#### Genre Handling

- Created a separate genre table to enable slicer-based filtering
- Added DAX measure `GenreFilterFlag` to identify movies matching selected genres

## Visualization Features

- Integrated CloudScope Image visual to render movie posters  
- Developed calculated DAX measures:
  - `Title` – Highest-rated movie title by genre
  - `Top5DirectorsByRating` – Average rating of top 5 directors
  - `TopGross` – Highest-grossing movie per filter
  - `TopMoviePoster` – Poster of highest-rated movie by filter
  - `TopStar1`, `TopStar2` – Lead actors of top-rated film
- Genre slicer for real-time user exploration

> Note: Some poster links are broken or low-resolution due to limitations in the dataset source.

## Team Members

- Erhan Asad Javed  
- Stephanie Ho  
- Zuhair Hussain  
- Dhananjai Lekhi  
- Kesar Mehta  
- Jane Piamkulvanich

## Acknowledgments

We would like to extend our sincere thanks to the professors and TAs of **COMM 335 – Information Systems Technology and Development** for their guidance, support, and constructive feedback throughout this project. Their insights played a key role in shaping our understanding of effective data visualization and dashboard development.

> Dataset retrieved from https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows