# Energy Systems

This section documents applied energy management and automation work within the
Open Physics Lab.  
The focus lies on real-world energy systems, their measurement, control, and
integration into larger technical environments.

Much of the work in this area is developed together with students as part of
teaching, engineering projects, and long-term experimental studies.

---

## Scope

This area covers practical energy systems and their interaction with physical,
electrical, and computational infrastructure.

Topics include building-level energy management, thermal systems, electrical
distribution, and integration with automation platforms.

---

## Core Areas of Interest

- heating control and thermal regulation  
- building automation and KNX integration  
- solar power generation and monitoring  
- electrical energy distribution and measurement  
- charging infrastructure and load management  

---

## Implementation Model

Energy-related projects in the Open Physics Lab combine domain-specific
engineering with shared control and automation methods.

Most energy systems are implemented primarily at the automation layer using
Node-RED (orchestration, data handling, dashboards, integration).  
Only the heating control includes an additional low-level embedded controller.

- **Heating control**  
  Embedded controller (Portenta H7, C++) + automation & UI (Node-RED)

- **KNX integration, solar monitoring, power measurement, charging systems**  
  Implemented primarily at the automation layer (Node-RED)

Control strategies, feedback logic, and automation patterns used here are
documented in the cross-cutting **Control & Automation** section
(`control/README.md`).


## Experimental & Engineering Directions

Current and planned work includes:

- development of networked heating controllers  
- integration of KNX-based building systems  
- monitoring and optimization of solar power production  
- charging station management and energy balancing  
- data-driven analysis of consumption patterns  

Related implementations and system designs are documented in the corresponding
project repositories referenced in **[PROJECTS.md](../PROJECTS.md)**.


## Implementations

The heating control system is split into two coordinated components:
a low-level embedded controller (Portenta H7, C++) and a higher-level automation
and user interface layer (Node-RED, deployed on RPi and Proxmox).

Control and automation patterns used across domains are documented in
`control/README.md`.

Related repositories:
- Heating Controller (Portenta H7, C++, MQTT): https://github.com/steffsplace/HeatingController_MQTT
- Automation / UI (Node-RED): https://github.com/steffsplace/HeatingController_NodeRED

---

## Methodological Principles

- system-level modeling and verification  
- reproducible engineering practices  
- careful instrumentation and logging  
- long-term operational observation  

---

## Open Questions

This section evolves continuously as systems are deployed, observed, and refined.

---

## References

Technical documentation, standards, and design notes are collected alongside
each concrete project and linked from the project index.
