# music-database-project
Introduction:
Our database focuses on tracking a library of songs from the hip-hop, pop, rock, and
k-pop genres. We have collected data about the characteristics of each song, such as genre,
popularity, artist (including features), song length, date of release, and name of the album from
the Spotify database. We chose this topic because of our collective interest in music and the
opportunity to learn more about music that we may not be familiar with. This data is useful for
people of all ages, especially those with an interest in music and those looking to expand their
musical repertoire. The database emphasizes the top 50 songs from each genre from the previous
year and updates them yearly in order to stay up-to-date with the most popular music. The data
includes information such as song names, song genre, artist names, length of the song, date of
release, if it’s part of an album or a single, and the number of times played.
Each genre table in the database contains 50 records for the top 50 songs of the year
2021. This database could be an incredibly useful tool for both music professionals and fans.
With the help of this database, people would be able to quickly and easily examine the current
trends in the music industry, while fans would be able to discover new music and artists. The
database provides valuable insights into the current music trends, such as which genres are most
popular, which artists are the most successful, and what types of songs are the most popular.
Database Description:
Physical Database:
team_02_final_project_backup.sql
team_02_final_project_queries.txt
The relationship between the artist-to-song tables and the artist-to-album tables is a
many-to-many relationship, meaning that one artist can have many songs and/or albums and one
song/album can have many artists (features, co-productions, etc.). The relationship between the
genre table and the artist table is a many-to-many relationship, meaning that one artist can have
multiple genres and one genre can have multiple artists.
Sample Data
Table 1: Genres
Team Project Final Project Report
Page: 2, Team 2
Table 2: Albums
Table 3: HipHop Tracks (2021)
Table 4: Pop Tracks (2021)
Table 5: Rock/Alternative Tracks (2021)
Team Project Final Project Report
Page: 3, Team 2
Table 6: Kpop Tracks (2021)
Queries:
Query
Name
Queries
don’t use
wildcard
character
(*)
Requirement A
(4 that use 2 or
more tables -
JOIN)
Requirement B
( 3 that use
filtering -
WHERE,
HAVING, etc.)
Requirement C
(2 that use
aggregation -
SUM,
COUNT,
AVG)
Requirement D
(1 that uses a
subquery)
No 2 queries
should be
variations of
each other.
Rank
albums in
certain
genre in
order of
popularity
using
streams
✔ ✔ ✔ ✔ ✔
Finds most ✔ ✔ ✔ ✔ ✔
Team Project Final Project Report
Page: 4, Team 2
popular
single in
each genre,
based on
streams
Fastest
growing
song based
on release
date & avg.
number of
plays/day
✔ ✔
Ranks
artists that
are present
in the most
genres
(most
diverse)
✔ ✔ ✔
Sort top
newest and
oldest
released
album per
genre
✔ ✔ ✔ ✔
Finds how
many times
the most
popular
Kpop artist
(genres
table) is on
the Kpop
chart (Kpop
✔ ✔ ✔ ✔ ✔
Team Project Final Project Report
Page: 5, Team 2
table)
Changes from Original Design:
First, we have decided to remove the language column from our Genre Table as finding a
reliable data source was not possible. To have more data, we increased our song list from 20-30
songs listed to 50 songs for each table. Additionally, we have removed both the link_to_lyrics
and date_added columns from the Song Track Table as we believe these two columns are not as
useful to the users of the database as the other columns. Moreover, we have chosen to remove the
album_cover art from our album table as this feature could either slow down query searches
immensely or use too much memory. Next, we have added a genre_id and album_id column to
the four different Song Track Tables so that we can JOIN these tables with both the Genre and
Album tables.
Lessons Learned:
One lesson we learned while working on this project was figuring out how to obtain data
in an efficient way. We had planned from the beginning to use Spotify’s 2021 music charts as our
data source, but we had not determined how we were going to directly transfer the data into
pgAdmin. We learned that there are online sites that directly turn Spotify’s chart data into CSV
files. Through these sites, we were able to easily create CSV files for each genre and copy that
data into pgAdmin. Another lesson we learned was how to better use primary and foreign keys
for connecting our tables. While we started to write our queries, we realized it was difficult to
join certain tables because they had no connecting columns. This led us to add primary and
foreign key columns to help us better connect each genre table with the albums table and also
with the overall genres table.
Potential Future Work:
This database has future potential to continue collecting data every year to perform the
same operations in order to continue providing information on the latest music. Furthermore, this
database can be expanded to use data from multiple years and perform comparisons between the
years. With data from multiple years, one can analyze the performance of a particular artist year
over year or see changes in the listens and plays of certain genres.
Team Project Final Project Report
Page: 6, Team 2
Additionally, this database could also be expanded by adding different genres, such as
jazz, country, metal, or classical. As a result, more comparisons can be made between genres and
there is a wider range of music genres for users to pick and explore.
