# qfieldcloud-aalto-demo
Documentation for running QFieldCloud and connecting from QField application and QGIS.

# Data from the NLS Topographic database
You can data from the Topographic database in three ways: Via QGIS using the WFS/OGC tool, download service and directly from browser or similar tool. All of those ways have their advantages and disadvantages. We will describe those ways here. You need to create an API key for the API if you decide to use something other than the download service.
## Using QGIS
Perhaps the most obvious way to obtain data from the Topographic database is to connect to their OCG Features API from the QGIS application. For this you need version 3.0 or newer since the feature was added in that version. However, this often doesn't work as well as it should. The tool tries to download all the features in Finland and therefore the QGIS application often hangs for a considerable time if you try to add some layer to a map. Some of the layers work better than others. For example, we managed to add layers 'korkeuskäyrä' (contours), 'kallioalue' (boulder areas) and 'rakennus' relatively easily but some returned errors and some hanged the application which required force killing the program using task manager. 

You can add API connection from QGIS source browser by going to WFS/OGC API -> New connection -> insert API endpoint as the URL and under Basic HTTP authentication insert API-key into the username field leaving the password field empty. Select OGC API from the dialog as the version. The layers should then appear into the source browser under the name you defined in the dialog. You can then try to add them into the project. If you manage to add them to the project, it's a good idea to limit the extent of the layer. For that it's recommendable to create a layer, for example an empty raster, which covers the area you want to use as the bounding box or you can use the current map view as the extent. The extent can be adjusted by clicking the layer in the 'Layer' window, then select Properties from the context menu, and then Metadata -> Extent. Under extent you might have to first set the CRS, then you can limit the extent by either clicking the 'Calculate from layer' or you can press the 'Map canvas extent' which will limit the extent to the current view. Finally, you can export the data to a different format such as geopackage or directly to a database.
### Method in a nutshell
- Hard to limit the extent or adjust the parameters before adding layers
- Hangs very often
- Some layers return errors
- If it works, you get to download everything at once

## Using the API via browser or equivalent networking tool



