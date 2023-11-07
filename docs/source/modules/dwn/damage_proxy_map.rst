Damage proxy maps
=================

Damage proxy maps based on coherence change detection (CCD)
-----------------------------------------------------------

This module provides a fully automated workflow for the creation of damage proxy maps based on the method of coherent change detection (CCD) with Sentinel-1 SLC data, as described by `Tay et al. (2020) <https://www.nature.com/articles/s41597-020-0443-5>`_. 

The output data files consist of the damage proxy map as GeoTiff (*dmp_...tif*) and KMZ (*dmp_...kmz*) files, as well as the raw CCD values in GeoTiff (*CCD_...tif*) and GeoJSON (*CCD_...geojson*) formats. 

The files are found within a newly created folder. The folder name is based on the name of your area of interest (AOI) and the event date.

.. attention:: 

    Minimum requirements:

    -   **m16 instance** (16 CPU and 64 GB RAM)
    -   **50 GB of free disk space** 
    
The two steps of the process are explained in the following section.
    
Select an AOI
-------------

Using the provided AOI selector, select an AOI of your choice between the different methods available in the tool. We provide three administration descriptions (from Level 0 to Level 2) and three custom shapes (drawn directly on the map or OGR-compatible files). 

.. figure:: https://raw.githubusercontent.com/sepal-contrib/damage_proxy_maps/main/doc/img/aoi_select.png 
    
    AOI selector
    
Parameters
----------

-   Disaster event date: Choose the date where the disaster event happened.
-   Copernicus credentials: Provide your Sci-Hub credentials for searching and downloading relevant Sentinel-1 scenes (if you do not have an account, register with `Copernicus Sci-Hub <https://scihub.copernicus.eu/>`_).  

Selecting this button will trigger the full workflow. (Note: Some of the steps such as downloading and processing may take a while. If you have an unstable internet connection, set the minimum runtime of your instance to two hours; otherwise, stay connected to the SEPAL website by keeping your browser and corresponding browser tab open.)

.. note::

    If processing does not finish, you can rerun the module with the same parameters and processing will continue from where it stopped.
    
Once the computation is finished, the result files will be stored in the :code:`module_results/Damage_proxy_map/<aoi name>_<event date>/` folder. 

.. figure:: https://raw.githubusercontent.com/sepal-contrib/damage_proxy_maps/main/doc/img/complete.png 

.. custom-edit:: https://raw.githubusercontent.com/sepal-contrib/damage_proxy_maps/release/doc/en.rst

.. custom-edit:: https://raw.githubusercontent.com/sepal-contrib/damage_proxy_maps/release/doc/en.rst
