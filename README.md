# Data Job Market Analysis

An exploratory analysis of 2023 data job postings using Python and pandas. The project compares requested skills, remote-work share, and represented countries across Data Analyst, Senior Data Analyst, Data Scientist, and Senior Data Scientist roles.

## Questions

- Which skills appear most often in each role?
- How do skill requirements differ between analyst and scientist roles?
- What share of postings are marked as remote?
- Which countries are most represented in the analyzed sample?

## Dataset

[Luke Barousse’s data jobs dataset](https://huggingface.co/datasets/lukebarousse/data_jobs), a collection of job postings from 2023. The original dataset contains about 785,000 rows and 17 columns.

## Tools and methods

- Python, pandas, matplotlib, and Hugging Face Datasets
- Removed exact duplicate rows
- Selected four analyst and scientist job-title categories
- Kept postings with skill information and parsed the skill lists
- Counted each skill once per posting and calculated the percentage of postings mentioning it
- Compared remote-work and country counts using the same skill-bearing subset

## Findings

The notebook’s previous exploratory run found:

- **Data Analyst:** SQL, Excel, and Python were the most frequently listed skills.
- **Data Scientist:** Python, SQL, and R were the most frequently listed skills.
- **Remote work:** The remote share ranged from 7.2% to 11.0% across the four roles; Senior Data Scientist postings had the highest share.
- **Location:** The United States was the most represented country for each role in this sample.

The percentages above came from the saved run before exact duplicate rows were removed. The notebook has since been updated to remove duplicates and its old outputs were cleared. Run all notebook cells to generate the final figures, then update this section if the results change.

## Limitations

This is a historical 2023 snapshot, not a view of the current job market. The results describe postings in this dataset and are not a ranking of all job opportunities. Remote-work and country comparisons use only postings with non-empty skill information.

## Run the notebook

Open [job analysis.ipynb](job%20analysis.ipynb) in Google Colab and choose **Runtime → Run all**. The notebook downloads the dataset, cleans duplicates, and regenerates the tables and charts.
