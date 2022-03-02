# QuantitativeSmokingStatusExtractionNLPTool
A rule-base NLP system to extract quantitative smoking information (e.g., pack-year) from clinical notes

## Aim
The package is used for extraction of quantitative smoking information from clinical notes.

## smoking information type
- pack per day
- smoking year
- quit year (e.g., quit for 10 years)
- year at quit (e.g., quit at 2008)
- pack-year

## requirment
- java 1.8

## Input format
For input, we expect a CSV file with a encoding as UTF-8. The data table should have no header (only real data in table) and 5 columns as
1. note ID
2. patient ID
3. note Date
4. note Type
5. note text
(You can use dummy text for 1-4)

## output format
The output is a TSV with encoding as UTF-8.
1. note ID
2. patient ID
3. note Date
4. note Type
5. extracted data type
6. extracted data value
7. a snippet of where the extracted value located in text (50 characters before and after the value)
(1-4 is copied from input data)

## how to run
1. change to the project directory
2. run java -jar RuleBaseSmokingInfoExtraction.jar <input file location> <output file1 location> <log location> <rule set name> or use the run.sh (modify arguments necessary)

## example (you can test system using the sample_idr.csv)
you can run java -jar RuleBaseSmokingInfoExtraction.jar sample_idr.csv sample_output1.tsv log.txt smoke

## note
- this is a rule-based system
- we are keeping update rules to cover special cases

## release
- we released the RuleBaseSmokingInfoExtraction.jar
- we will release source code

## citation
```
X. Yang et al., "A Natural Language Processing Tool to Extract Quantitative Smoking Status from Clinical Narratives," 2020 IEEE International Conference on Healthcare Informatics (ICHI), 2020, pp. 1-2, doi: 10.1109/ICHI48887.2020.9374369.

https://ieeexplore.ieee.org/abstract/document/9374369
```