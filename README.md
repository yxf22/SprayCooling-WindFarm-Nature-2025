# Code and Data Repository for "Water-Spray Cooling of Turbine Wakes"

This repository contains the complete simulation files and data for the manuscript titled "Water-Spray Cooling of Turbine Wakes: a Pathway to Enhance Wind Farm Power Generation" submitted to *Nature*.

## 🚀 **Overview for Reviewers**

We provide the **actual case file and data** used to generate the key results in our manuscript. This allows you to:
1.  **Immediately inspect the pre-computed results** by opening the case and data files in ANSYS Fluent.
2.  **Verify all simulation settings**, boundary conditions, and UDF implementations.
3.  **Re-run the simulation** on a capable machine to fully reproduce the results.

**Please Note:** This is the **full-scale, production-ready case**, not a simplified demo. A typical run requires significant computational resources and time, consistent with the scale of the physics reported in the paper.

---

## ⚙️ **Critical System Requirements & Prerequisites**

**BEFORE attempting to open the case files, please ensure your system meets the following requirements. Failure to do so will prevent the UDFs from loading.**

*   **Primary CFD Software:** ANSYS Fluent
*   **Fluent Version:** **18.0**
    > **Important：** This case and its UDFs were developed and tested **exclusively with Fluent 18.0**. Using a newer version will likely cause compatibility issues and UDF compilation failures.

*   **Mandatory Compiler: Microsoft Visual Studio 2010**
    *   This specific version is **required** by Fluent 18.0 to correctly compile the provided User-Defined Functions (UDFs).
    *   **Compatibility Note:** VS2010 is an older product. Please ensure it is installed on a compatible Windows system (e.g., Windows 10).

---

## 📥 **Installation & Setup Guide**

### Step 1: Configure the UDF Environment

The most critical step is to set up the compiler path before launching Fluent.

1.  Set the following environment variable in your system:
    *   Variable name: `VS100COMNTOOLS`
    *   Variable value: `C:\Program Files (x86)\Microsoft Visual Studio 10.0\Common7\Tools\` (Adjust the drive letter if necessary)

2.  **Recommended Alternative:** The most reliable method is to let Fluent set the path itself:
    *   Open the **Windows Command Prompt (cmd.exe)** as an administrator.
    *   Navigate to the `%ANSYS180_DIR%\fluent\ntbin\win64` directory (e.g., `C:\Program Files\ANSYS Inc\v180\fluent\ntbin\win64`).
    *   Run the command: `fluent18.0.exe -env`
    *   This will launch Fluent 18.0 with the correct environment variables for UDF compilation.

### Step 2: Load the Case & Compile UDFs

1.  In Fluent, use `File -> Read -> Case and Data...`
2.  Select the file `Simulation_Files/Full_WindFarm_Simulation.cas` (and the corresponding `.dat` file).
3.  Fluent will now attempt to compile and load the UDFs. You should see messages in the console:
    *   `cpp -I...` (This indicates the compiler is running)
    *   `Finished compilation...`
    *   `Loaded UDF library libudf` <-- **This message confirms SUCCESS.**

    **Troubleshooting:** If you see an error at this stage, it is almost certainly due to an incorrect Visual Studio 2010 installation or environment path.

---

## 🧪 **Instructions for Use & Verification**

### **Option 1: Quick Inspection of Pre-computed Results (STRONGLY RECOMMENDED)**
*   After successfully loading the case and data, the **fully converged solution is immediately available**.
*   You can now directly visualize the velocity field, temperature contours, spray particle tracks, and all other results discussed in the manuscript.
*   This allows for immediate verification of the reported flow physics and quantitative fields without any further computation.

### **Option 2: Full Re-run from Scratch (Optional, Resource-Intensive)**
*   If you wish to perform a completely independent run, you can initialize the solution and start iterating from zero.
*   **Computational Note:** A full run from scratch is computationally intensive and is estimated to take **several days to a week** on a high-performance workstation. The provided `.dat` file serves as a fully-converged restart point to save substantial computation time for the review process.

### **UDF Source Code**
*   The source code for all User-Defined Functions is provided in the `UDF_Source/` directory. You can review this code to understand the custom physics implemented (e.g., droplet injection, phase change models).

---

## 📜 **License**

The simulation setup files, UDF source code, and data in this repository are licensed under the [许可证名称，如 MIT License] - see the `LICENSE` file for details.
**Note:** The commercial software ANSYS Fluent and Microsoft Visual Studio are required to run the simulations and are not included in this license.
