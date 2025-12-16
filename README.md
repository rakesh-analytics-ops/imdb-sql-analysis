
# IMDb Movie Analytics – SQL Project

## 📌 Project Overview
This project involves analyzing IMDb movie data using SQL to derive insights
related to movies, directors, actors, genres, ratings, and voting patterns.
The analysis focuses on answering business-driven questions using structured queries.

## 🛠 Tools & Technologies
- SQL (MySQL / MS SQL Server)
- IMDb Dataset

## 📂 Analysis Performed
- Movie count analysis by year, country, and genre
- Director and actor performance analysis
- Rating and voting pattern analysis
- Identification of top-performing genres and production houses

## 📁 Project Structure
- `sql/imdb_analysis.sql` – SQL queries used for analysis
- `report/IMDb_SQL_Analysis_Report.pdf` – Summary of findings and insights

## 🎯 Outcome
The project demonstrates strong SQL querying skills, including joins,
aggregations, subqueries, filtering, and business-focused data analysis.

**Author:** Rakesh Mahakur
-- IMDb Movie Analytics Project
-- Author: Rakesh Mahakur

-- Q1: Total number of movies released per year
SELECT 
    YEAR(date_published) AS release_year,
    COUNT(*) AS total_movies
FROM movie
GROUP BY YEAR(date_published)
ORDER BY release_year;

-- Q2: Top 10 genres by average rating
SELECT 
    g.genre,
    AVG(r.avg_rating) AS avg_rating
FROM genre g
JOIN ratings r ON g.movie_id = r.movie_id
GROUP BY g.genre
ORDER BY avg_rating DESC
LIMIT 10;
-- IMDb Movie Analytics Project
-- Author: Rakesh Mahakur

-- Q1: Total number of movies released per year
SELECT 
    YEAR(date_published) AS release_year,
    COUNT(*) AS total_movies
FROM movie
GROUP BY YEAR(date_published)
ORDER BY release_year;

-- Q2: Top 10 genres by average rating
SELECT 
    g.genre,
    AVG(r.avg_rating) AS avg_rating
FROM genre g
JOIN ratings r ON g.movie_id = r.movie_id
GROUP BY g.genre
ORDER BY avg_rating DESC
LIMIT 10;
