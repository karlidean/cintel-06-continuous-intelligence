# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)

## Custom Project

### Dataset
The dataset is something I've been compiling myself for future data analysis and is a history of all UMSL volleyball statistics since 2013. It is pulled directly from the UMSL volleyball website.

### Signals
I created volleyball-specific signals to evaluate player performance in attacking using a continuous intelligence approach. Attack Attempts (TA) were treated as volume, or requests, Attack Errors (TA) were treated as failures. I calculated the attack error rate from the values to evaluate how often players make mistakes. I also created attempts_per_kill as a latency metric, representing how many tries it takes a player to score. I also used my success rate function to provide more of a positive measure of the player.

### Experiments
My modifications and experiments included modifying the original pipeline to be able to work with volleyball data. I replaced system metrics and experimenting with different signal definitions, deciding attempts per kill was the most meaningful latency measurement for a scouting report. I also adjusted threshold values to become more realistic to this type of performance, setting the max error rate to 0.2 and the latency to 4.0. I also changed the logic to group by player, allowing the system to evaluate each player individually, instead of summarizing the dataset as a whole.

### Results
The updated pipeline produced one aggregated record per player, summarizing their attacking efficiency. Players were then classified as stronger or weaker attackers based on their error rate or attempts latency exceeded thresholds. The results highlighted clear differences in player efficiency, with some players maintaining low error rates and efficient scoring, others showing higher inefficiency through increased errors or more attempts to score.

### Interpretation
This analysis provides an efficient, data driven way to evaluate offensive performance in volleyball. Players defined as a strong attacker were demonstrating high efficiency, low errors, and consistency in their play styles. This makes them more reliable and more likely to receive the ball during the game. This type of analysis can support coaching decisions, player development, and lineup optimization.
