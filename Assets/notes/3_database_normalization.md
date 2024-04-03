# [Database Fundalmentals](../../README.md)
## 3. Database Normalization

- [Database Fundalmentals](#database-fundalmentals)
  - [3. Database Normalization](#3-database-normalization)
    - [Initial Data (no normalized)](#initial-data-no-normalized)
    - [(1NF) First Normal Form](#1nf-first-normal-form)
    - [(2NF) Second Normal Form](#2nf-second-normal-form)
    - [(3NF) Third Normal Form \[5\]](#3nf-third-normal-form-5)
    - [(4NF) Fourth Normal Form](#4nf-fourth-normal-form)


To normalize a database is to apply certain rules so it is easier to manage by engineers. A Normalized database should comply with the [12 Edgar Codd's Rules](https://en.wikipedia.org/wiki/Codd%27s_12_rules). 

> **Database normalization** is a technique for [creating database tables](https://phoenixnap.com/kb/how-to-create-a-table-in-mysql) with suitable columns and keys by decomposing a large table into smaller logical units. The process also considers the demands of the environment in which [the database](https://phoenixnap.com/kb/what-is-a-database) resides.
>
> Normalization is an **iterative process.** Commonly, normalizing a database occurs through a series of tests. Each subsequent step decomposes tables into more manageable information, making the overall database logical and easier to work with.
>
> —[phoenixLab](https://phoenixnap.com/kb/database-normalization)

### Initial Data (no normalized)

![datatypes](Assets/images/initial_data.svg)

### (1NF) First Normal Form

No repeated columns or no colums with multiple values

Conditions:

- Every attribute is [atomic](#atomic_attribute).
- The number of columns is the same in every case (even if an attribute has multiple values). In the example above, the attibute "course" has multiple values, thats why it is represented in two columns.

![datatypes](Assets/images/1nf.svg)

### (2NF) Second Normal Form

Each item has a unique key. A primary key autimatically satisfies 2NF.

![datatypes](Assets/images/2nf.svg)

### (3NF) Third Normal Form [5]

- Every [non-prime](#non-prime_attribute) attribute of R is non-transitively dependent on every key of R.

- A [transitive dependency](https://en.wikipedia.org/wiki/Transitive_dependency) is a [functional dependency](https://en.wikipedia.org/wiki/Functional_dependency) in which _X_ → _Z_ (*X* determines _Z_) indirectly, by virtue of _X_ → _Y_ and _Y_ → _Z_ (where it is not the case that _Y_ → _X_).

![datatypes](Assets/images/3nf.svg)

### (4NF) Fourth Normal Form

Every non-trivial functional or [multivalued dependency](https://en.wikipedia.org/wiki/Multivalued_dependency) begins with a superkey.

![datatypes](Assets/images/4nf.svg)
