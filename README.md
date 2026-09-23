# JMeter Performance Testing

Performance testing was performed using **Apache JMeter** as part of the QA automation assessment.

## Test Configuration

* **Tool:** Apache JMeter
* **API:** ReqRes
* **Method:** POST
* **Endpoint:** `/api/users`
* **Virtual Users:** 10
* **Ramp-up:** 10 seconds
* **Loop Count:** 5
* **Total Requests:** 50

## Metrics

The test captures:

* Response Time
* Throughput
* Minimum/Maximum Response Time
* Error Percentage

## Test Plan

The JMeter test plan is available here:

```text
performance/OrangeHRM_API_Performance.jmx
```

Open the `.jmx` file using Apache JMeter and click **Run** to execute the test.

## Note

During execution, the ReqRes API returned a `rate_limit_exceeded` response after the anonymous API limit of **40 requests/day per IP** was reached. This is an external API limitation and not a JMeter configuration error.
