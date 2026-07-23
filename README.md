# DATA6550-Reproducibility-Summer2026
## Team Members:
- Jay Beladiya
- Tirth Laheri

## Paper being reproduced

**Detection of COVID-19 epidemic outbreak using machine learning**
Giphil Cho, Jeong Rye Park, Yongin Choi, Hyeonjeong Ahn, Hyojung Lee
*Frontiers in Public Health*, 11:1252357, published 18 December 2023.
DOI: [10.3389/fpubh.2023.1252357](https://doi.org/10.3389/fpubh.2023.1252357) — Open access (CC BY)

- Paper (Frontiers): https://www.frontiersin.org/journals/public-health/articles/10.3389/fpubh.2023.1252357/full
- Paper (PMC free full text): https://pmc.ncbi.nlm.nih.gov/articles/PMC10764024/
- Original code + data repository: https://github.com/modeling-computation/covid-19_outbreak

**Summary:** The authors build a "risk index" from South Korean public epidemiological data, then train
three classical ML models (SVM, Random Forest, XGBoost) to classify COVID-19 transmission trend into
three labels (decreasing / maintaining / increasing), using grid search for hyperparameter tuning. They
report >94% classification accuracy and use the trend classification to detect outbreak start times
(7 estimated vs. 5 officially reported outbreaks in Korea, March 2020–October 2022). A secondary result
is a sensitivity analysis varying the outbreak "duration of maintenance" parameter from 7 to 28 days.

## Data availability

The `data/` folder in the original repository already contains the files needed to run the *training*
and *figure* steps directly (`train.csv`, `test.csv`, `time_line.xlsx`, and — via `temp/` — the full
case series), so this reproduction does not need to pull fresh data from the Korea Public Data Portal or
KDCA for those steps.
- Korea Public Data Portal: https://www.data.go.kr/data/15106451/fileData.do
- KDCA (Korea Disease Control and Prevention Agency): https://ncov.kdca.go.kr/en/tcmBoardList.do?brdId=12&brdGubun=125&dataGubun=&ncvContSeq=&contSeq=&board_id=&gubun
