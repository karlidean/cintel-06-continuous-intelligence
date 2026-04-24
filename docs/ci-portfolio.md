# Continuous Intelligence Portfolio

Karli Dean

2026-04

This page summarizes my work on **continuous intelligence** projects.

## 1. Professional Project

### [Repository Link](https://github.com/karlidean/cintel-01-getting-started)

### Brief Overview of Project Tools and Choices
This project uses professional Python tooling (uv, src layout, linting, and documentation systems) to simulate a real continuous intelligence workflow. The shift from pipeline_case to pipeline_karlidean represents moving from running a provided template to owning and customizing a repeatable pipeline structure. In this project, I had changed the success message, as this was mainly a definition of the main function. There were not many ideas to change.

## 2. Anomaly Detection

### [Repository Link](https://github.com/karlidean/cintel-02-static-anomalies)

### Techniques
Anomalies are detected by creating derived signals (like rates and averages) and comparing them against predefined thresholds. Any values that fall outside acceptable ranges are flagged as anomalies using conditional logic, allowing the system to classify abnormal behavior.

### [Artifacts](https://github.com/karlidean/cintel-02-static-anomalies/tree/main/artifacts)
The artifacts returned multiple results, all detailing those who were over the age of 35 AND over the height of 66 inches. The example had shown a way to have a maximum value to exceed, which I altered to relay all people within a taller and older demographic.

### Insights
The analysis revealed a slew of records back to me, but I took it as a way that data works on sites like Tinder or Hinge. When you purchase a membership through these sites, you get the opportunity to filter people by your interests in a partner. Being able to do this lowers your demographic of people in your area (or people you're subjecting to an analysis). It is likely that sites like this use data filtering code like this to obtain greater results or more matches on their site.

## 3. Signal Design

### [Repository Link](https://github.com/karlidean/cintel-03-signal-design)

### Signals
In this repo, I created a latency alert signal because just looking at latency as a number isn’t useful on its own. I wanted to turn it into a decision-making signal that clearly shows when performance crosses a threshold and becomes a problem.

### [Artifacts](https://github.com/karlidean/cintel-03-signal-design/tree/main/artifacts)
In this repo, the result file adds a binary alert field that turns latency into a clear yes/no signal. Instead of just showing a number, it flags whether performance has crossed a threshold, making it much easier to interpret and act on. In my personalized script, this is outlined to be "1" if the threshold is crossed, and "0" if it is not.

### Insights
This reveals when latency actually becomes a problem, not just when it changes. It makes it easy to see patterns in performance issues and quickly understand whether the system is stable or starting to struggle.

## 5. Drift Detection

### [Repository Link](https://github.com/karlidean/cintel-05-drift-detection)

### Techniques
The script compares reference (baseline) data to current data by calculating the same signals for each and measuring the difference between them, flagging drift when that difference exceeds a defined threshold.\
\
In this script, I split the data into a baseline (reference) and a current set, then compared their signals to see if the system behavior changed. If the difference between them crosses a threshold, it flags drift—basically telling me “this isn’t behaving like it used to.”

### [Artifacts](https://github.com/karlidean/cintel-05-drift-detection/tree/main/artifacts)

In this repo, the drift summary file breaks out each signal and compares what it used to look like vs. what it looks like now. It shows the difference and adds a drift flag, so I can quickly see not just what changed, but what changed enough to actually matter.

### Insights

This summary shows that key signals have shifted between the reference and current datasets, with current values deviating from their baseline levels. We know these changes are meaningful because the differences exceed defined thresholds and are flagged as drift. This helps drive actionable decisions by identifying exactly which parts of the system require investigation, allowing for targeted responses such as performance optimization or system adjustments.

## 6. Continuous Intelligence Pipeline

### [Repository Link](https://github.com/karlidean/cintel-06-continuous-intelligence)

### Techniques

In this repo, I combined signal design and monitoring techniques by turning raw volleyball stats into performance signals, then using thresholds to evaluate each player’s attacking efficiency. The script calculates attack error rate, attempts per kill, and attack success rate, then groups the data by player to summarize total attempts, errors, kills, and average performance signals. This allows the system to classify each player as a strong or weak attacker, making the monitoring output easier to interpret and use for decision-making.

### [Artifacts](https://github.com/karlidean/cintel-06-continuous-intelligence/tree/main/artifacts)

This file is basically the “final answer” of the pipeline—it takes all the signals and turns them into a clear label for each player. Instead of digging through stats, you can instantly see who’s performing well and who needs work, which makes it super easy to actually make decisions.

### Assessment
The pipeline is answering the question of whether players are converting attacks efficiently. If too many players are flagged as weaker attackers, the team’s offense becomes less effective, which can negatively impact overall performance and win outcomes. Conversely, having more strong attackers increases the likelihood of offensive success.\
\
Because this analysis spans 13 seasons, the pipeline also provides insight into long-term trends. When aggregated at the team level, the results suggest that UMSL has frequently exhibited lower attacking efficiency, indicating a pattern of weaker offensive performance over time.
