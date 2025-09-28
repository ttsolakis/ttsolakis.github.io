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
**UAVs · Solar Power · Autonomy · Fire Detection**  
Concept for a solar-powered, long-endurance UAV system for early wildfire detection and continuous monitoring.  
- Vision: persistent aerial coverage with thermal/RGB cameras and onboard autonomy.  
- Current status: developing a Python-based wildfire simulator to study fire spread and detection strategies.  
- Next steps: platform and payload sizing, and integration of the autonomy stack.

<!-- <div class="gallery">
  <figure>
    <img src="/assets/img/flare_sim_01.gif" alt="Wildfire cellular automata simulation">
    <figcaption>Fire spread sim</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/flare_uav_01.jpg" alt="Solar UAV concept render">
    <figcaption>Solar UAV concept</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/flare_coverage_01.png" alt="Coverage planning heatmap">
    <figcaption>Coverage planning</figcaption>
  </figure>
</div> -->

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
    <img src="/assets/img/asv_rules_01.gif" alt="ASV trajectory with COLREGs compliance">
    <figcaption>Rule-compliant paths</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/asv_fault_01.gif" alt="Fault-tolerant control under actuator loss">
    <figcaption>Fault-tolerant MPC</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/asv_sim_01.png" alt="Simulation setup with dynamic obstacles">
    <figcaption>ROS-based sim</figcaption>
  </figure>
</div> -->

---

## Distributed IDA-PBC for Nonholonomic Mechanical Systems
**Passivity-Based Control · Multi-Agent Systems · MATLAB**  
MSc thesis: Designed a distributed Interconnection & Damping Assignment – Passivity-Based Control (IDA-PBC) algorithm for heterogeneous mechanical systems (mobile robots and manipulators).

<!-- <div class="gallery">
  <figure>
    <img src="/assets/img/idapbc_01.gif" alt="Formation control via IDA-PBC">
    <figcaption>Formation control</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/idapbc_02.png" alt="Block diagram of interconnections">
    <figcaption>Interconnection diagram</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/idapbc_03.gif" alt="Tracking performance plot">
    <figcaption>Tracking performance</figcaption>
  </figure>
</div> -->

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
