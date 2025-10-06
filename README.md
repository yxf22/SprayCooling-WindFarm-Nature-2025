# Code and Data Repository for "Water-Spray Cooling of Turbine Wakes"

This repository contains the complete simulation files and data for the manuscript titled "Water-Spray Cooling of Turbine Wakes: a Pathway to Enhance Wind Farm Power Generation" submitted to *Nature*.

## 🚀 **Overview for Reviewers**

We provide the **actual case file and data** used to generate the key results in our manuscript. This allows you to:
1.  **Immediately inspect the pre-computed results** by opening the case and data files.
2.  **Verify all simulation settings**, boundary conditions, and UDF implementations.
3.  **Re-run the simulation** on a capable machine to fully reproduce the results.

This repository contains the simulation setup and documentation for our study. The complete dataset, including all large simulation files, is hosted on Zenodo due to its size (>10 GB).

**🔗 Primary Data Download: https://doi.org/10.5281/zenodo.17275486

**Please Note:** This is the **full-scale, production-ready case**, not a simplified demo. A typical run requires significant computational resources and time, consistent with the scale of the physics reported in the paper.

---

## ⚙️ **Prerequisites for Access**

To successfully open and interact with the provided case, the following **must be available on your system**:

*   **CFD Software:** **ANSYS Fluent 18.0**
    > **Critical:** This case and its UDFs were developed **exclusively for Fluent 18.0**. Using a different version will likely cause fatal compatibility issues.

*   **Compiler:** **Microsoft Visual Studio 2010**
    *   This specific version is **required** to compile the provided User-Defined Functions (UDFs). The UDF source code is included in the `UDF_Source/` directory.

## 📥 **Usage Instructions**

## 🚀 **Verification Guide for Reviewers**

We provide two straightforward ways to verify our results:

### **Path 1: Guided Results Analysis (Recommended & Most Efficient)**

**We strongly recommend starting here.** This approach allows you to immediately inspect all key findings from the manuscript without running any simulations.

1.  **Download and extract the `Analysis.zip` file** from the Zenodo archive to a location of your choice.
2.  **Watch the `Analysis.mp4` video guide.** It provides a complete walkthrough of:
    *   Loading the `analysis-15mw-8ms.cas` file in Fluent.
    *   Visualizing the key flow fields: **velocity, temperature, and humidity**.
    *   Inspecting both **instantaneous** and **time-averaged** results.
    *   Viewing the critical **difference fields** between various spray scenarios and the baseline (no-spray) condition, which form the core of our findings.
3.  Follow the video to explore the pre-computed results directly. All quantitative results and figures discussed in the manuscript can be verified this way within minutes.

### **Path 2: Re-simulation Workflow Demonstration**

For transparency into our complete simulation setup and execution workflow, we provide a second demonstration.

**Prerequisite Setup for Re-simulation:**
1.  **Download and extract the `Re-simulation.zip` file** from the Zenodo archive.
2.  **Extract the Inlet Data:** Locate and extract the `pre-data-1-2000s.zip` archive.
3.  **Verify Path Consistency (Critical):** The journal files contain predefined paths to read the inlet velocity data. You must ensure that the path to the extracted `pre-data-1-2000s` folder on your system matches the path specified within the journal files. If the paths differ, the simulation will fail to read the necessary inlet conditions.

**Workflow Demonstration:**
1.  **Watch the `Resimulation.mp4` video.** It demonstrates the setup and subsequent steps:
    *   Loading the initial `Standard.case` and `Standard.data` files.
    *   Compiling the UDF (actuator disk model).
    *   Executing the pre-configured journal files in sequence to launch the transient simulation.
2.  The video concludes once the simulation is actively running and displaying convergence monitors. The subsequent automated 2,000-second calculation requires no further intervention.


---
