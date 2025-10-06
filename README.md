# Code and Data Repository for "Water-Spray Cooling of Turbine Wakes"

This repository contains the complete simulation files and data for the manuscript titled "Water-Spray Cooling of Turbine Wakes: a Pathway to Enhance Wind Farm Power Generation" submitted to *Nature*.

## 🚀 **Overview for Reviewers**

We provide the **actual case file and data** used to generate the key results in our manuscript. This allows you to:
1.  **Immediately inspect the pre-computed results** by opening the case and data files.
2.  **Verify all simulation settings**, boundary conditions, and UDF implementations.
3.  **Re-run the simulation** on a capable machine to fully reproduce the results.

**Please Note:** This is the **full-scale, production-ready case**, not a simplified demo. A typical run requires significant computational resources and time, consistent with the scale of the physics reported in the paper.

---

## ⚙️ **Prerequisites for Access**

To successfully open and interact with the provided case, the following **must be available on your system**:

*   **CFD Software:** **ANSYS Fluent 18.0**
    > **Critical:** This case and its UDFs were developed **exclusively for Fluent 18.0**. Using a different version will likely cause fatal compatibility issues.

*   **Compiler:** **Microsoft Visual Studio 2010**
    *   This specific version is **required** to compile the provided User-Defined Functions (UDFs). The UDF source code is included in the `UDF_Source/` directory.

## 📥 **Usage Instructions**

### **Primary Method: Inspection of Pre-computed Results**
1.  Ensure your Fluent 18.0 environment is correctly configured for UDF compilation with Visual Studio 2010. (General guidance on this setup is widely available in ANSYS documentation and online forums.)
2.  In Fluent, use `File -> Read -> Case and Data...` to load the files from the `Simulation_Files/` directory.
3.  Upon successful loading and UDF compilation (confirmed by a `"Loaded UDF library libudf"` message in the console), the **converged solution is immediately available** for inspection.
4.  You can now directly visualize all flow fields and results discussed in the manuscript without any further computation.

### **Secondary Method: Independent Re-run**
*   The provided case can also be used to perform a completely independent run from scratch.
*   **Computational Note:** A full run is resource-intensive and estimated to take **several days to a week** on a high-performance workstation. The provided `.dat` file serves as a fully-converged restart point.

---

## 📜 **License**

The simulation setup files, UDF source code, and data in this repository are licensed under the [许可证名称，如 MIT License] - see the `LICENSE` file for details.
**Note:** The commercial software ANSYS Fluent and Microsoft Visual Studio are required to run the simulations and are not included in this license.
