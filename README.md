<div align="center">
  <h1>DevicePropagation</h1>
  <p><strong>Discrete-event simulation of alerts and cancellations across connected devices.</strong></p>
  <p>
    <img alt="Python" src="https://img.shields.io/badge/Python-303840?style=flat-square" />
    <img alt="Simulation" src="https://img.shields.io/badge/Simulation-303840?style=flat-square" />
  </p>
  <p><a href="#overview">Overview</a> · <a href="#getting-started">Getting started</a> · <a href="#repository-map">Repository map</a></p>
</div>

---

## Overview

A command-line simulation of messages traveling between devices with configured propagation delays. Alerts and cancellations are expanded into a chronological event trace.

## What’s inside

- Parse device definitions, propagation links, alerts, cancellations, and an end time.
- Calculate sent and received events across device links.
- Print timestamped events followed by the simulation end marker.

## Getting started

Use Python 3.10 or newer:

```sh
python propagation_run.py
```

Enter the path to an input file on standard input. The parser recognizes `LENGTH`, `DEVICE`, `PROPAGATE`, `ALERT`, and `CANCEL` records. Input files are not bundled; see `create_lists.py` for the exact field layout.

## Repository map

| Location | Purpose |
| --- | --- |
| [`propagation_run.py`](./propagation_run.py) | CLI and chronological output |
| [`create_lists.py`](./create_lists.py) | Input parsing |
| [`prepare.py`](./prepare.py) | Propagation and cancellation processing |

## Project status

Educational simulation. No third-party packages are required. Validate custom graph and cancellation cases before relying on the output for other applications.
