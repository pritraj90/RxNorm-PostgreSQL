# RxNorm-PostgreSQL

RxNorm Download Page [**link**](https://www.nlm.nih.gov/research/umls/rxnorm/docs/rxnormfiles.html).

## About

Scripts to create your own RxNorm Current Prescribable Content database for PostgreSQL.

## Releases

For full database creation, see [Releases](https://github.com/ZionDials/RxNorm-PostgreSQL/releases)

## Things I Have Learned

If you're like me you'll think it's awesome to have all of this drug data! Well, the data from **RxNorm is not entirely accurate**. In that, there are duplications in the data or formatting errors in their releases (the RRF files). So **the recomended order of creating the database** would be:

1. Execute table creation scripts
2. Insert all data into the created tables
3. Execute constraint scripts (and debug, because of what I have stated prior)
4. Execute all index scripts

## Case in Point

According to NLM (National Library of Medicine), the RXNREL table should be able to have a Primary Key. It is not possible to create a composite key because of the NULL values in the Data. So, yea. There is that issue. This database is made with that in mind. So I have removed `NOT NULL` constraints on the columuns that are in reality `NULL`.

---

## Folder Structure

### Constraints  ( _constraints.sql )

The primary keys for each table in their respective SQL file.

### Indexes   ( _indexes.sql )

The unique and RxNorm recomended indexes for each table in their respective SQL file.

### Scripts ( _full.sql )

The FULL table, constraint, and index creation in their respective SQL file.

### Tables ( _table.sql )

The table only creation scripts.
