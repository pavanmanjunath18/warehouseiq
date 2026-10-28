# WarehouseIQ

![status](https://img.shields.io/badge/status-building-orange)

Warehouse operations analytics in Power BI and DAX, built on simulated WMS, timekeeping, and order data.

**Stack:** Power BI, DAX, PostgreSQL, SQL, Python

> **Status: Building.** Launching soon.

## Highlights

- Simulated warehouse data from three systems (WMS pick events, timekeeping punches, orders and shipments) loaded into PostgreSQL
- SQL views that clean and join the three systems into analysis-ready tables
- Data-quality checks (missing scans, duplicate picks, timekeeping gaps, and more) that write to a results table
- Power BI star-schema model with documented DAX measures: units per labor hour, on-time-in-full, dock-to-stock time, overtime %, cost per order
- Time intelligence (month-to-date, year-over-year, rolling windows)
- Multi-page report covering throughput, labor, fulfillment, and data quality
- Concept notes on star schema, DAX filter context, and time intelligence

Benchmarks will be published here once measured.

## Layout

```
data_gen/   Python generator for the simulated warehouse data and PostgreSQL loader
sql/        schema, cleaning and join views, data-quality checks
powerbi/    Power BI model and report, DAX measure documentation
bench/      scripts that write measured results to bench/results/*.json
docs/       concept notes (star schema, filter context, time intelligence)
```

## Roadmap

- [ ] Phase 1: stack decision
- [ ] Week 1: data generator, PostgreSQL load, cleaning views, data-quality checks
- [ ] Week 2: star-schema model, DAX measures, report pages, benchmarks
- [ ] Docs: interview-ready concept notes

## License

MIT
