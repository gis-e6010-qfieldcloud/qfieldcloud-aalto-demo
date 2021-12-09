# qfieldcloud-aalto-demo
Documentation for running QFieldCloud and connecting from QField application and QGIS.

# Where things can be found
- Spatial data used in the project
  - can be found as two ZIP-files. One contains the geopackages, other the SQL dumps which can be used to create data in a PostGIS database
- The final report
  - [As a separate PDF-file](https://github.com/gis-e6010-qfieldcloud/qfieldcloud-aalto-demo/blob/main/GIS_E6010_final_report.pdf)
- Example project file
  - [QGS-file](https://github.com/gis-e6010-qfieldcloud/qfieldcloud-aalto-demo/blob/main/exampleQfieldProject.qgs)
    - Note that the different line endings in Linux vs Windows might cause problems. Git will convert line changes but if you download the file directly, they will be Linux line endings.
- QFieldCloud used in the project
  - The [submodule](https://github.com/gis-e6010-qfieldcloud/qfieldcloud_gis-e6010/tree/fc422d1ab18f43d15eb5a01874d24bd2d57be4d4) in the repository is closest to the state of QFieldCloud when we were working on it. 

# How to use
Clone recursively
`git clone --recursive https://github.com/gis-e6010-qfieldcloud/qfieldcloud-aalto-demo.git´
to fetch repository and the submodule
or just
`git clone https://github.com/gis-e6010-qfieldcloud/qfieldcloud-aalto-demo.git´
if you don't want to use the supplied version of QFieldCloud.
