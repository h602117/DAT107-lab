# Lab veke 3

## Oppgåve a

```sql
SELECT *
FROM ansatt;
```

## Oppgåve b

```sql
SELECT *
FROM ansatt 
WHERE date_part('year', ansattdato) > 2010;
```

## Oppgåve c

```SQL
SELECT *
FROM ansatt 
WHERE date_part('year', ansattdato) BETWEEN 2004 AND 2012;
```

## Oppgåve d

```SQL
SELECT *
FROM ansatt 
WHERE date_part('year', ansattdato) != 1999;
```

## Oppgåve e

```SQL
SELECT *
FROM ansatt 
WHERE etternavn LIKE '%sen';
```

## Oppgåve f

```SQL
SELECT *
FROM ansatt 
WHERE etternavn LIKE '%sen' AND date_part('year', ansattdato) > 2012;
```

## Oppgåve g

```SQL
SELECT *
FROM ansatt 
WHERE etternavn LIKE '%sen' AND date_part('year', ansattdato) NOT IN (2010, 2011, 2012);
```

## Oppgåve h

```SQL
SELECT *
FROM ansatt 
WHERE etternavn LIKE '%sen' AND date_part('year', ansattdato) < 2015 AND lonn > 400000;
```

## Oppgåve i

```SQL
SELECT *
FROM ansatt 
WHERE etternavn LIKE '%sen' AND date_part('year', ansattdato) < 2015 AND stilling = 'Tekstforfatter';
```

## Oppgåve j

```SQL
SELECT *
FROM ansatt 
WHERE etternavn NOT LIKE '%sen';
```

## Oppgåve k

```SQL
SELECT ansattnr, etternavn, stilling
FROM ansatt;
```

## Oppgåve l

```SQL
SELECT ansattnr, etternavn, stilling
FROM ansatt 
WHERE date_part('year', ansattdato) > 2000;
```

## Oppgåve m

```SQL
SELECT ansattnr, etternavn, stilling
FROM ansatt 
WHERE date_part('year', ansattdato) > 2000 AND (etternavn LIKE '%sen' OR lonn > 500000);
```

## Oppgåve n

```SQL
SELECT ansattnr, etternavn, stilling
FROM ansatt 
WHERE date_part('year', ansattdato) > 2000 OR etternavn LIKE '%sen' OR lonn > 500000 ORDER BY lonn ASC;
```

## Oppgåve o

```SQL
SELECT ansattnr, etternavn, stilling
FROM ansatt 
WHERE date_part('year', ansattdato) > 2000 AND etternavn LIKE '%sen' AND lonn > 500000 ORDER BY lonn DESC;
```

## Oppgåve p

```SQL
SELECT ansattnr, lonn
FROM ansatt 
WHERE lonn > 400000;
```

## Oppgåve q

```SQL
SELECT AVG(lonn)
FROM ansatt;
```

## Oppgåve r

```SQL
SELECT AVG(lonn)
FROM ansatt
GROUP BY stilling;
```

## Oppgåve s

```SQL
SELECT AVG(lonn)
FROM ansatt
WHERE date_part('year', ansattdato) < 2000;
```

## Oppgåve t

```SQL
SELECT AVG(lonn)
FROM ansatt
WHERE date_part('year', ansattdato) > 2000;
```

