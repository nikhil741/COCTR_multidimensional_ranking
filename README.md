## Paper Description
This contains the codebase and the annotated relevant trial set for each of the 25 queries, for the paper titled **Towards an Aspect-based Ranking Model for Clinical Trial Search** accepted in the [8th International Conference on Computational Data and Social Networks (CSoNet 2019)](http://optnetsci.cise.ufl.edu/CSoNet/). 

Paper link is coming up!

## UMLS concept based retrieval and aspect based ranking model of clinical trials

### Requirements
1. Dump Of the Clinical Trials from the follwing link.
[https://clinicaltrials.gov/AllPublicXML.zip]

2. Setup of QuickUMLS tool.
[https://github.com/Georgetown-IR-Lab/QuickUMLS]

3. Download Adversity Events Reported from the site.
[https://aact.ctti-clinicaltrials.org/pipe_files]

4. Download Elastic Search for the baseline.

5. Baseline code [https://github.com/ajinkyathorve/TREC-2017-PM-CDS-Track].

6. All environment packages in [requirements.txt] file.


### Folder strucutre and descriptions 

#### allAnnotatedData
1. It contains the 25 annotated queries.
2. 5 queries for each disease class.

#### baselineSetup [https://github.com/ajinkyathorve/TREC-2017-PM-CDS-Track]
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