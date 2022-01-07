# postgreSQL_odev5
PostgreSQL -  Beşinci ödev - Ilgar Babashli

# _Q1_ 
film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.

# _Ans_
SELECT * FROM film
WHERE title LIKE ('%n')
ORDER BY length DESC
LIMIT 5;

Çıktı:
"Soldiers Evolution"
"Sorority Queen"
"King Evolution"
"Frontier Cabin"
"Wife Turn"

# _Q2_ 
film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.

# _Ans_
SELECT * FROM film
WHERE title LIKE ('%n')
ORDER BY length ASC
OFFSET 5
LIMIT 5;

Çıktı:
"Jekyll Frogmen"
"Daughter Madigan"
"Room Roman"
"Camelot Vacation"
"Birds Perdition"

# _Q3_ 
customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
# _Ans_
SELECT * FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;

Çıktı:
28	1	"Cynthia"	"Young"	"cynthia.young@sakilacustomer.org"	32	true	"2006-02-14"	"2013-05-26 14:49:45.738"	1
402	1	"Luis"	"Yanez"	"luis.yanez@sakilacustomer.org"	407	true	"2006-02-14"	"2013-05-26 14:49:45.738"	1
318	1	"Brian"	"Wyman"	"brian.wyman@sakilacustomer.org"	323	true	"2006-02-14"	"2013-05-26 14:49:45.738"	1
107	1	"Florence"	"Woods"	"florence.woods@sakilacustomer.org"	111	true	"2006-02-14"	"2013-05-26 14:49:45.738"	1



