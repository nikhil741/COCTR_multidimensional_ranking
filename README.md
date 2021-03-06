## Paper Description
This contains the codebase and the annotated relevant trial set for each of the 25 queries, for the paper titled **Towards an Aspect-based Ranking Model for Clinical Trial Search** accepted in the [8th International Conference on Computational Data and Social Networks (CSoNet 2019)](http://optnetsci.cise.ufl.edu/CSoNet/). 

[Paper link:](https://link.springer.com/chapter/10.1007/978-3-030-34980-6_25)

## UMLS concept based retrieval and aspect based ranking model of clinical trials

### Requirements
1. Download the dump of the clinical trials from the [link](https://clinicaltrials.gov/AllPublicXML.zip)
2. Setup [QuickUMLS](https://github.com/Georgetown-IR-Lab/QuickUMLS) tool 
3. Download the adversity events reported from the [site](https://aact.ctti-clinicaltrials.org/pipe_files)
4. Base Line Setup
    1. Download and setup Elastic search for the baseline.
    2. For the baseline code [refer](https://github.com/ajinkyathorve/TREC-2017-PM-CDS-Track)
5. All environment packages are listd in [requirements.txt] file.


### Folder strucutre & description

#### allAnnotatedData
1. It contains the 25 annotated queries.
2. 5 queries for each disease class.

#### baselineSetup [refer](https://github.com/ajinkyathorve/TREC-2017-PM-CDS-Track)
1. Scripts for indexing trials for each class of disease and script for retriving and ranking trials on the basis of query.

#### bigTableAndSmallTable
1. Calculates the precision, speraman's rank order correlation and overlap across 25 final queries retrieved trials and ranked on the basis of relevancy(5-methods) 

#### commonPatientSearchedTerms
1. QuickUMLS tool applied over 1440 lexicons of medDRA common patient terms
2. Finds the problematic queries.

#### datasetPreparation
1. Get PubMedIds for the clinical trials.
2. Map clinical trials linked with PubMed-Ids to different classes(26) of disease with all extra fields(Adversity, popularity) appended.

#### goldStandardDataTREC_2018
Robustness study
1. Precision@10
2. Recall

#### rankedTrialsOnDifferentRelevancyBasedSchemes
1. Contains trials in ranked order on the basis of different relevancy (pageRank, Exact Match, SynSet) based approach.

#### rankingOnTheBasisOfRelevancyAndAddingColumnsForInclusionExclusionCounts
1. Rank retrieved trials for 25 quries on the basis of different relevancy(25) methods.

#### All_Importan_Data_And_Dump_Data
1. 5 class Csv Files with all fields appended.
2. Pickle File of UMLS concepts for each trial across 5 disease classes.
3. Ranked trials on the basis of 5 relevancy based methodologies.
4. Dump files.

#### clusteringSourceFiles
1. Contains application of different clustering algorithm like DBScan, Affinity Algorithms on different variations of the data.

### Citation information
If you use the codes or the dataset, please cite the paper.
#### Bibtex
    @InProceedings{10.1007/978-3-030-34980-6_25,
    author="Roy, Soumyadeep
    and Rudra, Koustav
    and Agrawal, Nikhil
    and Sural, Shamik
    and Ganguly, Niloy",
    editor="Tagarelli, Andrea
    and Tong, Hanghang",
    title="Towards an Aspect-Based Ranking Model for Clinical Trial Search",
    booktitle="Computational Data and Social Networks",
    year="2019",
    publisher="Springer International Publishing",
    address="Cham",
    pages="209--222",
    doi="10.1007/978-3-030-34980-6_25",
    isbn="978-3-030-34980-6"
    }
