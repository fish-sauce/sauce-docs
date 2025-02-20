---
id: failure-analysis
title: Analyzing Failure Patterns Across Your Test Suite
sidebar_label: Failure Analysis
description: Use the machine learning power of Sauce Failure Analytics to uncover errors and inefficiencies in your tests to improve your testing process.
---

import useBaseUrl from '@docusaurus/useBaseUrl';

Failure Analysis is designed to help you optimize test efficiency and efficacy. The proprietary machine learning algorithms review the test pass/fail data to unearth common failures and their impact on the test suite as a whole. It then presents a report with tabs that aggregate patterns that are predictive of failure, helping you avoid similar or duplicate failures in future tests. Using Failure Analysis:

- Improves developer efficiency, streamlining detection and triage of the most pervasive errors
- Validates investment in test automation by showing larger patterns as a source of failure, allowing for global mitigation and faster time-to-market with better quality

:::note
Failure Analysis supports Cypress, Playwright, Selenium and Appium. Additionally, in case of Selenium and Appium, it can only be effective if your tests are configured to [report a pass/fail outcome](/basics/test-config-annotation/test-annotation#setting-passfail).
:::

## How it Works

Failure Analysis leverages your test data and identifies potential failure patterns based on aggregate test errors. More specifically, the tool:

- Identifies failed tests
- Aggregates failures on test names
- Detects common failure patterns
- Ranks and prioritizes patterns by most pervasive impact

For example, the image below shows a failed build where each test contains a bad, or outdated, web element locator. Failure Analysis detects any failure patterns and attributes a percentage to show how pervasive this failure is within this particular build.

<img src={useBaseUrl('img/insights/fa-tests.png')} alt="Failed Tests View" width="650" margin-bottom="50px"/>

To see the specifics of each failure pattern, go to **Insights > Failure Analysis**, or select **Failure Patterns** when viewing data about your build. As you can see in the next image, a pattern of failures due to invalid element locators has emerged that is impacting 25% of the tests in the build.

<img src={useBaseUrl('img/insights/fa-tests.png')} alt="Failed Tests View" width="650"/>

<!--
Incorporate from FAQs

* Filter by build
* Rename Failure Patterns
* Results last 30 days
* No test exclusion
-->

You can optimize the power of the Failure Analysis tool by [Providing Context for Selenium Commands with the JavaScript Executor](/basics/test-config-annotation/test-annotation#selenium-javascript-executor).
