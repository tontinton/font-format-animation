# File Format Animation

Single-page (`index.html`) interactive visualization comparing Apache Parquet vs Lance file format I/O patterns.

## What it does

Animates two query types side-by-side on block-level file layout diagrams:

- **Random Read** (`SELECT col_b WHERE id = 100`) — point lookup via index
- **Sequential Scan** (`SELECT count(*) GROUP BY col_b`) — full column scan

Highlights which blocks are read, skipped, or seeked to, showing how Parquet's row-group interleaving causes random I/O on scans while Lance's contiguous column layout enables sequential reads.

## Tech

- Pure HTML/CSS/JS, no dependencies
- Step-based animation engine with play/pause/reset and speed control
