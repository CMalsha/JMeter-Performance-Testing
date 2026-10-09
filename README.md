# JMeter Web Performance Testing

## Project Overview

This project demonstrates beginner-level web performance testing using Apache JMeter on the LambdaTest E-Commerce Playground website.

The objective is to practise sending HTTP requests, measuring response times, checking response errors, and comparing test results under different load settings.

**Website under test:** https://ecommerce-playground.lambdatest.io/

## Tools Used

- Apache JMeter
- HTTP Request Sampler
- Thread Group
- Response Assertion
- Summary Report
- Aggregate Report
- CSV test reports
- Git and GitHub

## Test Scenarios

The test plan includes HTTP requests intended to cover:

1. Opening the e-commerce website
2. Opening the home page
3. Sending a search-page request
4. Opening a product page
5. Opening the cart page
6. Opening the checkout page

Each configured request uses a response assertion to check for the expected HTTP status code of `200`.

**Note:** These are HTTP request checks, not full end-to-end browser interactions. Search, cart, and checkout requests may not reproduce the complete user journey or update cart state.

## Test Configurations

### Baseline Test

- Virtual users: 10
- Ramp-up period: 10 seconds
- Loop count: 2

### Load Test

- Virtual users: 20
- Ramp-up period: 20 seconds
- Loop count: 1

The configurations were used to practise comparing response times, throughput, and error rates. They are learning tests, not a production capacity assessment.

## Results

### Baseline Test

- Total samples: 120
- Average response time: approximately 2,175 ms
- Maximum response time: approximately 9,687 ms
- Error rate: 0%
- Throughput: approximately 3.3 requests/second

### Load Test — Summary Report

- Total samples: 120
- Average response time: approximately 2,278 ms
- Maximum response time: approximately 7,215 ms
- Error rate: 0%
- Throughput: approximately 3.56 requests/second

### Aggregate Report — 20-User Run

- Average response time: 9,125 ms
- 90% line: 23,590 ms
- 95% line: 35,120 ms
- 99% line: 38,384 ms
- Error rate: 0%
- Throughput: approximately 1.6 requests/second

The Aggregate Report values differ from the earlier Summary Report results. These results should be treated as separate test runs unless the saved reports confirm otherwise. Response times can vary due to network conditions, server load, and test execution conditions.

## Key Learnings

- Configuring Thread Groups, HTTP Request samplers, and Response Assertions
- Measuring average, minimum, and maximum response times
- Understanding throughput and error percentage
- Using percentile metrics to identify slower responses
- Saving JMeter reports as CSV files
- Comparing test runs and documenting findings
- Version-controlling test plans and results with GitHub

## How to Run the Test

1. Install Apache JMeter.
2. Clone or download this repository.
3. Open `E-Commerce_Web_Performance_Test.jmx` in JMeter.
4. Review the Thread Group settings and HTTP request URLs.
5. Select a listener such as Summary Report or Aggregate Report.
6. Run a small test and review the results.

Run tests against public websites responsibly. This project is for learning and does not establish the website's production capacity or service-level performance.

## Project Status

Beginner web performance testing practice project. Future improvements may include clearer test scenarios, repeatable test runs, and documented performance comparisons.
