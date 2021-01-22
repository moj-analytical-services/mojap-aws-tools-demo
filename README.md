# Demos on how to use our AWS Tools

If there are more tutorials I am eager to put them all as notebooks in root rather than subfolders (each with its own env). Reason being is that each of these notebooks _should_ work with a standard set of requirements. If they don't, that should force us to update some of our packages (if there is a good reason why it should be different then we move to subfolders).

To setup:

```
python -m venv env
source env/bin/activate
pip install --upgrade pip
```

Finally do one of the following:

```
pip install -r basic-requirements.txt
# OR
pip install -r requirements.txt
```

The former is what I ran to setup my env at the time of running this and the latter is my frozen env just incase something changes or you want to recreate my setup exactly.

# Tutorials

## Simple Database Creation and Manipulation

[/simple_database_creation_manipulation.ipynb]

Get some data, create a database add that data as a table in a database. Get some more data add it to the existing table.

Great place to start if you don't know what Athena, Glue, S3 are and how they fit together with our tools. Note what we run through here is the easiest way to put stuff together (it is not as airtight as using some of the other tools we use). However, it will get you most of the way there, so don't worry about it.


## Using Athena SQL to maintain and update databases

[/creating_and_maintaining_database_tables_in_athena.ipynb]

How to create new databases, add tables to a database using SQL queries and adding more data to these tables. (All using Athena SQL.)

## Data Conformance and DBs

[/data_conformance_and_dbs.ipynb]

This is a big indepth one, probably more for data engineers or people wanting to make sure their metadata is exact.

Uses aws wrangler, mojap-metadata and arrow-pd-parser to ensure conformance to and from data of different formats and also demonstrates how you can write data to/from S3 using `arrow-pd-parser`, `pyarrow` and/or `awswrangler` and also demonstrates how to create Glue schemas to query said data using `aws-wrangler` and/or the glue converter from `mojap-metadata`.


## Migrate from etl-manager to Metadata

[/etl_manager_migration.ipynb]

How to use our tools to migrate etl-manager schemas to our Metadata schemas.
