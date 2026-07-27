# ccm2cdse
Set of scripts and utilities allowing onboarding of Copernicus Contributing Mission (CCMs) data into the Copernicus Data Space Ecosystem

## CCM CAT-1 product naming convention

Name of the CCM product should follow this pattern: MMNN_TTTTTTTTTT_YYYYMMDDTHHMMSS_YYYYMMDDTHHMMSS_VXYZ

The CCM product name should be reflected in the:

- Tar file name i.e. MMNN_TTTTTTTTTT_YYYYMMDDTHHMMSS_YYYYMMDDTHHMMSS_VXYZ.tar
- Folder within the Tar file i.e. ./MMNN_TTTTTTTTTT_YYYYMMDDTHHMMSS_YYYYMMDDTHHMMSS_VXYZ/some.tif
- STAC item file name ./MMNN_TTTTTTTTTT_YYYYMMDDTHHMMSS_YYYYMMDDTHHMMSS_VXYZ.json

| Name element description | Pattern | Comment |
| ------------- |:-------------:| ------------- |
| This is equivalent to the “CCM ID” that is the mission identifier  | MMNN | String of 4 characters, generally 2 letters and 2 numbers |
| Product descriptor | TTTTTTTTTT  |  3 uppercase characters for the sensor identifier followed by _ plus 3 characters for the sensor mode/product abreviation (e.g. LST for Land Surface temperature) followed by _ and 2 characters for the Processing Level e.g. L2 for Level 2 |
| Product Validity Start Date and Time | [YYYYMMDD]T[HHMMSS] | 15 characters (separated by “T” character) YYYY -> year (e.g. 2008) MM -> month (e.g. 03) DD -> day (e.g. 01) HH -> hours (e.g. 23) MM -> minutes (e.g. 35) SS -> seconds (e.g. 22) |
| Product Validity End Date and Time | [YYYYMMDD]T[HHMMSS] | 15 characters (separated by “T” character) YYYY -> year (e.g. 2008) MM -> month (e.g. 03) DD -> day (e.g. 01) HH -> hours (e.g. 23) MM -> minutes (e.g. 35) SS -> seconds (e.g. 22) |
|Product version| VXYZ | 4 characters alphanumeric string, starting with V and three numbers identifying the product version. X – major version (e.g. 1): backwards-incompatible modification of the retrieval mechanism or a data format; user needs to adjust their processing flows. Y – minor version (e.g. 2): backwards-compatible modification of the retrieval mechanism (e.g. improved atmospheric correction) or addition of a new attribute/layer. Z – patch version (e.g. 3): backwards-compatible modification related to a bug-fix in the algorithm or input data. |
