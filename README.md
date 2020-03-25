# getting_started

## Team Chat on Matrix
We use Matrix to communicate (https://matrix.org/). Riot is the standard client for Matrix (https://about.riot.im/)

How to get started:
- Download Riot or start the web app: https://about.riot.im/downloads
- Create an account on the free matrix.org homeserver
- send us your username (something like @myusername:matrix.org)


## Public graph database
The database is hosted on covid.petesis.com with a public read only user.

Currently there is an issue with Chrome/Chromium and the SSL certificate. You cannot access the Neo4j Browser via HTTPS in Chrome.

- Neo4j browser: https://covid.petesis.com:7473
- Bolt URL: bolt://covid.petesis.com:7687

- user: public
- password: corona

## Adding knowledge from genes, transcripts and proteins from public databases
We added several well known sources from public databases

- Genes: Added 128'709 Gene names (actually gene symbols) from **Ensembl**
  - > Example: name: CNR2, sid: ENSG00000188822, source: Ensembl, taxid: 9606
- Transcripts: Added 409'882 transcripts from **Ensembl** and **RefSeq**
  - > Example: sid: ENST00000374472 source: Ensembl taxid: 9606
  - > Example: length: 3645sid: XM_017000261source: Refseqstatus: MODELtaxid: 9606
- Proteins: Added 483'906 protein names from **Uniprot**, **RefSeq**, **Ensembl**
  - > Example: category: secondarys id: Q4VBK8 source: Uniprot taxid: 9606
  - > Example: sid: ENSP00000363596 source: Ensembl taxid: 9606
  - > Example: category: primary desc: RecName: Full=Cannabinoid receptor 2 name: Cannabinoid receptor 2sid: P34972 source: Uniprot
  
## Connecting genes, transcripts and proteins
We connect (=map) each gene, transcript and protein with its synonyms, respectively

## Connecting genes, transcripts and proteins to Abstracts
We indexed all abstracts and connected  genes, transcripts and proteins if they *mentioned* in the specific abstract
