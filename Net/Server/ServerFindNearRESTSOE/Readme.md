## Find near features REST SOE

  <div xmlns="http://www.w3.org/1999/xhtml">This sample illustrates the basic framework for creating a server object extension (SOE) that will be hosted as an ArcGIS Server REST SOE. The SOE extends the functionality of a map service with a basic geospatial operation<font face="Verdana">—</font>namely the ability to find features in all feature layers via a user-defined location and distance.   
</div>
  <div xmlns="http://www.w3.org/1999/xhtml">All the information needed to deploy the SOE is included in this sample encapsulated in a .soe file. Deploying the SOE from this file does not require you to open Visual Studio. However, you can open the Visual Studio solution included with this sample to explore the coding patterns used in the SOE.</div>
  <div xmlns="http://www.w3.org/1999/xhtml"> </div>
  <div xmlns="http://www.w3.org/1999/xhtml">The instructions below assume that you have installed the developer kit on the machine running ArcGIS Server Manager. If you installed the developer kit on some other machine, you'll need to copy the .soe file to the machine running Manager, or otherwise make the .soe file visible to Manager by placing it in a shared folder.</div>  


<!-- TODO: Fill this section below with metadata about this sample-->
```
Language:              C#
Subject:               Server
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
#### Deploy the SOE  
1. Log in to ArcGIS Server Manager and click Site.  
1. Click Extensions.  
1. Click Add Extension.  
1. Click Browse and navigate to the .soe file, which by default is located at <ArcGIS DeveloperKit install location>\Samples\ArcObjectsNet\ServerFindNearRESTSOE\CSharp\FindNearFeaturesRestSOE\bin\Debug\NetFindNearFeaturesRESTSOE.soe.   
1. Click OK.  

#### Enable the SOE on a service  
1. Start ArcMap and click File > Open.  
1. Browse to or type the location of USA.mxd, which is located in <ArcGIS Developer Kit Location>\Samples\data\Usa.  
1. Click File > Share As > Service.  
1. Click Save a service definition and click Next.  
1. Choose "No available connection" and check "Include data in service definition when publishing".  
1. Change the Server type to ArcGIS Server.  
1. Leave the Service name as USA and click Next.  
1. Choose a location where you want to save the service definition, then click Continue.  
1. Click Stage to create the service definition. In the success message, note the path of your service definition (.sd).  
1. Copy the USA.sd file to the machine running ArcGIS Server Manager.  
1. On the machine running ArcGIS Server Manager, log in to Manager and click Services.  
1. If necessary, click the Manage Services tab.  
1. Click Publish Service.  
1. Click Browse, browse to the location of USA.sd on the local machine, and click Open. Then click Next.  
1. Accept the default properties for the service by clicking Next.  
1. Click Publish. This creates the USA map service.  
1. On the Services tab of Manager, select the USA map service, then select Capabilities. In the list of available capabilities, find ".NET Find Near Features REST SOE" and check the box to enable it. If there is a list of available operations allowed, select all of them.  
1. Click Save, then click Restart to restart the service.  

#### Test the SOE in the ArcGIS Server Services Directory  
1. Open a browser and navigate to the root REST services endpoint for ArcGIS Server (for example: http://<server name>:6080/arcgis/rest/services). You'll see a list of services, including the USA map service created in the previous section.   
1. Click the USA map service created in the previous section and scroll to the bottom of the map service description page. The section titled Supported Extensions includes the SOE NetFindNearFeaturesRestSOE.   
1. Click the SOE name. The REST SOE description page displays a list of layers in the map service.   
1. Click a layer to display a layer description and a list of supported operations. One supported operation is listed: findNearFeatures.   
1. Click the operation to display the interactive dialog box to define a location and distance to use when searching for features in this layer.   
1. Define a location in ArcGIS JavaScript Object Notation (JSON) format; for example: {x:-112,y:35}. Do not include spatial reference in the location JSON.  
1. Define a distance in map units; for example: 1.   
1. Click either the findNearFeatures (GET) or findNearFeatures (POST) button to initiate the request. A response containing the features and attributes for features within the search distance is returned.   









---------------------------------

#### Licensing  
| Development licensing | Deployment licensing | 
| ------------- | ------------- | 
|  |  |  
|  |  |  


