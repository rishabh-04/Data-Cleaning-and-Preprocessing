# Netflix Dataset Cleaning

This project cleans and standardizes the Netflix Dataset(`netflix_titles.csv`) using Python (Pandas) in Jupyter Notebook.

1. **Import Dataset**
   Loaded the original dataset into Pandas for processing.

2. **Handle Missing Values**

   * Replaced all `NaN` values with `"nil"` for consistency.

3. **Remove Duplicates**

   * Dropped all duplicate rows to keep only unique records.

4. **Standardize Text Values**

   * Trimmed extra spaces.
   * Converted text columns to consistent casing:

     * Proper nouns (e.g., *title*, *country*, *director*) → **Title Case**
     * Categories (e.g., *type*, *rating*, *listed\_in*) → **Title Case**
     * Special: `show_id` → **Uppercase** (e.g., `S1`, `S2`)
     * `duration` → **First Letter Capitalized** (e.g., `90 Minutes`, `2 Seasons`)

5. **Fix Specific Columns**

   * Standardized `country` names (e.g., *Usa* → *United States*).
   * Corrected `gender` values if present (e.g., *m* → *male*).

6. **Date Formatting**

   * Converted `date_added` to **datetime** type.
   * Saved/exported dates in `dd-mm-yyyy` format.

7. **Rename Column Headers**

   * Converted all column names to **lowercase** and replaced spaces with **underscores**.

8. **Check and Fix Data Types**

   * Ensured numeric columns are integers where applicable.
   * Kept `date_added` as `datetime64[ns]`.

## **Output**

* Cleaned dataset saved as **`netflix_titles_cleaned.ipynb`**.
* Ready for analysis, visualization, or machine learning.


