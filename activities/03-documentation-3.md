According to the FAIRCookBook 10.4.1 Metadata model for transcriptomics, the suggested metadata fields are the following ones listed below: https://faircookbook.elixir-europe.org/content/recipes/interoperability/transcriptomics-metadata.html#transcriptomics-data-model 

For ENA submissions, an extensive list of metadata templates is [here](https://github.com/ELIXIR-Belgium/ENA-metadata-templates) 

|Section|Metadata field|Required?|Definition|Comment|Metadata field GEO|Metadata field ENA|
|------|--------|--------|--------|--------|-------|------|
|Project|||Unique identificator for a study. This is used to link experiments to the study.||project title|Project/Study title/alias|
|Project|||Title of the study as would be used in a publication.||project title|Project/Study name|
|Project|project summary||Briefly describes the goals, purpose, and scope of the Study. This need not be listed if it can be inherited from a referenced publication.||summary|study summary/abstract|
|Project|literature reference||||publications|pudmed id|
|Project|center name||Lab, Organisation name||Lab, Organisation name|Center Name|
|Experiment|||Short text that can be used to call out experiment records in searches or in displays. This element is technically optional but should be used for all new records.||experiment ?|experiment title|
|Experiment|||Goal and setup of the individual library including library was constructed.||?|design description|
|Experiment|||Free form text describing the protocol by which the sequencing library was constructed.||construction protocol|construction protocol|
|Experiment|||Sequencing technique intended for this library.||Library Strategy|Library Strategy|
|Experiment|||The LIBRARY_SOURCE specifies the type of source material that is being sequenced.||Library source|Library source|
|Experiment|||Method used to enrich the target in the sequence library preparation||Library selection|Library selection|
|Experiment|||LIBRARY_LAYOUT specifies whether to expect single, paired, or other configuration of reads. In the case of paired reads, information about the relative distance and orientation is specified.||Library layout|Library layout|
|Experiment|||Model of the sequencing instrument.||Instrument|instrument model|
|Experiment|||The PLATFORM record selects which sequencing platform and platform-specific runtime parameters. This will be determined by the Center. Optional if 'instrument_model' is provided.
instrument_model 	Mandatory 	||Platform|instrument platform|
|Run|||Unique identificator for each run.||run accession|run alias|
|Run|||The name or relative pathname of a run data file.||file name|file name|
|Sample|unique ID|required|Identifier for a sample that is at least unique within the project||sample accession|sample alias|
|Sample|title|required|Short text that can be used to call out sample records in search results or in displays||sample title|sample title|
|Sample|sample type|required|The type of the collected specimen, eg tissue biopsy, blood draw or throat swab|`ontology field` - e.g. OBI or EFO|||
|Sample|species|required|The primary species of the specimen, preferably the taxonomic identifier|This may not be the same as the "host" organism, eg in the case of a PDX tissue sample, the host may be a mouse but the tissue may be human. Ontology field - NCBITaxonomy|tax id|tax id|
|Sample|scientific name|required|Scientific name of sample that distinguishes its taxonomy. Please use a name or synonym that is tracked in the INSDC Taxonomy database. Also, this field can be used to confirm the TAXON_ID setting|This may not be the same as the "host" organism, eg in the case of a PDX tissue sample, the host may be a mouse but the tissue may be human. Ontology field - NCBITaxonomy|organism|scientific name|
|Sample|tissue/organism part|required|The tissue from which the sample was taken|`ontology field` - e.g. Uberon|tissue/cell line||
|Sample|disease|required|Any diseases that may affect the sample|This may not necessarily be the same as the host's disease, eg healthy brain tissue might be collected from a host with type II diabetes while cirrhotic liver tissue might be collected from an otherwise healthy individual. Ontology field - e.g. MONDO or DO|||
|Sample|sex|required|The biological/genetic sex of the sample|`ontology field` - e.g. PATO|||
|Sample|development stage|required|The developmental stage of the sample|`ontology field` - e.g. Uberon or Hsadpdv; species dependent|developmental stage|development stage|
|Sample|collection date|required|The date on which the sample was collected, in a standardised format|Collection date in combination with other fields such as location and disease may be sufficient to de-anonymise a sample||collection date|
|Sample|external accessions|recommended|Accession numbers from any external resources to which the sample was submitted|eg Biosamples, Biostudies|||
|Sample|strain|recommended|Strain of the species from which the sample was collected, if applicable|`ontology field` - e.g. NCBITaxonomy||
|Sample|ancestry/ethnicity|recommended|Ancestry or ethnic group of the individual from which the sample was collected|`ontology field` - e.g. HANCESTRO|||
|Sample|age |recommended|Age of the organism from which the sample was collected||
|Sample|age unit|recommended|Unit of the value of the age field|`ontology field` - e.g. UO|||
|Sample|BMI|recommended|Body mass index of the individual from which the sample was collected|Only applies to human samples|||
|Sample|treatment category|recommended|Treatments that the sample might have undergone after collection|`ontology field` - e.g. OBI, NCIt or OGMS|||
|Sample|cell type|recommended|The cell type(s) known or selected to be present in the sample|`ontology field` - e.g. CL|source name|cell type|
|Sample|growth conditions|recommended|Features relating to the growth and/or maintenance of the sample||||
|Sample|genetic variation|recommended|Any relevant genetic differences from the specimen or sample to the expected genomic information for this species, eg abnormal chromosome counts, major translocations or indels||||
|Sample|sample collection technique|recommended|The technique used to collect the specimen, eg blood draw or surgical resection|`ontology field` - e.g. EFO or OBI|||
|Sample|phenotype|recommended|Any relevant (usually abnormal) phenotypes of the specimen or sample ||`ontology field` - e.g. HP or MP; species dependent|||
|Sample|cell cycle|recommended|The cell cycle phase of the sample (for synchronized growing cells or a single-cell sample), if known|`ontology field` - e.g. GO|||
|Sample|cell location|recommended|The cell location from which genetic material was collected (usually either nucleus or mitochondria)|`ontology field` - e.g. GO|||
