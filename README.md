---
data_name: Human readable name of dataset, e.g. ADGC, GTEx, etc.
accession: dbGaP, NIAGADS, EGA, etc accession code
source: URL of data. Additional instructions should be put in body
data_type: [WGS, WES, Phenotype, Expression, eQTL, etc]
date_release: Optional; Date that dataset was made available to the public
date_downloaded: date YOU downloaded the files
use_permissions: one of public, public_dua, or private
lab_lead: your name
uses: # Any time you publish something, link to the analysis directory here
  - path1
  - path2
---

# DELETE THIS: Suggested directory structure

Here is a suggested directory structure. Modify file locations as needed,
but keep it as close as possible to the below tree:

```
project_dir
├── README.md (document your workflow)
├── .gitignore (ignore outputs you don't want to track)
├── config/ (you can put multiple config files here)
│   └── config.yaml
├── docs/
│   ├── data_use/ (latest DUAs, access lists, agreements and applications go here)
│   ├── workflow/ (DAGs, more detailed docs)
│   └── dataset/ (original documentation from datatset)
├── workflow/ (your pipeline goes here)
│   ├── rules/ (subworkflows)
│   │   ├── module1.smk
│   │   └── module2.smk
│   ├── envs/ (conda envs for reproducability)
│   │   ├── env1.yaml
│   │   └── env2.yaml
│   ├── report/ (output report scripts/templates)
│   └── Snakefile
├── resources/ (non-workflow dependancies of your pipeline)
│   ├── reference/ (Optional: put reference files or symlinks here)
│   ├── src/ (Optional: non conda/container software)
│   └── raw/ (Optional: can symlink raw files into this)
├── results/ (final output goes here)
│   ├── reports/
│   ├── images/
│   ├── genotypes/
│   ├── phenotypes/
│   ├── expression/
│   └── sumstats/
├── intermediate/ (Optional: non-temporary intermediates go here)
└── temp/ (Optional: temporary intermediates go here)
```

<!---
Generated using https://tree.nathanfriend.io/:
project_dir
  README.md (document your workflow)
  .gitignore (ignore outputs you don't want to track)
  config/ (you can put multiple config files here)
    config.yaml
  docs/
    data_use/ (latest DUAs, access lists, agreements and applications go here)
    workflow/ (DAGs, more detailed docs)
    dataset/ (original documentation from datatset)
  workflow/ (your pipeline goes here)
    rules/ (subworkflows)
      module1.smk
      module2.smk
    envs/ (conda envs for reproducability)
      env1.yaml
      env2.yaml
    report/ (output report scripts/templates)
    Snakefile
  resources/ (non-workflow dependancies of your pipeline)
    reference/ (Optional: put reference files or symlinks here)
    src/ (Optional: non conda/container software)
    raw/ (Optional: can symlink raw files into this)
  results/ (final output goes here)
    reports/
    images/
    genotypes/
    phenotypes/
    expression/
    sumstats/
  intermediate/ (Optional: non-temporary intermediates go here)
  temp/ (Optional: temporary intermediates go here)
--->


# data_name processed fileset

Put information about the dataset and its uses here

## Access details

Talk in generalities about how the data is allowed to be used here. You can link to files in the `documentation/data_use` folder.

## Download Instructions

Instructions for downloading the dataset. If there are passwords or other sensitive information, DO NOT put them here because this will be on GitHub. Those details can go in the parent directory.

## Processing

What you did to the raw data

### Installation

If there are any things that need to be done other than cloning the repo (e.g. symlinks or downloads), talk about them here.

### Workflow

Document the major QC and processing steps used in data processing. This will make manuscript writing easier. If you're using standardized pipelines, you can link to them.

### Configuration

Document the configuration file here, along with the choices you made for config options
