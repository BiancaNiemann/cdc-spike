# CDC Change Producer Script 
## What is this?
This Python script allows you to **produce changes in your PostgreSQL database** to trigger CDC (Change Data Capture) events.

### What it does:
- Provides an **interactive menu** to perform operations on the database
- Supports INSERT, UPDATE, DELETE operations for `users` and `orders` tables
- Performs **bulk operations** for testing multiple CDC events at once
- Shows **current data** in the database with tables using Rich

### Why it matters:
- Generates CDC events that Debezium captures and streams to Kafka
- Helps test your CDC pipeline without manually modifying the database
- Demonstrates how changes propagate to Kafka topics

### How to run:
```bash
python produce_changes.py
```

### Next steps:
1. Run this script to make changes in your database
2. Observe messages in Kafka via `consume_kafka.py`
3. Optionally, verify downstream effects in Elasticsearch if using a sink connector

This script is beginner-friendly and perfect for experimenting with CDC event streams.

