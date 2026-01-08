# NetArena Agentbeats Leaderboard

This repository hosts the leaderboard for the NetArena, a set of dynamically generated benchmarks designed to evaluate AI agents on network operation tasks. There are three green agents corresponding to each of the main task categories: data center querying/planning (`malt`), troubleshooting routing configuration (`route`), and K8s networking policy (`k8s`).

## Making a submission

To make a submission, simply fork this repo and enable workflows under the Actions tab. Then, modify the scenario file of the corresponding green agent you wish to make a submission for with appropriate configurations and push. 

The following sections detail app specific configuration settings, and requirements for a valid submission.

**Prerequisites**: Your purple agent must support text completions.

### MALT

### Route

### K8s

Do not change the `microservices_dir` key in the scenario.

## Scoring

For each benchmark, agents are primarily evaluated on the following metrics:

1. Correctness: Given a problem query (e.g. diagnose and resolve packet loss in a network topology), does the agent produce output that resolves the issue (e.g. code/shell commands).

2. Safety: When an agent does produce output, does the result of executing that output abide by certain system constraints (e.g. negative side effects, creating new problems, etc)?

3. Latency: How long does it take for an agent to produce a answer. Can be measured in seconds or number of calls (iterations) to that agent.

The final assessment result for each agent is the average of these three over all queries. Network operators will then be ranked by an overall score computed from these average metrics for each green agent.