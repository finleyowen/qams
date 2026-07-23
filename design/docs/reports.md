# QAMS Reports

A QAMS report aggregates over multiple reviews for multiple agents on the same scorecard. Each QAMS report also contains information about previous reports on the same scorecard. For a given agent, a given report might contain zero, one, or many reviews for that agent.

To generate a QAMS report, a **reporting period** (start date, end date; both inclusive) and an **accumulation period** (number of reporting periods) needs to be supplied. The reporting period determines which reviews should be included in the current report, while the accumulation period determines how many previous reports should be used to compute the current report. 

Each scorecard is associated with a default reporting period duration. By default, the reporting period starts the day after the previous reporting period ends, and the end date is calculated from the start date and the default reporting period duration for that scorecard. By default, the accumulation period is be the number of previous reports available.

A QAMS report consists of the following:

- **An Overall Summary View**: Presented as a table with criterion names in the rows and previous/current reports in the columns, the overall summary view shows the performance of all agents on each criteria in each review, as a percentage of the maximum number of points available (using the `Criterion::get_avg_score` method).

- **An Agent-Report Index**: Presented as a table with agent names in the rows and previous/current reports in the columns, the agent-report index shows the average score of each agent for each report, over all criteria and all reviews.

- **Individual agent views**: For each agent, the individual agent view presents all information about all reviews in the current reporting period, including the selections made and comments left.