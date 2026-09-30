# AI Use and Independent Verification Log

## AI assistance
- Tool: ChatGPT
- Tasks: 
  - Interpreted the DS-A1 assignment requirements.
  - Suggested a reproducible project structure.
  - Helped draft the initial audit notebook structure.
  - Helped explain provenance, duplicate handling, and claim boundaries.

## Accepted suggestions
- Use a frozen local CSV dataset with a SHA-256 hash for reproducibility.
- Perform explicit checks for:
  - schema consistency
  - missing values
  - duplicate rows
  - numerical ranges
  - anomalies
  - possible data leakage
  - Separate descriptive claims from causal claims.

## Rejected or modified suggestions

- AI-generated explanations were reviewed and adjusted to match my own understanding.
- I did not accept any results without checking the notebook outputs myself.


## Independent verification performed by student

After opening and running the notebook in Jupyter Notebook, I personally verified:

- The notebook executed successfully.
- The dataset loaded correctly from the local frozen CSV file.
- The dataset contained 150 rows and 5 columns.
- Missing value checks returned zero missing values.
- The duplicate audit identified one exact duplicate row.
- Class counts were checked and confirmed as:
  - setosa: 50
  - versicolor: 50
  - virginica: 50

The final notebook outputs and report were reviewed before submission.