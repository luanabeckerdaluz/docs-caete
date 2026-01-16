HARMONIZE Brazil INPE - Instance V2
===================================

The HARMONIZE instance V2, presented in Figure below,  is our new technical-scientific concept for data visualization and analysis based on the Brazil Data Cube (BDC) project solutions, but tuned for the HARMONIZE project using the concept of toolkits for health attention (cube4health). It comprises a web portal (HARMONIZE Explorer) and a Data Science environment (BDC Lab) that provide mechanisms for manipulating Earth Observation data (Cubes), drone data (images, mosaic, multispectral, thermal data, and vegetation index), health and climate data (indicators).

The user defines collections and temporal coverage on the portal, which queries the data via the SpatioTemporal Asset Catalog (STAC) API, returning all the data or images found based on the user's query. As a web service interface, the STAC API is a core service of the BDC project. This service enables complex query abilities, such as spatial or temporal predicates, over a group of STAC objects in a database.

In this context, the integration of drone data and other data sources used in the HARMONIZE project adapts and incorporates STAC specifications to preserve interoperability with the current infrastructure of the BDC project, which serves as the basis for our Earth Observation Data Cube tuned for Health Response Systems (EODCtHRS) component.

.. figure:: ../source/img/instance-v2.png
   :align: center
   :width: 90%
   :figclass: align-center

   **The overview of HARMONIZE Instance V2 infrastructure components based on Back-end (cube4health) and Front-end software solutions.**