# Assignment

For today's assignment, you will store library book information.  As a result, you will need to create a MySQL database with the following criteria:

| Column          | Constraint |
|-----------------|------------|
| Author          | 18 chars   |
| Title           | 44 chars   |
| Publish Date    | N/A        |

**NOTE:** The primary key for this table should be auto incrementing.

Once the table is created, do the following:

* Add the following records:

| Author              | Title             | Date Published  |
|---------------------|-------------------|-----------------|
| Leo Tolstoy         | Anna Karenina     | January 1, 1878 |
| Homer               | Odyssey           | January 1, 1541 |
| Charles Dickens     | David Copperfield | May 1, 1849     |
| Frank Hubert        | Dune              | June 1, 1965    |
| F. Scott Fitzgerald | The Great Gatsby  | April 10, 1925  |

* Select all entries in the table
* Select only the titles
* Select all entries based on publish date (earliest to recent)