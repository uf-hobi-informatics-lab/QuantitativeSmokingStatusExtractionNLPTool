# QuantitativeSmokingStatusExtractionNLPTool
A rule-base NLP system to extract quantitative smoking information (e.g., pack-year) from clinical notes

## Aim
The package is used for extraction of quantitative smoking information from clinical notes.

## Smoking information type
- pack per day
- smoking year
- quit year (e.g., quit for 10 years)
- year at quit (e.g., quit at 2008)
- pack-year

## Requirement
- java 1.8

## Input format
For input, we expect a CSV file with encoding as UTF-8. The data table should have no header (only real data in table) and 5 columns as
1. note ID
2. patient ID
3. note Date
4. note Type
5. note text
(You can use dummy text for 1-4)

## Output format
The output is a TSV with encoding as UTF-8.
1. note ID
2. patient ID
3. note Date
4. note Type
5. extracted data type
6. extracted data value
7. a snippet of where the extracted value located in text (50 characters before and after the value)
(1-4 is copied from input data)

## How to run
1. change to the project directory
2. run java -jar RuleBaseSmokingInfoExtraction.jar <input file location> <output file1 location> <log location> <rule set name> or use the run.sh (modify arguments necessary)

## Example
- we provide sample.csv for testing, see run.sh

## Note
- this is a rule-based system
- we are keeping update rules to cover special cases

## Release
- we released the RuleBaseSmokingInfoExtraction.jar
- we will release source code

## Citation
```
Yang X, Yang H, Lyu T, Yang S, Guo Y, Bian J, Xu H, Wu Y. 
A Natural Language Processing Tool to Extract Quantitative Smoking Status from Clinical Narratives.
2020 IEEE International Conference on Healthcare Informatics (ICHI), 2020, pp. 1-2. 
doi: 10.1109/ICHI48887.2020.9374369.
PMID: 33173920; PMCID: PMC7654916.

https://ieeexplore.ieee.org/abstract/document/9374369
```