# CDC Kafka Consumer & Event Inspector Script 

## What is this?
This Python script consumes **CDC (Change Data Capture) events** from Kafka and shows how they can be mapped to Elasticsearch.

### What it does:
- Connects to Kafka topics produced by the Debezium PostgreSQL connector
- Explains the structure of CDC events:
  - **Key** → Primary key / Elasticsearch _id
  - **Value** → Event envelope with `op`, `before`, `after`, `source` metadata
  - **Tombstones** → Messages with null value after DELETE
- Displays events interactively using Rich
- Indexes documents into Elasticsearch for CREATE/UPDATE events
- Deletes documents from Elasticsearch for DELETE events
- Provides statistics about consumed events
- Optionally exports sample events to a JSON file for documentation

### Why it matters:
- Helps you **understand Debezium CDC events**
- Shows how to **map changes to Elasticsearch**
- Useful for testing your CDC pipeline and ensuring data flows correctly

### How to run:
```bash
python consume_kafka.py
```

### Next steps:
1. Observe how INSERT, UPDATE, DELETE operations appear in Kafka
2. Verify documents in Elasticsearch if using the sink or manual indexing

This script is beginner-friendly and perfect for inspecting CDC events and understanding how data flows from Postgres → Kafka → Elasticsearch.