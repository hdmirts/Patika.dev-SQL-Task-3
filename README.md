# Patika.dev-SQL-Task-3
 ### dvdrental örnek veri tabanı kullanılmıştır <br>

 _tablolara sqltask3.1.csv şeklindeki başlıklardan ulaşabilirsiniz_



Aşağıdaki sorgu senaryolarını **dvdrental** örnek veri tabanı üzerinden gerçekleştiriniz.

1. **country** tablosunda bulunan **country** sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
2. **country** tablosunda bulunan **country** sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
3. **film** tablosunda bulunan **title** sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
4. **film** tablosunda bulunan tüm sütunlardaki verilerden **title** 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.

1.

```sql
select * from country
where country like 'A%a';
```

2.

```sql
select * from country
where country ilike '_____%n';
```

3.

```sql
select * from film
where title ilike '%T%';
```

4.

```sql
select * from film
where title like 'C%' and length >90 and rental_rate = 2.99;
```

