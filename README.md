# GloBox Mastery Project (A/B Testing) by Masterschool
###### Updated on July 24th, 2023.
# Metadata
* A/B test user (test subject) onboarding data, activity data and personal data for a fictitious e-commerce platform called GloBox, provided by Masterschool. Project introduction can be found [here](https://cms.master.school/sprint-overview-extract-the-ab-test-data).
* [ISO 3166 country codes](https://www.iso.org/obp/ui/#search).

# Background
* Author is a candidate in the [Masterschool's](https://www.masterschool.com/) Data Analytics program (January 2023 intake).
* This project is a mastery project, and the first one of such for the author's cohort (of candidates).
* A mastery project is significant. It is a graded project by Masterschool to evidence a candidate's job-readiness to prospective employers, and for the candidate to graduate from the program.  

## 1. Project description
 * Plan, organize and run A/B test on a new banner that highlights the food and drink products of GloBox, a fictitious e-commerce platform.

## 2. Submission & Feedback
 * First and only submission was made on July 6, 2023. The [submission pack](https://github.com/coderedstorage/globox/blob/f41a12aab900ea02881c509247a6d3f0f95e4f22/Submission_AB_testing_project_AK.zip) includes:
    * [A/B testing report](https://github.com/coderedstorage/globox/blob/main/GloBox%20AB%20Testing%20Report%20-%20AK.pdf).
    * [2-page presentation](https://github.com/coderedstorage/globox/blob/main/GloBox%20AB%20Testing%20Presentation%20-%20AK.pdf).
 * The author received direct feedback for his first submission on his Masterschool Campus account on July 23rd, 2023 (ahead of the project's final submission date August 5th, 2023).
 * The author received A+, the highest grade possible and will de-facto graduate from the program. Thus there is no further requirement to re-submit the project. 

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
 * Generate visualizations from workbook [GloBox v4.twbx](https://github.com/coderedstorage/globox/blob/main/GloBox%20v4.twbx) 
 * Data committed to Tableau saved on [globox_tableau_commits.zip](https://github.com/coderedstorage/globox/blob/main/globox_tableau_commits.zip).
    *  ab_boxplots.csv.
    *  ab_lifecycle.csv.
    *  ab_test_final.csv.
    *  test_result.csv.
