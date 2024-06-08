# Labor Condition Application(LCA) Analytics

JupyterLite Web assembly deployed as a static site to GitHub Pages.
- Reference: https://jupyterlite.readthedocs.io/en/latest/reference/index.html
- About LCA: https://flag.dol.gov/programs/LCA

## ✨ Try it in your browser ✨
https://forager365.github.io/julite/notebooks/index.html?path=data%2Flca-analytics.ipynb

https://forager365.github.io/julite/lab/index.html

## JPM Chase LCA applications for Q1 2024
https://forager365.github.io/

## Query using DuckDB

go to https://sql-workbench.com/
for Q1 JPMChase data
```
select * from read_csv_auto('https://forager365.github.io/lca.csv')
where case_status = 'Certified'
and worksite_state = 'OH'
```
LCA_Q1_Q2.parquet is the Q1 and Q2 dataset
```
select * from 'https://forager365.github.io/LCA_Q1_Q2.parquet'
where employer_name ilike 'JPM%'
and case_status = 'Certified'
and worksite_city = 'Houston'
and job_title like '%Lead%'
```





