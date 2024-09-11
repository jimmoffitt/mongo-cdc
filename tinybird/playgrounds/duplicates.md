
# Duplicates

## total_duplicates

```sql
SELECT SUM(duplicate_count) as total_duplicates
FROM (
    SELECT timestamp, site_name, COUNT(*) -1 as duplicate_count 
    FROM mongo_weather_reports
    GROUP BY timestamp, site_name
    HAVING COUNT(*) > 1
) AS subquery
```

## unique_reports

```sql
SELECT COUNT(DISTINCT site_name, timestamp) AS distinct_report_count
FROM mongo_weather_reports
```
## where_are_duplicates_coming_from

```sql
SELECT toStartOfMonth(timestamp) AS month, site_name, COUNT(*) AS num_duplicates
FROM mongo_weather_reports
GROUP BY month,site_name
ORDER BY num_duplicates DESC
```

## including_all_duplicates_for_city

```sql
SELECT timestamp, site_name, temp_f
FROM mongo_weather_reports
WHERE site_name = 'Fullerton'
ORDER BY timestamp DESC
```
