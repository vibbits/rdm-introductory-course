According to the FAIRCookBook 10.4.1 Metadata model for transcriptomics, the suggested metadata fields are the following ones listed below: https://faircookbook.elixir-europe.org/content/recipes/interoperability/transcriptomics-metadata.html#transcriptomics-data-model 


|Metadata field|Required?|Definition|Comment|Metadata field GEO|
|--------|--------|--------|--------|-------|
|||||project title|
|project summary||||summary|
|study title||||Title|
|center name||||Lab, Organisation name|
|||||study name|
|||||experiment accession|
|||||experiment type|
|||||run accession|
|||||sample title|
|||||source name|
|unique ID|required|Identifier for a sample that is at least unique within the project||sample accession|
|sample type|required|The type of the collected specimen, eg tissue biopsy, blood draw or throat swab|`ontology field` - e.g. OBI or EFO||
|species|required|The primary species of the specimen, preferably the taxonomic identifier|This may not be the same as the "host" organism, eg in the case of a PDX tissue sample, the host may be a mouse but the tissue may be human. Ontology field - NCBITaxonomy|tax id|
|organism|required|The primary species of the specimen, preferably the taxonomic identifier|This may not be the same as the "host" organism, eg in the case of a PDX tissue sample, the host may be a mouse but the tissue may be human. Ontology field - NCBITaxonomy|organism|
|tissue/organism part|required|The tissue from which the sample was taken|`ontology field` - e.g. Uberon|tissue/cell line|
|disease|required|Any diseases that may affect the sample|This may not necessarily be the same as the host's disease, eg healthy brain tissue might be collected from a host with type II diabetes while cirrhotic liver tissue might be collected from an otherwise healthy individual. Ontology field - e.g. MONDO or DO||
|sex|required|The biological/genetic sex of the sample|`ontology field` - e.g. PATO||
|development stage|required|The developmental stage of the sample|`ontology field` - e.g. Uberon or Hsadpdv; species dependent|developmental stage|
|collection date|required|The date on which the sample was collected, in a standardised format|Collection date in combination with other fields such as location and disease may be sufficient to de-anonymise a sample||
|external accessions|recommended|Accession numbers from any external resources to which the sample was submitted|eg Biosamples, Biostudies||
|strain|recommended|Strain of the species from which the sample was collected, if applicable|`ontology field` - e.g. NCBITaxonomy||
|ancestry/ethnicity|recommended|Ancestry or ethnic group of the individual from which the sample was collected|`ontology field` - e.g. HANCESTRO||
|age |recommended|Age of the organism from which the sample was collected||
|age unit|recommended|Unit of the value of the age field|`ontology field` - e.g. UO||
|BMI|recommended|Body mass index of the individual from which the sample was collected|Only applies to human samples||
|treatment category|recommended|Treatments that the sample might have undergone after collection|`ontology field` - e.g. OBI, NCIt or OGMS||
|cell type|recommended|The cell type(s) known or selected to be present in the sample|`ontology field` - e.g. CL|source name|
|growth conditions|recommended|Features relating to the growth and/or maintenance of the sample|||
|genetic variation|recommended|Any relevant genetic differences from the specimen or sample to the expected genomic information for this species, eg abnormal chromosome counts, major translocations or indels|||
|sample collection technique|recommended|The technique used to collect the specimen, eg blood draw or surgical resection|`ontology field` - e.g. EFO or OBI||
|phenotype|recommended|Any relevant (usually abnormal) phenotypes of the specimen or sample |`ontology field` - e.g. HP or MP; species dependent||
|cell cycle|recommended|The cell cycle phase of the sample (for synchronized growing cells or a single-cell sample), if known|`ontology field` - e.g. GO||
|cell location|recommended|The cell location from which genetic material was collected (usually either nucleus or mitochondria)|`ontology field` - e.g. GO||