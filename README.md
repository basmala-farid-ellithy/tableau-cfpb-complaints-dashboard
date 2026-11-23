# US Consumer Complaints | Tableau Dashboard

[Open the native interactive Tableau Public dashboard](https://public.tableau.com/app/profile/basmala.farid.ellithy/viz/USConsumerComplaints-CFPBPublicDataDemo/Dashboard1#1)

Built and published in Tableau Public web authoring. Portfolio demonstration using US public data, not employment or client work.

## Dashboard
- Monthly complaint volume, November 2025 through October 2026.
- Timely response rate, calculated as `SUM([Timely Yes]) / (SUM([Timely Yes]) + SUM([Timely No]))`.
- Product complaint totals across the full 12-month period, sorted by volume.
- Hover tooltips for values and full product names.

The two aggregate data sources remain separate. Product totals are not joined to monthly rows and there is no date filter pretending to filter the full-period product data.

## Data and method
Source: [CFPB Consumer Complaint Database](https://www.consumerfinance.gov/data-research/consumer-complaints/). Retrieved November 23, 2026. The retrieval script requests zero complaint-level records and retains only server-side aggregate counts. Inclusive first and last dates define each month.

Monthly totals reconcile to product totals: **7,256,133 complaints**. No narratives, personal records, company-level records or granular location are included.

Timely response excludes unknown status from its denominator. It does not mean the complaint was resolved to the consumer's satisfaction. Complaint volume is not market share, product quality or a representative consumer survey. Historical counts may change when the source is updated.

The downloadable supporting-data ZIP in this repository contains the CSV aggregates, source retrieval script, aggregate evidence and Tableau build notes. The native dashboard is hosted on Tableau Public at the link above.

## Related project
[Power BI-ready model, DAX and Power Query](https://github.com/basmala-farid-ellithy/powerbi-cfpb-complaints), clearly labeled as an import-ready package rather than a native PBIX report.
