INVEST AI Historical Price Loader v1
Objective
Load and maintain historical price data for all assets.

Data Source Priority
Yahoo Finance
Stooq
Initial Load
Start Date: 2018-01-01

End Date: Current Date

Incremental Updates
Start Date: Last stored trading date

End Date: Current Date

Required Fields
Asset Prices Table
asset_id
trading_date
open_price
high_price
low_price
close_price
adjusted_close
volume
Data Validation
Date
Must not be null.

Close Price
Must be > 0.

High Price
Must be >= Low Price.

Volume
Must be >= 0.

Missing Trading Days
Allowed.

Reason: Weekends and market holidays.

Duplicate Rules
One record per:

asset_id + trading_date

No duplicates allowed.

Error Handling
If data retrieval fails:

Log error
Do not overwrite previous prices
Update Log
Every execution must register:

start date
end date
rows imported
execution status
in data_update_log

Future Phases
Phase 2: Technical Indicators Generation

Phase 3: Score Calculation

Phase 4: Scanner Execution

Phase 5: Opportunities Generation
