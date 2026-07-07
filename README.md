# CloudSchedX: Automated Security and Privacy Enforcement Framework for Cloud Resource Allocation

CloudSchedX is a CloudSim-based project for studying cloud resource allocation, scheduling, and policy-driven control in simulated cloud environments. The project focuses on how tasks are assigned to virtual machines and how virtual machines process those tasks, with the broader goal of supporting security- and privacy-aware resource allocation decisions.

This repository contains the CloudSim source code used for the project, example workloads and simulations, and the project report that describes the problem statement, design, and evaluation in more detail.

## Project Report

The main report for this project is available in [docs/ProjectReport.pdf](docs/ProjectReport.pdf). A short companion note about the scheduling context used by the project is available in [docs/ABOUT.md](docs/ABOUT.md).

## Background

In CloudSim, scheduling happens at two levels:

1. Global scheduling is handled by the broker. It decides which cloudlet is assigned to which VM.
2. Local scheduling is handled by the VM. It decides how CPU time is shared among the cloudlets already assigned to that VM.

This distinction is important for CloudSchedX because the project evaluates resource allocation policies from both a system-level and an execution-level perspective.

## Repository Layout

- `cloudsim/` - CloudSim source and example modules
- `docs/` - Project report and supporting notes
- `README.md` - Project overview and setup entry point

## Prerequisites

- Java 21
- Maven

## Build

From the `cloudsim/` directory, run:

```bash
mvn clean install
```

This builds the CloudSim modules and runs the test suite.

## Run an Example

After building, you can run a CloudSim example from the examples module. For example:

```bash
mvn exec:java -pl modules/cloudsim-examples/ -Dexec.mainClass=org.cloudbus.cloudsim.examples.CloudSimExample1
```

## Next Steps

This README is an initial draft. The next update should add the project-specific architecture, experiment workflow, and the main security and privacy policies implemented by CloudSchedX.
