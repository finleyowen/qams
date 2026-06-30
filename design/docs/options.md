# QAMS CLI Options

The following options should be stored as JSON inside of each QAMS instance (visible to users, who can change it at any time).

- `path_to_reviews`: path to the directory where past reviews are stored (default = `./reviews`)
- `path_to_reports`: path to the directory where past reports are stored (default = `./reports`)
- `accumulation_period`: the number of previous reports on which the next report should be based (assuming availability).