# Repair Data

I took data from the website of the [Open Repair Alliance](https://openrepair.org/open-data/downloads/). The structure of the data follows the technical documentation of the [Open Repair Data Standard](https://standard.openrepair.org/) (ORDS Version 0.21). 

> The initial objective of the Open Repair Alliance is to help organizations involved in community repair to harmonize the way we collect and share information about successes and challenges in repairing small electrical and consumer electronic devices, to increase the visibility and the impact of the work we all do.


The value of the last column of the following table (`R data types`) is set by me according to the `Type` description in the [documentation of the Open Repair Data Standard](https://standard.openrepair.org/standard.html#field-reference) (ORDS Version 0.21).

| Title               | Field name                    | Type                                                                                                            | R Data Type |
|---------------------|-------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------|
| ID                  | id                            | Unique identifier from the partner organisation. Does not have to be unique across all partner data.            | character   |
| Partner category    | partner_product_category      | Option from partner codelist.                                                                                   | character   |
| Product category    | product_category              | Option from ORDS *product category codelist*.                                                                   | factor      |
| Brand               | brand                         | Free text.                                                                                                      | character   |
| Year of manufacture | year_of_manufacture           | Year. YYYY.                                                                                                     | character*  |
| Problem             | problem                       | Free text. Personal data should be removed, e.g. email addresses.                                              | character   |
| Repair status       | repair_status                 | Option from ORDS *repair status codelist*.                                                                      | factor      |
| Repair barrier      | repair_barrier_if_end_of_life | Option from ORDS *repair barrier codelist*. Optional. Only relevant where repair_status = "End of life".        | factor      |
| Group identifier    | group_identifier              | String. Unique. A unique identifier across all partners that can identify the group responsible for the repair. | factor      |
| Event date          | event_date                    | Date. YYYY-MM-DD format. The date of the repair event that the repair took place at.                            | Date        |
| Data provider       | data_provider                 | Option from ORDS codelist. Name of partner organisation.                                                        | factor      |
| Country             | country                       | String. 3 letter ISO code, e.g. ???GBR???.                                                                          | factor      |
| Record date         | record_date                   | Date. YYYY-MM-DD format. The date that the record was last updated.                                             | Date        |

* Because of many NA's written as "????" I chose to import this column as "character".  
