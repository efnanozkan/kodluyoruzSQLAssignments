# kodluyoruzSQLAssignments
## Cohorts Ödev 3 (kodluyoruz ödev 4) 

### 1) Film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız. 
<code> SELECT DISTINCT replacement_cost FROM film; </code>

### 2) film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
<code> SELECT COUNT  (DISTINCT replacement_cost) FROM film; </code>

### 3) film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
<code> SELECT COUNT (title) FROM film 
WHERE title LIKE ('T%') AND  rating = 'G'; </code>

### 4) country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
<code> SELECT COUNT(country) FROM country
WHERE length(country) = 5; </code>

### 5) city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?
<code> SELECT COUNT(city) FROM city
WHERE city ILIKE '%r'; </code>


## Cohorts Ödev 4 (kodluyoruz ödev 7) 
### 1) Film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
<code> SELECT rating, COUNT(*) FROM film
GROUP BY rating ;  </code>

### 2) film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
<code> SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(replacement_cost)>50 ; </code>

### 3) customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
<code> SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id; </code>

### 4) city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
<code> SELECT country_id , COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1 ; </code> 
