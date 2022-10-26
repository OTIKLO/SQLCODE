# SQLCODE
SQL 관련 정리

```
SELECT count(DISTINCT Name)
From ANIMAL_INS
Where Name IS NOT Null
Order by Name;
```

```
SELECT NAME
From ANIMAL_INS
Where 1=1 AND DATETIME IN (SELECT MIN(DATETIME) FROM ANIMAL_INS);
```

```
SELECT count(*)
FROM USER_INFO
WHERE age >=20 AND age <=29
AND JOINED BETWEEN '2021-01-01 00:00:00' AND '2021-12-31 23:59:59';
```

```
SELECT ANIMAL_ID, NAME, DATETIME
FROM ANIMAL_INS
ORDER BY NAME, DATETIME desc;
```

```
SELECT Name, Count(Name)
FROM ANIMAL_INS
GROUP BY NAME
HAVING COUNT(NAME) >= 2
ORDER BY NAME;
```

```
SELECT ANIMAL_TYPE, CASE WHEN NAME IS NULL THEN 'No name' ELSE NAME END,
SEX_UPON_INTAKE
FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
```
CASE WHEN ~ IS NULL THEN ~ ELSE ~ END

```
SELECT ANIMAL_ID, NAME, DATE_FORMAT(DATETIME, '%Y-%m-%d') AS '날짜'
FROM ANIMAL_INS
ORDER BY ANIMAL_ID
```
