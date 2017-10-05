# KET – Knickzone Extraction Tool

## summary

This tool was created to identify knickzones (relatively steep segment along rivers) using a DEM by user specified constraints. It also calculates the height and length of the kniczones. The toold is designed for Esri ArcGIS software, comprising two steps as below:

1. Computation of relative steepness (Rd) raster for a given DEM.  
Required:
    * TauDEM (5.1.1 for ArcGIS 10, 10.1, and 10.2)
    * Spatial Analyst license
    * DEM as GeoTIFF format
    * 'From', 'to', and 'by' values in scale for slope calculation
2. Produces a knickzone shapefile.  
Required:
    * DEM as TIFF
    * Rd (relative steepness) raster previously calculated
    * Flow accumulation raster for stream network extraction
    * A threshold value in Rd for knickzone extraction  

![img](./fig_ket_sample.png)

## download
* [ArcGIS Toolbox (.tbx) with Help files (zip, 51 KB)](https://github.com/hdtopography/sandbox/raw/master/KET/KET.tbx)
* [tutorial (pdf, 1.6 MB)](https://github.com/hdtopography/sandbox/raw/master/KET/tutorial_160226.pdf)  
* sample data  
  * [sample DEM GeoTIFF (zip, 71 MB)](http://topography.csis.u-tokyo.ac.jp/resources/tools_ket/sampleDEM.zip)  
  * [Rd raster (result of Step 1) GeoTIFF (zip, 75 MB)](http://topography.csis.u-tokyo.ac.jp/resources/tools_ket/SampleRS.zip)

## help
1. [tool part I](./help/KET1Help.htm)  
computation of Rd raster by various scale slope calculation  
> http://topography.csis.u-tokyo.ac.jp/resources/tools_ket/KET1Help.htm

2. [tool part II](.help/KET2Help.htm)  
extraction of knickzones by Rd raster and knickzone form calculation
> http://topography.csis.u-tokyo.ac.jp/resources/tools_ket/KET2Help.htm

## source code
1. [tool part I (txt)](./source_code/source_code_1.txt)  
2. [tool part II (txt)](./source_code/source_code_2.txt)  

## references

* Hayakawa, Y.S., Oguchi, T., 2006: DEM-based identification of fluvial knickzones and its application to Japanese mountain rivers. Geomorphology 78, 90–106. [doi:10.1016/j.geomorph.2006.01.018](http://www.sciencedirect.com/science/article/pii/S0169555X06000316?via%3Dihub)  
* Hayakawa, Y.S., Oguchi, T., 2009: GIS analysis of fluvial knickzone distribution in Japanese mountain watersheds. Geomorphology 111, 27–37. [doi:10.1016/j.geomorph.2007.11.016](http://linkinghub.elsevier.com/retrieve/pii/S0169555X09001408)  
* Zahra, T., Paudel, U., Hayakawa, Y.S., Oguchi, T. (2017.04) Knickzone Extraction Tool (KET) - A new ArcGIS toolset for automatic extraction of knickzones from a DEM based on multi-scale stream gradients. Open Geosciences, 9 (1), 73-88. [doi:10.1515/geo-2017-0006](https://doi.org/10.1515/geo-2017-0006)
