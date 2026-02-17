# linux-systems-lab 
Linux Systems Lab
Overview

This repository documents hands-on lab work focused on Linux system administration, service management, process isolation, and security hardening.

The objective of this lab is to develop practical systems engineering skills through iterative experimentation, debugging, and deployment in controlled environments.

All work is performed in lab environments (local machines, VMs, and cloud instances) for educational and professional development purposes.

**Core Focus Areas**

Linux system fundamentals

Process management and daemons

systemd service creation and management

Log analysis using journalctl

User permissions and least-privilege configuration

Service hardening and isolation

Secure remote access and tunneling

Debugging production-like failures

**Lab Environment**

Operating Systems

Ubuntu Server (AWS EC2)

Debian-based Linux environments

Local Linux installations

Tools Used

Bash

Python 3

systemd

journalctl

SSH

tmux

Git

**Project Timeline**
Day 1 – Service Execution and Process Behavior

Created and executed Python scripts from terminal

Explored execution context differences

Learned importance of initialization and state control

Day 2 – Daemon Concepts and Background Execution

Built a basic long-running Python process

Explored loop-driven execution models

Practiced starting and stopping background services

Day 3 – systemd Service Deployment

Converted manual process into systemd-managed service

Created custom unit file

Implemented restricted user execution

Practiced service enable/disable workflows

Day 4 – Debugging and Log Analysis

Used journalctl to trace service failures

Diagnosed permission issues

Investigated environment variable scope problems

Implemented fixes and validated stability

Security Principles Practiced

Least privilege

Separation of execution context

Controlled service startup

Log auditing and monitoring

Principle of explicit configuration over implicit behavior

Example systemd Unit File
[Unit]
Description=Custom Agent Service
After=network.target

[Service]
User=agentuser
WorkingDirectory=/opt/agent
ExecStart=/usr/bin/python3 agent.py
Restart=always

[Install]
WantedBy=multi-user.target

Key Lessons

Variables must be initialized before execution.

State and time define system behavior.

Background processes require structured lifecycle control.

Service isolation improves stability and security.

Logging is the first line of debugging.

Future Improvements

Implement resource limits (CPU/memory constraints)

Add structured logging

Integrate health checks

Expand into zero-trust network modeling

Introduce containerization layer (Docker)

**Purpose**

This repository serves as a documented progression of Linux systems engineering skills with a security-first mindset. Future labs will extend into distributed systems, automation pipelines, and robotics infrastructure.
