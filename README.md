# kodluyoruzSQLAssignments
Cohorts Ödev 3 (kodluyoruz ödev 4) 

## 1) Film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız. 
<code> SELECT DISTINCT replacement_cost FROM film; </code>

## 2) film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
<code> SELECT COUNT  (DISTINCT replacement_cost) FROM film; </code>

## 3) film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
<code> SELECT COUNT (title) FROM film 
WHERE title LIKE ('T%') AND  rating = 'G'; </code>

## 4) country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
<code> SELECT COUNT(country) FROM country
WHERE length(country) = 5; </code>

## 5) city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?
<code> SELECT COUNT(city) FROM city
WHERE city ILIKE '%r'; </code>
