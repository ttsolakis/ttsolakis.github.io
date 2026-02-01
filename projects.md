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
  .gallery figure { flex-basis: calc(50% - 10px); max-width: calc(50% - 10px); }
}
@media (max-width: 520px) {
  .gallery figure { flex-basis: 100%; max-width: 100%; }
}
</style>

Here’s a selection of my projects, ordered from most recent to earlier work.  
They span from hands-on robotics builds to research in control and autonomy.

<p style="max-width: 150ch; margin: 0 auto; text-align: center;">
👉 Learn more <a href="/aboutme">about me</a>.
</p>

---

## nav_mpc (Home Project)  
**Nonlinear MPC · OSQP · Embedded Control · Python · ROS2**  

A personal research project to design a **real-time nonlinear MPC framework** for autonomous navigation, with a strong focus on computational efficiency, modularity, and embedded deployment.

- Symbolic definition of nonlinear MPC problems (dynamics, constraints, objectives).
- Automatic reformulation into an LTV-QP with Cython-accelerated evaluation.
- Real-time QP solution using OSQP, guaranteeing control-loop feasibility.
- Integrated simulator with plotting and animation for fast prototyping.
- Designed with embedded and robotic applications in mind (UGVs, UAVs, USVs).

Current status:
- End-to-end examples working (simple pendulum, double pendulum, rover).
- Collision avoidance constraints under active development.
- Intended as the planner backbone for the **Autonomous Rover** and **FLARE** projects.

**Repository:** [nav_mpc](https://github.com/ttsolakis/nav_mpc)

<div class="gallery">
  <figure>
    <img src="/assets/img/mpc_01.gif " alt="Simple pendulum swing-up and stabilization">
    <figcaption>Simple pendulum swing-up and stabilization (avg control cycle: 1.29 ms) </figcaption>
  </figure>
  <figure>
    <img src="/assets/img/mpc_02.gif" alt="Double pendulum swing-up and stabilization">
    <figcaption>Double pendulum swing-up and stabilization (avg control cycle: 1.45 ms) </figcaption>
  </figure>
  <figure>
    <img src="/assets/img/mpc_03.gif" alt="Simple rover set-point tracking">
    <figcaption>Simple rover set-point tracking (avg control cycle: 4.24 ms) </figcaption>
  </figure>
  <figure>
    <img src="/assets/img/mpc_04.gif" alt="Global path and path following">
    <figcaption>Simple rover path following with half-space corridor constraints (avg control cycle: 6.21 ms) </figcaption>
  </figure>
  <figure>
    <img src="/assets/img/nav_mpc_ros.gif" alt="ROS2-wrapper for nav_mpc with RVIZ visualization.">
    <figcaption>ROS2-wrapper for nav_mpc with RVIZ visualization. </figcaption>
  </figure>
</div>

---

## Autonomous Rover (Home Project)  
**Rover · Raspberry Pi 5 · LiDAR · IMU · Odometry · ROS2**  

A personal project to build a 4-wheel differential rover with full onboard autonomy.  

- SLAM and perception on one Raspberry Pi (pi-slam) using LiDAR–IMU–odom data.  
- Motion planning and control on a second Raspberry Pi (pi-plan).  
- Hands-on experience in hardware/software integration with ROS2 while experimenting with autonomous navigation.  
- Status: hardware assembled, custom 3D-printed case designed for component mounting, communication between modules set.

**Repository:** [rover_odom](https://github.com/ttsolakis/rover_odom)

<div class="gallery">
  <figure>
    <img src="/assets/img/rover_01.jpeg" alt="Rover hardware build-up">
    <figcaption>Rover hardware build-up</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/rover_02.gif" alt="Rover first pi-plan/ESP32 chat">
    <figcaption>Rover first pi-plan/ESP32 chat</figcaption>
  </figure>
  <!-- <figure>
    <img src="/assets/img/rover_03.gif" alt="Rover remote control play">
    <figcaption>Rover remote control play</figcaption>
  </figure> -->
  <figure>
    <img src="/assets/img/rover_04.gif" alt="Rover SLAM WIP">
    <figcaption>Rover SLAM WIP</figcaption>
  </figure>
</div>

---

## Wildfire Monitoring and Detection (FLARE)  
**UAVs · Solar Power · Environmental Monitoring · Fire Detection**  

Research project to develop **FLARE (Fire-Line Aerial Reconnaissance and Early Warning)**, a solar-powered, long-endurance UAV system for continuous monitoring and early wildfire detection.  

- Designed a wildfire simulator based on cellular automata and GeoTIFF vegetation maps.  
- Conducted payload study and initial airframe sizing for >24 h endurance.  
- Conceptual design of solar-powered autonomous glider with thermal/RGB payloads.  
- Planned autonomy stack: distributed multi-UAV persistent monitoring, robust path-following and control, and integrated avionics.  
- Status: simulator completed, sizing underway.

**Repositories:** [wildfire_surveillance](https://github.com/ttsolakis/wildfire_surveillance) [fire_simulator](https://github.com/ttsolakis/fire_simulator)
 
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
**MPC · Set-Membership Estimation (SME) · Reconfigurable Control · COLREGs**  

PhD research on safe and reliable motion planning for Autonomous Surface Vessels (ASVs).  

- Developed **MPC-based planners** integrating vessel dynamics, navigation objectives, and obstacle avoidance.  
- Embedded **COLREGs maritime traffic rules** via finite-state machines combined with MPC for rule compliance.  
- Designed an **SME-based framework for online fault detection and diagnosis**.  
- Proposed **reconfigurable and robust MPC planners** to ensure safety under actuator faults and environmental disturbances.  
- Validated in **ROS-based simulations** with dynamic obstacles.
- 📄 View my <a href="/assets/data/Tsolakis-PhD-Thesis.pdf" target="_blank">Thesis</a>
  
<div class="gallery">
  <figure>
    <img src="/assets/img/cor_01.gif" alt="Approach overview">
    <figcaption>Approach overview</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/cor_02.gif" alt="MPC for navigation">
    <figcaption>MPC for navigation</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/cor_03.gif" alt="Rule-compliance integration">
    <figcaption>Rule-compliance integration</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/cor_04.gif" alt="Uncertainties and faults">
    <figcaption>Uncertainties and faults</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/cor_05.gif" alt="Fault diagnosis with SME">
    <figcaption>Fault diagnosis with SME</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/cor_06.gif" alt="MPC reconfiguration and robustness to disturbances">
    <figcaption>MPC reconfiguration and robustness</figcaption>
  </figure>
</div>

---

## Distributed IDA-PBC for Nonholonomic Mechanical Systems  
**Passivity-Based Control · Distributed Control · Multi-Agent Systems**  

MSc thesis extending **distributed IDA-PBC** to a broad class of **nonholonomic** mechanical systems (e.g., differential robots), demonstrating cooperative control with heterogeneous teams.  

- Developed port-Hamiltonian modeling with IDA-PBC and adapted **Passive Configuration Decomposition (PCD)**.  
- Proposed a **novel non-smooth desired potential** enabling sequential stabilization on the constrained manifold.  
- Designed a **unified distributed control law** handling heterogeneous, underactuated, and nonholonomic agents.  
- Integrated **Artificial Potential Fields (APF)** for dynamic inter-agent collision avoidance.  
- Demonstrated faster convergence vs. prior PBSC baseline and successful distributed consensus in mixed-agent simulations.
- 📄 View my <a href="/assets/data/Tsolakis-Master-Thesis.pdf" target="_blank">Thesis</a>  

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
    <img src="/assets/img/idapbc_03.gif" alt="Trajectory comparison: proposed vs PBSC">
    <figcaption>Proposed vs. PBSC</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/idapbc_04.png" alt="State traces comparing proposed controller with PBSC">
    <figcaption>State comparison with PBSC</figcaption>
  </figure>
</div>

---

## Vehicle Dynamics & Torque Vectoring  
**Vehicle Dynamics · Control Systems · Multi-Body Dynamics · Simulation**  

Bachelor thesis on the effect of power distribution architectures and torque vectoring on vehicle dynamics.  

- Built detailed multi-body vehicle models in **Altair MotionView**.  
- Compared FWD, RWD, and AWD architectures.  
- Designed a **sliding-mode controller** in Python for active-AWD torque vectoring.  
- Demonstrated improved stability and cornering response vs. passive architectures.
- 📄 View my <a href="/assets/data/Tsolakis-Diploma-Thesis.pdf" target="_blank">Thesis</a>

<div class="gallery">
  <figure>
    <img src="/assets/img/auth_01.png" alt="Vehicle model setup in MBD environment">
    <figcaption>Multi-body dynamics vehicle model</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/auth_02.png" alt="Comparison across passive architectures and with torque vectoring">
    <figcaption>Passive vs. torque vectoring</figcaption>
  </figure>
</div>

---

## Formula Student Race Car (Team Project)  
**Mechanical Design · CAD/CAE · Assembly · Teamwork**  

Member of the **Aristotle Racing Team**, contributing to the design and build of a Formula Student race car that competed in three international events with top-10 placements.  

- Led the design, structural analysis, and manufacturing of the tubular steel frame.  
- Coordinated subsystem integration and supported vehicle assembly and testing.  
- Achieved successful participation in 3 international competitions.  

<div class="gallery">
  <figure>
    <img src="/assets/img/art_01.png" alt="Tubular frame CAD">
    <figcaption>Frame CAD design</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/art_02.jpg" alt="Frame welding during manufacturing">
    <figcaption>Frame welding</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/art_03.jpg" alt="Grinding process during frame manufacturing">
    <figcaption>Frame grinding</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/art_04.gif" alt="Vehicle testing session">
    <figcaption>Vehicle testing</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/art_05.gif" alt="Autocross session in Italy">
    <figcaption>Autocross competition</figcaption>
  </figure>
  <figure>
    <img src="/assets/img/art_06.png" alt="Aristotle Racing Team in Italy">
    <figcaption>Team in Italy</figcaption>
  </figure>
</div>
