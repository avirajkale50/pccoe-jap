# Cinemate

By AVIRAJ POPAT KALE

#Video overview: <URL HERE>

## Scope

### purpose of database
The purpose of the database is to easily access the information of the a anime movie and series.It will help user to share the information they have also update the existing information in database and a log of it also there.This help animation industry for marketing as well as the production house and writer to get more famous for their work.

### Things Including in the database
- Movie and Series information with attributes like `id`, `title`,`discription`, and `price` on online platforms.
- Writer of the movie and the series with there information like `name`,`birthdate`
- Production house information with their details like `since` they exist and the `desc` discription of them
- Genre of the moviee and the series

### Things Outside in the database
- SPII information of the writers
- Financial data of production house

## Functional Requirements

### User provisions
Users should be able to:
- Create,Update and Delete the movies and series information in the database.
- Find production house and writer of the anime easily.
- Add there discription about the movie.
- Find the movie or series belong to which genere.

### Beyond the scope
- Get the personal information of the writers.
- View logs of the deleted data


## Representation

### Entities

**movie:**
- `id` (Primary Key)
- `title`
- `desc`
- `cover`
- `price`
- make the tital not null as it is important

**production_house**
- `id` (Primary Key)
- `name`
- `since`(Date when theyu get start)
- `desc`

**movie_rel_prod**
- `movie_id` (Foreign Key referencing movies)
- `Production_house_id`(Foreign Key referencing production houses)

**genre**
- `id` (Primary Key)
- `name`

**movie_rel_genre**
- `movie_id` (Foreign Key referencing movies)
- `genre_id`(Foreign Key referencing genre)

**movie_audit**
- `id` (Primary Key)
- `movie_id`
- `action`(To maintain what happen with the data)
- `old_title`
- `old_desc`
- `old_cover`
- `timestamp`(When the action get perform)

### Relationships

![Cinemate ERD](https://i.imgur.com/ibi3G21.png)

- The relation between the movie and the production house `movie_rel_prod`
- The relation between the movie and the writer `movie_rel_writer`
- The relation between the movie and the genre `movie_rel_genre`

## Optimizations
- Created the index on the `id` of the movie,production_house and in the writer table as it mostly get search
- Also the `id's` in the relation as it is important for the join

## Limitations
- The views are not there in ther database so it can be a threat to the security.
- Flatform not able to perform the financial transcation

