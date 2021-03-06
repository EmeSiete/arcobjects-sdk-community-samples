## Draw text on a MapControl

  <div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">This draw text sample application demonstrates the splined text rendering capabilities of ArcObjects. When you click the map to track a line, the MapControl method DrawText is used to place the text within the text box along the tracked line. At least two clicks are required for the line and text to appear on the MapControl. </div>  


<!-- TODO: Fill this section below with metadata about this sample-->
```
Language:              C#, VB
Subject:               Controls
Organization:          Esri, http://www.esri.com
Date:                  11/17/2017
ArcObjects SDK:        10.6
Visual Studio:         2015, 2017
.NET Target Framework: 4.5
```

### Resources

* [ArcObjects .NET API Reference online](http://desktop.arcgis.com/en/arcobjects/latest/net/webframe.htm)  
* [Sample Data Download](../../releases)  
* [What's new](http://desktop.arcgis.com/en/arcobjects/latest/net/webframe.htm#05247c04-bfd9-4e36-ae09-bc6e833c3b14.htm)  
* [Download the ArcObjects SDK for .Net from MyEsri.com](https://my.esri.com/)  

### Usage
1. Type the text to annotate the map.   
1. Use the left mouse button to trace a line on the map, and use the right mouse button to zoom in.  





#### Additional information  
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">The application uses the AddLayerFromFile method to load the world continents sample data, which is then symbolized. The OnClick event either uses the TrackRectangle method to zoom in (if the right or middle mouse button has been used) or adds the new point to the line and updates the display through the Refresh method. The Refresh method is used to draw the esriViewForeground, thereby removing any previously drawn annotation and triggering the MapControl's OnAfterDraw event. The OnAfterDraw event uses the DrawShape and DrawText methods to draw the line and text onto the MapControl in response to the refresh of the esriViewForeground phase. </div>  


#### See Also  
[MapControl class](http://desktop.arcgis.com/search/?q=MapControl%20class&p=0&language=en&product=arcobjects-sdk-dotnet&version=&n=15&collection=help)  
[IMapControl2 interface](http://desktop.arcgis.com/search/?q=IMapControl2%20interface&p=0&language=en&product=arcobjects-sdk-dotnet&version=&n=15&collection=help)  


---------------------------------

#### Licensing  
| Development licensing | Deployment licensing | 
| ------------- | ------------- | 
| Engine Developer Kit | Engine |  
|  | ArcGIS Desktop Basic |  
|  | ArcGIS Desktop Standard |  
|  | ArcGIS Desktop Advanced |  


