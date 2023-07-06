# A/B Testing Final Project - Masterschool

# Metadata
* Fictitious e-commerce platform A/B test user (test subject) onbording data, acitivity data and personal data (provided by Mastershcool).
* [ISO 3166 country codes](https://www.iso.org/obp/ui/#search).

## 1. Project description
 * Plan, organize and run A/B test on a new banner that highlights the food and drink products of a fictitious e-commerce platform called GloBox. 

## 2. Submission & Feedback
 * [A/B testing report](https://github.com/coderedstorage/globox/blob/main/GloBox%20AB%20Testing%20Report%20-%20AK.pdf).
 * [2-page presentation](https://github.com/coderedstorage/globox/blob/main/GloBox%20AB%20Testing%20Presentation%20-%20AK.pdf).

## 3. Tools and resources
### MySQL
 * Raw inputs imported as tables (see [globox_raw_inputs.zip](https://github.com/coderedstorage/globox/blob/main/globox_raw_inputs.zip)).
    * activity.csv imported into table abglobox.activity
    * groups.csv imported into table abglobox.groups
    * iso_3166_country_code.csv imported into table abglobox.iso_codes
    * users.csv imported into table abglobox.users
 * MySQL scripts to create views and outputs (see [globox_sql.zip](https://github.com/coderedstorage/globox/blob/main/globox_sql.zip)).
    *  abglobox.ab_test_final.sql to join data from tables above into view abglobox.ab_test_final.
        *  Output into ab_test_final.csv.
    *  abglobox.ab_lifecycle.sql to generate view abglobox.ab_lifecycle (from view abglobox.ab_test_final).
        *  Output into ab_lifecycle.csv.
    *  abglobox.ab_boxplots.sql to generate view abglobox.ab_boxplots (from view abglobox.ab_test_final).
        *  Output into ab_boxplots.csv.
### Python
 * Python notebook used [AB_testkit.ipynb](https://github.com/coderedstorage/globox/blob/main/AB_testkit.ipynb).
    *  Generate test results from data drawn from ab_test_final.csv.
    *  Results saved in test_results.csv.
### Tableau
 * Generate visualizations from.
 * Data committed to Tableau saved on [globox_tableau_commits](https://github.com/coderedstorage/globox/blob/main/globox_tableau_commits.zip).
    *  ab_boxplots.csv.
    *  ab_lifecycle.csv.
    *  ab_test_final.csv.
    *  test_result.csv.
