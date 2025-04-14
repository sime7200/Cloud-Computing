# ☁️ Cloud Computing Project – Power Measurement on Chameleon Cloud

This repository documents the final project for the *Cloud Computing* course, focused on measuring the **energy consumption** of virtual machines deployed on the **Chameleon Cloud** using **Scaphandre**, **Prometheus**, and **Grafana**.

The project demonstrates how to monitor real-time power usage of **bare-metal instances**, visualize energy metrics, and configure a lightweight monitoring pipeline using open-source tools.

---

## 📚 Course Context

The project was developed within the context of the following topics:

- Introduction to Cloud Computing principles
- Hands-on labs on **Google Cloud Platform**, **Amazon Web Services**, and **OpenStack**
- Practical experience with **Chameleon Cloud**, a research-oriented cloud testbed

---

## 🛠️ Tools & Technologies

- **Chameleon Cloud (CHI @ TACC)** – OpenStack-based IaaS for research
- **Scaphandre** – Lightweight energy metrics exporter for Linux systems
- **Prometheus** – Open-source monitoring and alerting toolkit
- **Grafana** – Dashboard and visualization platform
- **Ubuntu 20.04** – Base OS image used on all instances
- **Bare-metal instances** – Required to access power consumption data via RAPL

---

## 📈 Project Overview

The goal of the project is to measure and visualize the **power consumption** of bare-metal cloud instances using a monitoring stack composed of:

1. **Scaphandre** running on secondary instances to export power metrics
2. **Prometheus** running on a main instance to scrape those metrics
3. **Grafana** installed on the main instance for data visualization

Key features include:
- Metric exposure via HTTP (`8080` port)
- Prometheus configuration for multi-source metric scraping
- Grafana dashboard provisioning for intuitive energy monitoring

---

## 🔧 Setup Summary

### 🔹 Step-by-step guide includes:
- Creating and configuring **leases** and **instances** on Chameleon
- Installing dependencies and monitoring tools via `apt` and `cargo`
- Configuring **firewall rules** to expose Prometheus and allow internal access
- Creating **Grafana dashboards** using official templates
