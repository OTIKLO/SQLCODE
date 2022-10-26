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
