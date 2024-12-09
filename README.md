# dronedata
This github offerst tools to be used to transform drone-based datasets into FAIR datasets to be archived. 

Author: richard.hann@ntnu.no & ilkka.matero@sios-svalbard.org, Date: 2024.12.09

Short python code for converting GDAL output to CF-compliant netCDF format.

The intended use of this code is for converting files that are already in netcdf format to CF-compliant NetCDF -files by adding the required and recommended metadata elements to the output file. For installing and using Geospatial Data Abstraction Library (GDAL) for converting GeoTIFF to NetCDF, please refer to https://nsidc.org/data/user-resources/help-center/how-do-i-convert-geotiff-netcdf-file.

Usage:
0.1 Install python, GDAL and the required packages
0.2 Download this code
0.3 Use GDAL to convert your GeoTIFF to netCDF4

Add the required and recommended metadata fields into a .csv file in the "data" folder. There is an example file that you can use guidance.
Change the following lines in "dronedata_to_cf_netcdf.py" in the root to point to the correct paths for the input files (.nc and .csv files containing the DEM and metadata respectively): gdal_fp = 'data/<input_filepath.nc>' metadata_fp = 'data/<metadata_filepath.csv>' output_fp = 'output/<output_filepath>.nc'
Run the "dronedata_to_cf_netcdf.py" code.
Requirements:

python
xarray
netCDF4
csv
datetime
subprocess
gdal
