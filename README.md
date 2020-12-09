# Demo on how to use our AWS Tools

**AND WHY THEY ARE IMPORTANT**

See `data_conformance_and_dbs.ipynb`. 

If there are more tutorials I am eager to put them all as notebooks in root rather than subfolders (each with its own env). Reason being is that each of these notebooks _should_ work with a standard set of requirements. If they don't, that should force us to update some of our packages (if there is a good reason why it should be different then we move to subfolders).

To setup either:

```
python -m venv env
source env/bin/activate
pip install --upgrade pip
```

Finally 

```
pip install -r basic-requirements.txt
# OR
pip install -r requirements.txt
```

The former is what I ran to setup my env at the time of running this and the latter is my frozen env just incase something changes or you want to recreate my setup exactly.

## Tutorials

### Data Conformance and DBs

[/data_conformance_and_dbs.ipynb]

Uses aws wrangler, mojap-metadata and arrow-pd-parser to ensure conformance to and from data of different formats and also demonstrates how you can write data to/from S3 using `arrow-pd-parser`, `pyarrow` and/or `awswrangler` and also demonstrates how to create Glue schemas to query said data using `aws-wrangler` and/or the glue converter from `mojap-metadata`.
