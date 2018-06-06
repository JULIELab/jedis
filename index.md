---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

The Jena Document Information System is a UIMA-enabled architecture for automatic
linguistic text analysis. It supports large bodies of documents by the following features:
* Documents and their annotations are stored in a [Postgres] (https://www.postgresql.org/) database.
* The database contains a table for each processing task. These tables are views of the primary document data table, possibly of a subset of the complete data. Thus, they are called subset tables. Subset tables hold meta data regarding the processing state of each document, including whether it is currently in process, has finished processing or has errors. The creation, manipulation and management of document data tables and subset tables is done by the [Corpus Storage System (CoStoSys)](https://github.com/JULIELab/costosys).
* JeDIS offers a special UIMA Collection Reader and a CAS consumer, ''viz.'' the [XMI Database Reader](https://github.com/JULIELab/jcore-base/tree/2.3.0-SNAPSHOT/jcore-xmi-db-reader) and the [XMI Database Writer](https://github.com/JULIELab/jcore-base/tree/2.3.0-SNAPSHOT/jcore-xmi-db-writer). Both components support the automatic modularization of UIMA CAS documents. For each type in the type system, a module can be created and stored in the database that contains all annotations of the respective type of a CAS. The reader has parameters that allow the specification of the annotation modules to load.

