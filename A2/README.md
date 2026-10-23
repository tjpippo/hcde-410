# A2 — Bias in Data

**Dataset:** Wikipedia Talk Corpus (Wikipedia Detox project): annotator demographics and toxicity-labelled comments
**Source:** https://figshare.com/projects/Wikipedia_Talk/16731 (documentation: https://meta.wikimedia.org/wiki/Research:Detox/Data_Release)
**License / terms of use:** The Wikipedia Talk datasets are released under a **CC0 public domain dedication**, so they can be used, modified, and shared freely. The original comments come from Wikipedia talk pages.

## About the data
The Wikipedia Talk Corpus contains comments from English Wikipedia talk pages (2001–2015), labelled by crowdworkers on CrowdFlower for toxicity, aggression, and personal attacks. It was used to train Google Jigsaw's Perspective API toxic-speech classifier. This analysis uses:
- `toxicity_worker_demographics.tsv`, `attack_worker_demographics.tsv`, `aggression_worker_demographics.tsv`: the gender, first language, age group, and education of the crowdworkers
- `toxicity_labelled_comments_3k_sample.csv`: a random sample of 3,000 toxicity labels with comment text

## What I did
1. **Data preparation:** loaded the three demographic files and found that the attack and aggression files are identical (undocumented duplicates). I also found that `worker_id` refers to different people across datasets, so I combined the toxicity and attack/aggression workers into one dataset (5,781 workers) with new unique IDs.
2. **Demographic analysis (Q1–Q6):** summarised workers by gender, first language, age, and education; checked for missing data; and measured how keeping the duplicate file would change the results.
3. **Bias reasoning (Q7–Q8, Q13–Q16, no-code option):** compared annotators to internet users overall, reviewed 60 labelled comments (20 toxic, 20 neutral, 20 non-toxic) for agreement with the labellers, critiqued the labelling instructions, and considered how these biases could affect the Perspective API.


## Files
- `A2.ipynb`: the analysis notebook, with code, outputs, and written answers
- `a2_all_annotator_demographics.csv`: the cleaned, combined annotator demographics exported from the notebook
- `wikipedia_datasets/`: the source data files
- `README.md`: this file
- `LICENSE`: MIT license for my code
- A2 toxicity comment review: my own pick of the comments

## How to re-run
Open `A2.ipynb` and run all cells. Needs Python 3 with `pandas` and `matplotlib`, and the data files in `wikipedia_datasets/`. 
## AI use
- I used claude code to help me code python from the data. I dropped the data in Claude and then ask claude to generate me a Phyton code that would give me the data to the specific topics I need.
- I use
