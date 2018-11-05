# RxNorm-PostgreSQL

## About

RxNorm Download Page [**link**](https://www.nlm.nih.gov/research/umls/rxnorm/docs/rxnormfiles.html).

## Things I Have Learned

If you're like me you'll think it's awesome to have all of this drug data! Well, the data from **RxNorm is not entirely accurate**. In that, there are duplications in the data or formatting errors in their releases (the RRF files). So **the recomended order of creating the database** would be:

1. Execute table creation scripts
2. Insert all data into the created tables
3. Execute constraint scripts (and debug, because of what I have stated prior)
4. Execute all index scripts

---

## Folder Structure

### Constraints

The primary keys for each table in their respective SQL file.

### Indexes

The unique and RxNorm recomended indexes for each table in their respective SQL file.

### Scripts

The FULL table, constraint, and index creation in their respective SQL file.

### Tables

The table only creation scripts.
