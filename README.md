# Hadoop MapReduce: Small Files Optimization & Distributed Counters

> Implemented advanced Hadoop MapReduce workflows including custom WholeFileInputFormat, small-file optimization via SequenceFiles, and NOAA weather analysis using distributed job counters.

**Author:** Amisha Farhana Shaik  
**Project Type:** Big Data Engineering | Distributed Systems | Hadoop MapReduce  

---

## Project Overview

This project demonstrates advanced Hadoop MapReduce concepts executed on a distributed cluster.

The objectives were to:

- Solve the Hadoop small files problem
- Implement custom InputFormats
- Convert multiple small files into optimized SequenceFiles
- Create MapFiles with indexing
- Execute MapReduce jobs with custom counters
- Analyze NOAA weather data (year 1930) at scale

---

# Part 1: Small Files Optimization (Examples 7-2, 7-3, 7-4)

## Problem: Small Files in Hadoop

HDFS is optimized for large files.  
Too many small files cause:

- Excessive metadata overhead
- Increased NameNode memory usage
- Reduced performance

---

## Solution Implemented

### 1️⃣ Custom WholeFileInputFormat

Created and compiled:

- `WholeFileInputFormat`
- `WholeFileRecordReader`
- `SmallFilesToSequenceFileConverter`
- Nested Mapper class
- `JobBuilder`

These classes allow entire files to be read as single records.

---

### 2️⃣ Convert Small Files to SequenceFile

Workflow:

- Transfer Java files to cluster
- Compile against Hadoop libraries
- Package into JAR
- Run MapReduce job
- Generate optimized output directory

Result:
Multiple small files converted into a consolidated SequenceFile structure.

---

### 3️⃣ MapFile Structure Validation

Verified:

- Output directory structure
- Part files
- `_SUCCESS` marker
- Correct key-value aggregation

This demonstrated understanding of MapFile architecture (data + index).

---

## What This Demonstrates

- Custom InputFormat implementation
- Distributed file aggregation
- SequenceFile generation
- Efficient HDFS storage patterns
- MapReduce job configuration
- Reduce task tuning (`-D mapred.reduce.tasks=2`)

---

# Part 2: Max Temperature with Counters (Example 8-1)

## Objective

Analyze NOAA weather dataset (1930 data only) and compute maximum temperatures using MapReduce with custom counters.

---

## Dataset

- NOAA weather records (1930)
- Compressed `.gz` files
- Real historical climate data

---

## Classes Implemented

- `MaxTemperatureWithCounters`
- `MaxTemperatureMapperWithCounters`
- `MaxTemperatureReducer`
- `NcdcRecordParser`
- `JobBuilder`

Packaged into executable JAR.

---

## Custom Counters Implemented

Tracked:

- MISSING temperature values
- Temperature quality issues
- File input/output bytes
- Map & reduce task statistics
- Shuffle metrics

---

## Why Counters Matter

Counters enable:

- Debugging distributed jobs
- Monitoring data quality
- Tracking malformed records
- Evaluating job performance
- Observing cluster-level execution metrics

This bridges engineering and analytics.

---

## Key Technical Skills Demonstrated

- Custom Hadoop InputFormats
- SequenceFile optimization
- Small-file aggregation strategy
- MapReduce job packaging (multi-class JAR)
- Nested class handling
- Hadoop counters
- NOAA dataset parsing
- Distributed execution monitoring
- HDFS directory management
- Cluster-based debugging

---

## Advanced Concepts Covered

- File system metadata optimization
- Distributed sorting and aggregation
- Counter-based job instrumentation
- Performance-aware MapReduce design
- Real-world large-scale dataset processing

---

## Why This Project Is Important

This project demonstrates knowledge beyond basic Hadoop:

- Understanding of system-level inefficiencies
- Optimization of storage patterns
- Distributed performance monitoring
- Handling real-world structured weather data
- Engineering-grade MapReduce implementation

---

This project demonstrates applications in:

Big Data Engineering | Hadoop Optimization | Distributed Systems | Scalable Data Processing | Data Infrastructure Design
