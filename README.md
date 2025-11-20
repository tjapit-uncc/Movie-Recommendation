# Movie Recommendation System

## Usage

- Open `Movie_Recommendation.ipynb`
- Run all cells using Python Kernel
- Input data files:
  - `u.data`: User-movie ratings (`user_id movie_id rating timestamp`)
  - `u.item`: Movie metadata (`movie_id | title | release_date | IMDB_website`)
  - `u.user`: User demographics (`user_id | age | gender | occupation | zip_code`)

## Output CSV Files (File: Column Names)

- `users.csv`: `user_id,age,gender,occupation`
- `movies.csv`: `movie_id,title,release_date`
- `ratings.csv`: `user_id,movie_id,rating,timestamp`

## Testing

- **User-User Collaborative Filtering**: Edit arguments for last line of cell `print(recommend_movies_for_user(10, num = 5))` based on the function definition: `def recommend_movies_for_user(user_id, num)`. Can also change `k` value (default = `5`) in this line of the function to use top `k` most similar users found: `k = 5`
- **Item-Based Collaborative Filtering**: Edit arguments for last line of cell `print(recommend_movies("Jurassic Park (1993)", num=5))` based on function definition: `def recommend_movies(movie_name, num=5)`
- **Random-Walk Based Pixie**: Edit arguments for last line of cell `print(weighted_pixie_recommend("Jurassic Park (1993)", walk_length=100, num=10))` based on function definition: `def weighted_pixie_recommend(movie_name, walk_length=15, num=5)`

## Written Reports

- `Pixie_Algorithm_Explanation.md`: Explanation of Random-Walk-Based Pixie algorithm
- `Recommendation_Report.md`: Overall report detailing the movie recommendation system, dataset, implementations of the filtering methods used, and key conclusions from the project.
