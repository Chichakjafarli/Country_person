This script will create the person_country table with the specified columns and insert the provided data into the table.
```sql
CREATE TABLE peraon_country (
    id INT,
    name VARCHAR(20),
    surname VARCHAR(20),
    height INT,
    weight INT,
    age INT,
    gender VARCHAR(20),
    Country VARCHAR(20)
);

INSERT INTO peraon_country VALUES (1, 'Ali', 'Yilmaz', 180, 64, 20, 'M', 'TR');
INSERT INTO peraon_country VALUES (2, 'Jack', 'Wender', 192, 88, 21, 'M', 'USA');
INSERT INTO peraon_country VALUES (3, 'Isabella', 'Gabriel', 166, 48, 19, 'W', 'ES');
INSERT INTO peraon_country VALUES (4, 'Maya', 'Hess', 174, 57, 21, 'W', 'DE');
INSERT INTO peraon_country VALUES (5, 'Merve', 'Yavuz', 180, 65, 22, 'W', 'TR');
INSERT INTO peraon_country VALUES (6, 'Fuad', 'Hasanov', 192, 89, 21, 'M', 'AZ');
```

Find all the data in the table
```sql
Select * from peraon_country;
```
| id | name     | surname | height | weight | age | gender | country |
|----|----------|---------|--------|--------|-----|--------|---------|
| 1  | Ali      | Yilmaz  | 180    | 64     | 20  | M      | TR      |
| 2  | Jack     | Wender  | 192    | 88     | 21  | M      | USA     |
| 3  | Isabella | Gabriel | 166    | 48     | 19  | W      | ES      |
| 4  | Maya     | Hess    | 174    | 57     | 21  | W      | DE      |
| 5  | Merve    | Yavuz   | 180    | 65     | 22  | W      | TR      |
| 6  | Fuad     | Hasanov | 192    | 89     | 21  | M      | AZ      |

Find the name and surname of the athletes from the table.
```sql
Select name,surname from peraon_country;
```
| name     | age |
|----------|-----|
| Isabella | 19  |
| Ali      | 20  |
| Jack     | 21  |
| Maya     | 21  |
| Fuad     | 21  |
| Merve    | 22  |

Find the athletes who are older than 20 years old.
```sql
Select * from peraon_country where age>20;
```

| id | name  | surname | height | weight | age | gender | country |
|----|-------|---------|--------|--------|-----|--------|---------|
| 2  | Jack  | Wender  | 192    | 88     | 21  | M      | USA     |
| 4  | Maya  | Hess    | 174    | 57     | 21  | W      | DE      |
| 5  | Merve | Yavuz   | 180    | 65     | 22  | W      | TR      |
| 6  | Fuad  | Hasanov | 192    | 89     | 21  | M      | AZ      |

Find the athletes who are younger than or equal to 20 years old.
```sql
Select * from peraon_country where age<=20;
```
| id | name     | surname | height | weight | age | gender | country |
|----|----------|---------|--------|--------|-----|--------|---------|
| 1  | Ali      | Yilmaz  | 180    | 64     | 20  | M      | TR      |
| 3  | Isabella | Gabriel | 166    | 48     | 19  | W      | ES      |

Find the name and age of the athletes by ordering younger to older  in the ascending order.
```sql
Select name,age from peraon_country order by age asc;
```
| name     | age |
|----------|-----|
| Isabella | 19  |
| Ali      | 20  |
| Jack     | 21  |
| Maya     | 21  |
| Fuad     | 21  |
| Merve    | 22  |