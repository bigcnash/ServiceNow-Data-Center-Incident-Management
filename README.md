# 🖥️ ServiceNow Data Center Incident Management & Troubleshooting Lab

## 📋 Project Overview

In this project, I used ServiceNow to simulate how a Data Center Technician would handle a production server outage.

The goal was to work through an incident from start to finish — reviewing the ticket, identifying possible causes, troubleshooting the issue, documenting findings, and resolving the incident.

I wanted to demonstrate not only how to navigate ServiceNow, but also how I would approach troubleshooting an infrastructure issue in a real data center environment.

> **Lab Note:** This project uses a simulated server outage. Troubleshooting findings and corrective actions were documented in ServiceNow as part of the exercise. No physical server or network testing was performed.

---

## 🏢 Lab Environment

| Component | Details |
|-----------|---------|
| Platform | ServiceNow |
| Environment | Personal Developer Instance |
| Module | Incident Management |
| Incident | INC0010002 |
| Priority | P2 - High |
| Assignment Group | Datacenter Engineering |
| Assigned Technician | Christen Mitchell |
| Server | SRV-DC01-APP03 |
| Location | Data Center 01 - Rack B12 |
| Final Status | Resolved |

---

# 🚨 Incident Overview

A monitoring alert reported that production server SRV-DC01-APP03 was unreachable.

The server was located in Rack B12 of Data Center 01, and the outage was affecting application availability.

At this point, the cause was unknown.

The incident was categorized as Hardware and assigned a P2 - High priority based on its reported impact and urgency.

### Creating the Incident

I created the incident in ServiceNow, entered the affected server information, and documented the reported symptoms.

![Incident Creation](screenshots/01_Incident_Creation.png)

### Ticket Assignment

The ticket was routed to Datacenter Engineering and assigned to a technician for investigation.

![Incident Assignment](screenshots/02_Incident_Assignment.png)

---

# 🔧 Troubleshooting Process

## Step 1 — Identify the Problem

The first thing I needed to understand was what was actually happening.

The monitoring alert indicated that the server was unreachable, but that alone didn't tell me whether I was dealing with a hardware failure, network issue, or something else.

I reviewed the incident information and established what was known:

- Server SRV-DC01-APP03 was reported unreachable.
- Application services were unavailable.
- The affected server was located in Rack B12.
- The cause of the outage had not been identified.

I documented an initial investigation plan in the ticket's work notes.

### Initial Investigation

![Initial Investigation](screenshots/06_Initial_Investigation_Workflow.png)

---

## Step 2 — Establish a Theory of Probable Cause

With the initial information documented, the next step was figuring out what could be causing the problem.

Since the server was unreachable, I considered several possibilities:

- **Network cable:** A disconnected or damaged Ethernet cable could interrupt connectivity.
- **Switch port:** A failed or disabled switch port could prevent communication.
- **Network interface:** A faulty server NIC could cause the connection to drop.
- **Server hardware:** A power or hardware failure could make the server unavailable.
- **Network configuration:** An incorrect network setting could prevent communication.

Rather than immediately assuming the server had failed, I wanted to narrow down the possibilities.

---

## Step 3 — Test the Theory

The next step was determining how to isolate the problem.

For this scenario, I documented the checks I would perform during an actual data center investigation.

### Troubleshooting Checklist

| Check | What I'm Looking For |
|-------|----------------------|
| Server Power | Is the server powered on? |
| Hardware Indicators | Are there any warning or failure lights? |
| Switch Port | Is the connected switch interface up? |
| Ethernet Cable | Is the cable connected and undamaged? |
| Server Logs | Are there hardware or network errors? |

The idea was to start with basic physical checks before moving into more advanced troubleshooting.

### Simulated Findings

For this exercise, the scenario established that:

- Server power and hardware indicators were normal.
- Network connectivity was unavailable.
- The Ethernet cable was disconnected.

This pointed to a physical connectivity issue rather than a failed server.

These findings were simulated, not obtained through live equipment testing.

### Troubleshooting Documentation

I recorded the simulated findings and troubleshooting activities in ServiceNow.

![Troubleshooting Results](screenshots/05_Simulated_Troubleshooting_Results.png)

---

## Step 4 — Establish a Plan and Implement the Solution

With the simulated cause identified, the next step was deciding how to restore connectivity.

### Root Cause

The server had lost network connectivity because its Ethernet cable was disconnected.

### Corrective Action

In a real data center, I would first confirm the correct server and network connection before making any changes.

The recovery process would involve:

1. Locating the affected server in Rack B12.
2. Identifying the disconnected network cable.
3. Confirming the correct connection point.
4. Reconnecting the cable.
5. Checking that the network link comes back up.

For this simulation, the Ethernet connection was treated as restored.

No physical cabling changes were performed.

---

## Step 5 — Verify Full System Functionality

Restoring a network connection doesn't automatically mean the entire problem is resolved.

Before closing the incident, I would want to confirm that the server and its application services were functioning normally.

### Verification Checks

- Confirm the switch port shows an active connection.
- Verify the server responds to network connectivity tests.
- Confirm the affected application services are accessible.
- Check for additional errors or recurring connectivity problems.

### Simulated Results

The scenario concluded with:

- Network connectivity restored.
- Server accessibility restored.
- Application services operational.

These results were documented as part of the simulation. No live verification tests were performed.

---

## Step 6 — Document Findings and Resolution

Once the simulated issue was resolved, the final step was making sure the incident record clearly explained what happened.

I documented the reported problem, simulated root cause, corrective action, and outcome in ServiceNow.

### Resolution Summary

| Field | Details |
|-------|---------|
| Incident | INC0010002 |
| Root Cause | Disconnected Ethernet Cable |
| Resolution | Simulated Cable Reconnection |
| Resolution Code | Solution provided |
| Final Status | Resolved |

### Resolution Documentation

![Resolution Details](screenshots/03_Incident_Resolution_Details.png)

### Final Resolution Record

The completed ServiceNow record shows the saved resolution details and the documented outcome.

![Final Resolution](screenshots/07_Final_Resolution_Verification.png)

### Incident Resolved

The incident was successfully moved to the Resolved state in ServiceNow.

![Incident Resolved](screenshots/04_Incident_Resolved.png)

---

# 🛠️ Skills Demonstrated

### ServiceNow Incident Management
- Creating and managing incident tickets
- Setting incident priority
- Assigning incidents to technical support teams
- Documenting investigation activities
- Recording resolution details
- Managing the incident lifecycle

### Data Center Troubleshooting
- Identifying infrastructure issues
- Evaluating potential hardware failures
- Understanding network connectivity problems
- Developing troubleshooting plans
- Identifying possible root causes
- Planning service restoration and verification

### Technical Documentation
- Writing incident work notes
- Recording troubleshooting findings
- Documenting corrective actions
- Maintaining clear incident histories
- Communicating technical information

---

# 📚 What I Learned

This project gave me hands-on experience navigating ServiceNow and managing an incident through its lifecycle.

One of the biggest takeaways was the importance of approaching infrastructure problems systematically.

A server being unreachable doesn't necessarily mean the server itself has failed. The issue could be something as simple as a disconnected cable or an inactive switch port.

I also gained a better understanding of how important documentation is during an incident.

Recording what was reported, what was investigated, and how the issue was resolved helps other technicians understand the situation and provides a useful history if the problem happens again.

---

# 🏁 Project Conclusion

I completed a simulated P2 data center incident using ServiceNow, taking the ticket from initial creation through assignment, investigation, troubleshooting documentation, and resolution.

The project helped me become more familiar with the incident management workflow used by IT operations teams.

It also reinforced how I would approach troubleshooting in a real data center: understand the problem, consider possible causes, investigate systematically, apply the appropriate fix, verify the results, and document the work.

**Project Status: Completed — ServiceNow Data Center Incident Simulation**


