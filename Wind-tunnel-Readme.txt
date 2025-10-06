Wind Tunnel Experimental Data Description

This directory contains the raw and processed data from wind tunnel experiments referenced in our manuscript.

File Contents:
- .THA files: Raw data from 3D anemometer measurements
- .ASA files: Post-processed data containing physical quantities at each measurement point

Data Processing:
The MATLAB script 'ReadTHFile.m' is provided to read and process the raw .THA files. The script includes detailed instructions for:
1. Reading the raw .THA data files
2. Reconstructing three velocity components (Ux, Uy, Uz)
3. Calculating mean velocity, turbulence intensity, and other physical quantities

For Reviewers:
- For quick verification: Refer to the .ASA files for post-processed results
- For full reproduction: Use the ReadTHFile.m script with the .THA files as described above

Contact: [shenglichen@sz.tsinghua.edu.cn]