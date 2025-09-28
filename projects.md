---
layout: page
title: Projects
permalink: /projects/
---

<style>
/* simple, scoped gallery */
.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
  margin: 8px 0 18px;
}
.gallery figure {
  flex: 1 1 calc(33.333% - 10px); /* max 3 per row */
  max-width: calc(33.333% - 10px);
  margin: 0;
}
.gallery img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 6px;
}
.gallery figcaption {
  text-align: center;
  font-size: 0.85rem;
  color: #666;
  margin-top: 4px;
}
/* responsive breakpoints */
@media (max-width: 900px) {
  .gallery figure { flex-basis: calc(50% - 10px); max-width: calc(50% - 10px); } /* 2 per row */
}
@media (max-width: 520px) {
  .gallery figure { flex-basis: 100%; max-width: 100%; } /* 1 per row */
}
.badges span {
  display: inline-block;
  padding: 5px 10px;
  background-color: #f0f0f0;
  color: #007BFF;
  border-radius: 5px;
  font-size: 0.8em;
  margin: 5px 5px 0 0;
}
</style>

Here’s a selection of my projects, ordered from most recent to earlier work.  
They span from hands-on robotics builds to research in control and autonomy.

---

## Autonomous Rover (Home Project)
**Rover · Raspberry Pi 5 · LiDAR · IMU · Odometry · ROS2**  
A personal project to build a 4-wheel differential rover with full onboard autonomy.  
- SLAM and perception on one Raspberry Pi (pi-slam) using LiDAR–IMU–odom data.  
- Motion planning and control on a second Raspberry Pi (pi-plan).  
- Goal: hands-on experience in hardware/software integration with ROS2 while experimenting with autonomous navigation.
- Status: Hardware assembled, custom 3D-printed case designed for component mounting, communication between modules set.

<div class="gallery">
  <figure>
    <img src="/assets/img/rover_01.jpeg" alt="Rover hardware build-up">
    <figcaption>Rover hardware build-up</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/rover_02.gif" alt="Rover first pi-plan/ESP32 chat">
    <figcaption>Rover first pi-plan/ESP32 chat</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/rover_03.gif" alt="Rover remote control play">
    <figcaption>Rover remote control play</figcaption>
  </figure>
</div>

---

## Wildfire Monitoring and Detection (FLARE)  
**UAVs · Solar Power · Environmental Monitoring · Fire Detection**  
A research project to develop **FLARE (Fire-Line Aerial Reconnaissance and Early Warning)**, a solar-powered, long-endurance UAV system for continuous monitoring and early wildfire detection.  
- **Goal**: achieve >24 h endurance flights with onboard thermal/RGB cameras for persistent monitoring, early ignition detection, and fire-front tracking.  
- **Approach**: (i) payload study and initial sizing; (ii) solar-powered autonomous glider design; (iii) autonomy stack combining distributed persistent monitoring (multi-UAV), robust path-following and control, and integrated avionics.  
- **Status**: wildfire simulator based on cellular automata and GeoTIFF data completed; payload study and initial sizing underway.  

<div class="gallery">
  <figure>
    <img src="/assets/img/fire_01.png" alt="Wildfire GeoTIFF data">
    <figcaption>Wildfire GeoTIFF data</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/fire_02.gif" alt="Wildfire cellular automata simulation">
    <figcaption>Cellular automata simulation</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/fire_03.png" alt="Feasibility study and sizing results">
    <figcaption>Feasibility & sizing results</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/fire_04.png" alt="FLARE concept scheme">
    <figcaption>FLARE system concept</figcaption>
  </figure>
</div>


---

## Rule-Compliant & Fault-Tolerant Motion Planning for ASVs
**MPC · Set-Membership Estimation (SME) · Reconfigurable MPC · COLREGs**  
PhD research on safe and resilient planning for ASVs.  
- Integrated maritime traffic rules into finite-state machines and MPC for rule-compliant navigation.  
- Developed SME-based parameter estimation for online fault diagnosis.  
- Designed reconfigurable/robust MPC planners to maintain safety under actuator faults and disturbances.  
- Validated through ROS-based simulations with dynamic obstacles.

<!-- <div class="gallery">
  <figure>
    <img src="/assets/img/idapbc_01.gif" alt="Differential robots reach desired formation">
    <figcaption>Differential robots reach desired formation</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/asv_fault_01.gif" alt="Fault-tolerant control under actuator loss">
    <figcaption>Fault-tolerant MPC</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/asv_sim_01.png" alt="Simulation setup with dynamic obstacles">
    <figcaption>ROS-based sim</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/asv_sim_01.png" alt="Simulation setup with dynamic obstacles">
    <figcaption>ROS-based sim</figcaption>
  </figure>
</div> -->

---

## Distributed IDA-PBC for Nonholonomic Mechanical Systems  
**Passivity-Based Control · Multi-Agent Systems · MATLAB**  
MSc thesis extending **distributed IDA-PBC** to a broad class of **nonholonomic** mechanical systems (e.g., differential robots), demonstrating cooperative control with **heterogeneous** teams (mobile robots + manipulators).

- **Methodology**: port-Hamiltonian modeling with IDA-PBC; adaptation of **Passive Configuration Decomposition (PCD)** to the Hamiltonian setting; design of a **novel (non-smooth) desired potential** enabling sequential stabilization on the constrained manifold.
- **Unified control law**: handles **heterogeneous, underactuated, and nonholonomic** agents within one distributed framework; includes **kinetic/potential energy shaping**, gyroscopic/damping terms, and feasibility via matching conditions.
- **Collision avoidance**: integrated **Artificial Potential Fields (APF)** at low level for dynamic inter-agent avoidance within the constrained space.
- **Results**: smooth stabilization and **faster convergence** vs. prior PBSC baseline on a differential-drive robot; **distributed consensus** achieved in simulations with mixed agents (2 differential robots + 2 manipulators).

<div class="gallery">
  <figure>
    <img src="/assets/img/idapbc_01.gif" alt="Differential-drive robots forming target configuration">
    <figcaption>Formation with differential robots</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/idapbc_02.gif" alt="Coordinated motion: manipulators and differential robots">
    <figcaption>Heterogeneous coordination</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/idapbc_03.gif" alt="Trajectory comparison: proposed vs PBSC (animation)">
    <figcaption>Proposed vs. PBSC (animation)</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/idapbc_04.png" alt="State traces comparing proposed controller with PBSC">
    <figcaption>State comparison with PBSC</figcaption>
  </figure>
</div>

---

## Vehicle Dynamics & Torque Vectoring
**Control Systems · Vehicle Dynamics · Simulation**  
Studied power distribution architectures and designed a torque-vectoring controller with multibody dynamics models and sliding-mode control.

<!-- <div class="gallery">
  <figure>
    <img src="/assets/img/veh_dyn_01.png" alt="Vehicle model diagram">
    <figcaption>Vehicle model</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/veh_dyn_02.gif" alt="Torque vectoring comparison across architectures">
    <figcaption>TV comparison</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/veh_dyn_03.png" alt="Lateral dynamics response plot">
    <figcaption>Lateral response</figcaption>
  </figure>
</div> -->

---

## Formula Student Race Car (Team Project)
**Mechanical Design · CAD/CAE · Teamwork**  
Member of Aristotle Racing Team; led the tubular steel frame design, structural analysis, and manufacturing; coordinated subsystem integration and final assembly.

<!-- <div class="gallery">
  <figure>
    <img src="/assets/img/fs_01.jpg" alt="Tubular frame CAD">
    <figcaption>Frame CAD</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/fs_02.jpg" alt="Manufacturing process photo">
    <figcaption>Manufacturing</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/fs_03.jpg" alt="Car at competition">
    <figcaption>Competition</figcaption>
  </figure>
</div> -->
