# covid-einstein-fapesp
Preprocessed data from 2,982 de-identified COVID-19 patients, provided by the Albert Einstein hospital, in Sao Paulo, Brazil.

## Data
This COVID-19 dataset was built from originally unlabeled data collected from COVID-19 patients of the Israelite Albert Einstein Hospital, located in Sao Paulo, Brazil. The original database comprises a total of 1,853,695 results from 127 different medical tests, collected from 43,562 de-identified patients, who received treatment in the hospital from January 1, 2020 until June 24, 2020.

For this version, firstly, we identify the patients who tested positive in at least one of the following COVID-19 detection tests: 
- polymerase chain reaction (PCR), 
- immunoglobulin M (IgM), 
- immunoglobulin G (IgG) and 
- enzyme-linked immunosorbent assay (ELISA). 

Next, we filter the patients and left in the dataset only the ones who have made at least one complete blood count (CBC) test, in a date no earlier than the date to be tested positive for COVID-19. In case a patient has made more than one CBC test, we then consider only the results of the first test. Afterwards, we run an algorithm to automatically label each patient of the dataset as presenting or not signs from each type of insufficiency (hepatic, renal and respiratory), strictly according to results from the specific tests listed below, and using their respective reference values provided in the same original database, which are standardized in the medical literature.

After the data cleansing, we end up with a total of 2,982 different patients in the dataset, with each of them presenting a class label regarding whether he or she presented signs of Hepatic Insufficiency, Renal Insufficiency and Respiratory Insufficiency (1 = With Signs, 0 = Without Signs, for each label).

#### Tests considered for detecting signs of insufficiency in patients
Hepatic: 
- transaminase TGO (AST)
- transaminase TGP (ALT)
- alkaline phosphatase
- gamma-glutamyl transpeptidase (GGT)

Renal: 
- creatinine clearance (urine test)
- creatinine (blood test)
- blood urea nitrogen (BUN) 

Respiratory: 
- arterial blood gas
- respiratory pathogen panel
- lactate
- ionized calcium
- potassium

### Columns:
* id_paciente: patient's unique number	
* ic_sexo:	0=Female, 1=Male
* idade: patient's age
* idade_faixa: 0 = age < 20, 1 = 20 <= age < 40, 2 = 40 <= age < 60, 3 = 60 <= age < 80, 4 = age >= 80 
* Neutrófilos #:  neutrophils
* CHCM: Mean Corpuscular Hemoglobin Concentration	
* Eosinófilos #: eosinophils
* Hematócrito: hematocrit
* Hemoglobina: hemoglobin
* Basófilos #: basophils
* VCM: Mean corpuscular volume
* Neutrófilos: neutrophils (%)
* Volume Médio Plaquetário:	Average Platelet Volume
* Linfócitos: Lymphocytes (%)	
* Basófilos: basophils (%)	
* Hemácias: Red Cells	
* HCM: Medium Corpuscular Hemoglobin	
* Plaquetas: Platelets
* Leucócitos: leukocytes (%)	
* Monócitos #: monocytes
* Monócitos: monocytes (%)	
* Linfócitos #: Lymphocytes 	
* Eosinófilos: eosinophils (%)	
* RDW: Red Cell Distribution Width	
* Leucócitos #: leukocytes	
* dt_hemo: CBC tests date	
* respiratoria: presents signs of respiratory insufficiency (0 = No, 1 = Yes)	
* dt_respiratoria: date when respiratory insufficiency tests were made
* hepatica: presents signs of hepatic insufficiency (0 = No, 1 = Yes)	
* dt_hepatica: date when respiratory insufficiency tests were made	
* renal: presents signs of renal insufficiency (0 = No, 1 = Yes)		
* dt_renal: date when renal insufficiency tests were made		
* all: presents signs of all three types of insufficiency (0 = No, 1 = Yes)			
* any: presents signs of any type of insufficiency (0 = No, 1 = Yes)		


## Source
Dados COVID Hospital Israelita Albert Einstein: https://repositoriodatasharingfapesp.uspdigital.usp.br/handle/item/98

## Citation
If this material was useful in your research, please kindly cite the following article:

Colliri, T., Minakawa, M., & Zhao, L. (2021, November). Detecting Early Signs of Insufficiency in COVID-19 Patients from CBC Tests Through a Supervised Learning Approach. In Brazilian Conference on Intelligent Systems (pp. 42-57). Springer, Cham.

https://link.springer.com/chapter/10.1007/978-3-030-91699-2_4
