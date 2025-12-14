
# Drone Surveillance and Police Response Simulation

## Description

This NetLogo model simulates a **drone-based surveillance system** operating over an urban area divided into zones. Drones patrol assigned zones, detect suspects, and communicate with police officers who respond and make arrests. The model also includes pedestrians and a small probability of **false positive detections**.

The purpose of the simulation is to study how autonomous drones, human responders, and random events interact in a multi-agent environment.

---

## Agents

### Drones

* Patrol fixed zones
* Detect nearby suspects
* Communicate with other drones in the same zone
* Alert police when a suspect is detected
* Have limited energy and may fail randomly
* Backup drones replace failed main drones

### Police Officers

* Fixed number of agents
* Respond to alerts from drones
* Move toward reported targets
* Arrest real suspects
* Release pedestrians in case of false positives

### Suspects

* Move randomly
* Can be arrested and removed from the simulation

### Pedestrians

* Innocent agents moving randomly
* May be falsely detected with very low probability

---

## Environment

* The world is divided into a grid of **zones**
* Each drone is permanently assigned to one zone
* Drones are not allowed to leave their assigned zone

---

## Model Behavior

* Drones patrol their zones and search for suspects
* When a suspect is detected, the nearest police officer is alerted
* Police move to the target and make an arrest
* A very small probability of false detection causes police to investigate pedestrians
* Drones consume energy, recharge during daytime, and can fail and recover

---

## Metrics and Outputs

The model records:

* Total number of arrests
* Total number of false positives
* Number of active and failed drones
* Average drone energy level

A plot shows **arrests versus false positives over time**.

---

## Parameters

* `detection-radius`: Range of drone detection
* `failure-rate`: Probability of drone failure
* `false-positive-rate`: Probability of false detection
* `suspect-spawn-rate`: Rate of new suspect appearance
* `max-suspects`: Maximum number of suspects in the system

---

## How to Run

1. Click **Setup**
2. Click **Go**
3. Observe drone patrols, police responses, and plots

---

## Purpose

This model demonstrates:

* Multi-agent coordination
* Autonomous surveillance behavior
* Effects of false positives
* Resource management and system reliability

---

