# Circular Task Analysis Project – MouseReMoCo

## Authors : Camille Jaffeux, Théo Lecomte & Baptiste Augros

This repository contains data, tools, and scripts for analyzing circular and linear mouse-based motor control tasks using MouseReMoCo. It provides the interface to perform tasks, record data, and reproduce results programmatically. The project is licensed under the GNU General Public License v3 (GPLv3).

---

## Summary
1. [Overview](#overview)  
2. [Project Structure](#project-structure)
3. [Requirements](#requirements)  
4. [Getting Started](#getting-started)  
5. [Launch](#launch)
6. [Files and Folder Descriptions](#files-and-folder-descriptions)
   - [1. Data Folder](#1-data-folder)
   - [2. Tools Folder](#2-tools-folder)
   - [3. Document Folder](#3-document-folder)
   - [4. HTML File](#4-html-file)
   - [5. main.ipynb file](#5-mainipynb-file)
7. [Licence](#licence)  

---

## Overview 

The project allows to :

-Perform circular steering tasks with optional rhythmic pacing using MouseReMoCo.  
-Record mouse coordinates over time, along with task markers.  
-Visualize results interactively in the HTML interface and reproduce graphs and analyses via Python/Jupyter Notebook (main.ipynb).  
-Optionally stream data in real-time using Lab Streaming Layer (LSL) or record into XDF files for offline analysis.

---

## Project Structure
```
├── data/                           # Task data
│   ├── 001MoDe_R1.csv              # Raw task data
│   ├── 001MoDe_R1.marker.csv       # Raw task markers
│   ├── data.csv                    # Recorded task data from student experiments
│   └── marker.csv                  # Recorded task markers from student experiments 
├── Tools/                          # Software tools
│   └── MouseReMoCo                 # MouseReMoCo software for recording tasks
├── Document/                       # Documentation
│   └── Fauviaux                    # Scientific article
│
├── main.ipynb                      # Jupyter Notebook to reproduce results and generate figures
├── circular-task-assignment.html   # HTML interface for circular task, interactive visualization
│   
├── README_CircularTask.md                       # This file
└── LICENSE                         # GNU General Public License 
```

---

## Requirements:
-Python 3.12+ (for Jupyter Notebook analysis)  
-Java 8+ (https://www.java.com/fr/download/)  
-MouseReMoCo.jar (latest release)  
-Optional: LSL library for streaming (https://github.com/sccn/liblsl/releases)  
-Optional for recording: LabRecorder (https://github.com/labstreaminglayer/App-LabRecorder/releases)  

---

## Getting Started

1. Clone the repository:
```bash
git clone <repository-url>
cd <repository-directory>
```

2. Run MouseReMoCo:

```bash
cd tools/MouseReMoCo
java -jar mouseReMoCo.jar
```

3. Record tasks using the HTML interface or MouseReMoCo.

4. Analyze data in main.ipynb:

-Load data.csv and marker.csv  
-Reproduce figures and results programmatically

---

## Launch:
```bash
cd /path/to/MouseReMoCo
java -jar mouseReMoCo.jar
```
### Controls:

- space – toggle record/pause  
- c – display configuration  
- q – quit  
- w – (undocumented) real-time circular task view

---

## Files and Folder Descriptions :

### 1. Data Folder :

Contains both raw data provided by MouseReMoCo and processed data recorded during student experiments.  

- 001MoDe_R1.csv – Raw task data from MouseReMoCo  
- 001MoDe_R1.marker.csv – Raw task markers  
- data.csv – Task data recorded by the student group  
- marker.csv – Task markers recorded by the student group  

### 2. Tools Folder :

- MouseReMoCo software for running circular and linear mouse tasks.  
- Records mouse coordinates and task markers over time.  
- Supports optional streaming via LSL and recording to XDF files.

### 3. Document Folder :

Contains the scientific article(s) used as the foundation for this research, including:

- Fauviaux, *Can a circular steering task quantify sensorimotor integration in persons with stroke?*

### 4. HTML File :

- circular-task-assignment.html – Interactive HTML template to follow to achieve circular task assignment.  
- Provides real-time visual feedback and results visualization.  
- Can export data.csv and marker.csv for further analysis in Python.

### 5. main.ipynb file :

Jupyter Notebook containing Python scripts to:  

- Load and process the recorded CSV data
- Generate graphs and figures for analysis
- Reproduce results programmatically from the HTML output

---

## Licence :

This project is free software: you can redistribute and/or modify it under the terms of the GNU GPL v3.
No warranty is provided; see LICENSE for details.