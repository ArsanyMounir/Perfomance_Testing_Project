# ITI Performance Testing Project

This project contains performance testing tasks using **Apache JMeter**.

## 📌 Project Overview

The performance project consists of three main tasks:

### Question I: Scripting

#### 1. UI Scenario
A complete user journey simulated on the PetStore application:
- Navigate to homepage
- Register a new account
- Browse products
- Add item to cart
- Complete checkout
- Assert that the order confirmation page is reached

#### 2. API Scenario
Tests the full lifecycle of a booking on [Restful-Booker](https://restful-booker.herokuapp.com):
- Authenticate
- Create a booking
- Retrieve all bookings
- Update booking with ID=1
- Delete booking with ID=1

##### Script Features:
- Proper parameterization using CSV data (`Test_Data.csv`)
- Text-based assertions for response validation
- HTTP Request Defaults for environment independence
- Constant timers for realistic delays
- Cache and Cookie managers for reliable test iterations

### 📈 Question II: Running and Analyzing

- A **Thread Group** simulates 2 users for 10 minutes
- Results visualized using an **Aggregate Report**
- Final report (`Report.pdf`) includes:
  - Screenshot of the Aggregate Report
  - SLA validation table with colored indicators:
    - SLA 1: Total error percentage ≤ 10%
    - SLA 2: 90% of requests ≤ 3 seconds
    - SLA 3: 99% of requests ≤ 5 seconds

### 🔁 Question III: Load Profiling

Configured a **jp@gc - Stepping Thread Group** plugin to simulate the following load:
- Ramp-up: 100 users at 1 user/sec
- Ramp-down: Exit at 1 user/sec

## 📁 Project Files

| File/Folder         | Description |
|---------------------|-------------|
| `jmeter/JMeter_Assignment.jmx` | JMeter test plan file |
| `jmeter/Test_Data.csv`         | CSV file with test data |
| `jmeter/Report.pdf`            | Analysis and SLA validation report |
| `screenshots/aggregate_report_screenshot.png` | Aggregate report screenshot |

## 🛠 Tools & Tech Used
- Apache JMeter
- CSV Data Config
- Regex & JSON Extractors
- Stepping Thread Group Plugin
- Assertions, Timers, and Config Elements

## 📋 How to Run
1. Open `JMeter_Assignment.jmx` in JMeter.
2. Ensure the `Test_Data.csv` is placed in the correct directory.
3. Run the test with 2 users for 10 minutes.
4. Use `Aggregate Report` listener to view results.
5. For load profiling, use the `jp@gc - Stepping Thread Group`.


---

> **Note:** Please use only the specified number of users to avoid blacklisting from test servers.
