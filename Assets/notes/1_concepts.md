# [Database Fundalmentals](../../README.md)
## 1. Concepts

- [Database Fundalmentals](#database-fundalmentals)
  - [1. Concepts](#1-concepts)
    - [Data Persistance](#data-persistance)
    - [Relational vs. Non-Relational](#relational-vs-non-relational)
    - [Services](#services)
    - [Definitions](#definitions)


### Data Persistance

**History of Persistance** - We need to store data since the birth of humanity.

1. Word of mouth.
2. Stone - Keep information from changing and outlive a human.
3. Papyrus and parchment - Ease of use and portability.
4. Paper - Better degradation resistance.
5. Microfilm - Practically does not degrade but [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) became more dificult.
6. Digital storage - Massive amounts of information in small spaces.
7. The Cloud - Omnipresence (within the internet) and reliability.

### Relational vs. Non-Relational

https://aukera.es/blog/bases-de-datos-relacionales-vs-no-relacionales/

1. Relational

   > Examples:
   >
   > - SQL Server
   > - Oracle
   > - PostgreSQL
   > - MySQL
   > - MariaDB - MySQL Fork

2. Non-relational

   > Examples:
   >
   > - Memcache
   > - Cassandra
   > - DynamoDP
   > - Elastic Search
   > - Big Query
   > - neo4j
   > - MongoDB
   > - Firesurf

### Services

- Self-managed
- Managed: This are services like Azure, AWS, GCP.

### Definitions

- **<a name="atomic_attribute">Atomic Attibute:</a>** An attribute that cannot be divided further into **meaningful** subcomponents/sub-attributes is an Atomic attribute. Example 1: Name can be divided into First Name and Last Name. Example 2: A list of courses can be divided into each particular course.
- **<a name="functional_dependency">Functional Dependency:</a>** Given a relation _R_ and sets of attributes _X_,_Y_ $\subseteq R$, _X_ is said to **functionally determine** _Y_ (written _X_ $\to $ _Y_) if and only if each _X_ value in _R_ is associated with precisely one _Y_ value in _R_; _R_ is then said to _satisfy_ the functional dependency _X_ $\to$ _Y_.
- **<a name="non-prime_attribute">Non-prime attribute:</a>**  A _non-prime attribute_ of R is an attribute that does not belong to any [candidate key](https://en.wikipedia.org/wiki/Candidate_key) of R [[3](https://en.wikipedia.org/wiki/Third_normal_form#cite_note-Codd2-3)].