## Controls commands environment

  <div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">This sample demonstrates changing the symbols used by the out-of-the-box New Marker, Line, Freehand, Rectangle, and Polygon element tools. By default, these tools use a black symbol (and a yellow fill where appropriate). The default symbols can be changed by updating the properties of the CommandsEnvironment singleton object. The sample uses the SymbologyControl in conjunction with the PageLayoutControl, ToolbarControl, and the controls commands. The properties on the IGraphicProperties interface are used by the controls commands to manage default symbology.</div>
  <div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53"> </div>
  <div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">This sample has been developed on a machine with a display screen resolution of 96 dots per inch (dpi). This sample also contains code that will correctly scale the ArcGIS Engine controls when run at a resolution of 120 dpi. This issue is discussed in detail in the [Workaround for controls display issues in 96 versus 120 dpi](http://6cebc1d9-2318-472e-923a-13e13b1a8e45) topic. </div>  


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
1. Load a map document into the PageLayoutControl.  
1. Add elements to the display using the commands on the ToolbarControl.  
1. Right-click the display to add a text element containing today's date.  
1. Change the application default symbol properties using the combo box and the items displayed in the SymbologyControl.  
1. Repeat steps 2 and 4 if desired.  





#### Additional information  
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">The LoadStyleFile method is used within the Form_Load event to add the contents of ESRI.ServerStyle into the SymbologyControl. A new ServerStyleGalleryItem is created with its name set to myStyle and its item set to the MarkerSymbol, LineSymbol, FillSymbol, and TextSymbol properties on the IGraphicProperties interface. ServerStyleGalleryItem is added to the appropriate StyleClass using the ISymbologyStyleClass.AddItem method.</div>  
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53"> </div>  
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">A combo box is populated with marker, line, fill, and text symbol items. The SelectedIndexChanged event of the combo box is used to set the type of items displayed in the SymbologyControl using the StyleClass property. Clicking an item displayed in the SymbologyControl fires OnItemSelectedEvent. The IStyleGalleryItem.Item property is used to determine whether the item implements IMarkerSymbol, ILineSymbol, IFillSymbol, or ITextSymbol; and either the MarkerSymbol, LineSymbol, FillSymbol, or TextSymbol property on the IGraphicProperties interface is set.</div>  
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53"> </div>  
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-02-10T23:25:53">The IPageLayoutControlEvents.OnMouseDown event is used to create a new TextElement. The Text property is set to today's date and the Symbol property is set to IGraphicsProperties.TextSymbol. The element is added to the GraphicsContainer using the IPageLayoutControl.AddElement method.</div>  


#### See Also  
[CommandsEnvironment class](http://desktop.arcgis.com/search/?q=CommandsEnvironment%20class&p=0&language=en&product=arcobjects-sdk-dotnet&version=&n=15&collection=help)  
[IGraphicProperties interface](http://desktop.arcgis.com/search/?q=IGraphicProperties%20interface&p=0&language=en&product=arcobjects-sdk-dotnet&version=&n=15&collection=help)  
[Workaround for controls display issues in 96 versus 120 dpi](http://desktop.arcgis.com/search/?q=Workaround%20for%20controls%20display%20issues%20in%2096%20versus%20120%20dpi&p=0&language=en&product=arcobjects-sdk-dotnet&version=&n=15&collection=help)  


---------------------------------

#### Licensing  
| Development licensing | Deployment licensing | 
| ------------- | ------------- | 
| Engine Developer Kit | Engine |  
|  | ArcGIS Desktop Basic |  
|  | ArcGIS Desktop Standard |  
|  | ArcGIS Desktop Advanced |  


