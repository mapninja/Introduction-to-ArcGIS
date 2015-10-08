#Introduction to GIS with ArcGIS

####Stacey Maples – Geospatial Manager – Stanford Geospatial Center – <stacemaples@stanford.edu>
####David Medeiros – GIS Instruction & Support Specialist  - Stanford Geospatial Center - <davidmed@stanford.edu> 
This introductory session will focus upon the fundamental concepts and skills needed to begin using Geographic Information Systems software for the exploration and analysis of spatial data using the ArcGIS platform.  Topics will include: 

* What is GIS? 
* Spatial Data Models and Formats
* Projections and Coordinate Systems
* Basic Data Management
* The ArcMap User Interface 
* Simple Analysis using Visualization  

#GIS Resources:
Stanford Geospatial Center website - [http://gis.stanford.edu/](http://gis.stanford.edu/)  
Stanford GIS Listserv - [https://mailman.stanford.edu/mailman/listinfo/stanfordgis](https://mailman.stanford.edu/mailman/listinfo/stanfordgis)    
Esri ArcGIS 10.2 Help - [http://resources.arcgis.com/en/help/main/10.2/](http://resources.arcgis.com/en/help/main/10.2/)
   
##Download Tutorial Data
1. In a browser, go to [https://stanford.box.com/SGCIntroGIS](https://stanford.box.com/SGCIntroGIS) and click on the drop-down arrow to the right of each folder to download individual datasets. Save the Dataset(s) to your Desktop.
2. Right-click on the resulting *.zip file and select **Extract All…**
3. Accept all defaults to extract the data file.


##Open ArcMap and Explore the User Interface
ArcMap is the 2D mapping component of the ArcGIS Suite of software.  Most of your basic data management and analysis will be done in using ArcMap.  The first thing we want to do is Open ArcMap and get familiar with the Default User Interface.  

1. In Windows, go to the Programs menu and find the ArcGIS Program Group, then select ArcMap to Open ArcMap.
2. You should be presented with the New Document dialog window, with the Blank Map template selected by default.  Simply click OK to accept this template.

You should then be presented with something like the interface you see below:

##The Basic Components of the ArcMap Interface
The ArcMap interface is made up of three basic components:   

* The Data Frame – The Data Frame is where your geographic datasets will be visualized
* Tabbed Windows:
* The Table of Contents – The Table of Contents is the most important of the ‘Tabbed Windows” set, and is visible by default.  This window is where you will interact with your data most of the time.  As you add geographic and non-geographic datasets to your Map Document, they will show up in the Table of Contents as Layers.  Much of your work in ArcMap will be initiated by right-clicking on one or more of the Layers in the Table of Contents.
* Search Window – The Search Window shows up, by default, as a Tabbed Window.  This window is used to search for ArcToolbox Tools, Map Documents and Data (provided you have enabled indexing for your data folders, which will be covered in a later lab).
* Catalog Window – The Catalog Window functions much as Explorer does in Windows.  In this window, you can create connections to drives, folders and network resources for use in ArcGIS.  Many of the tasks related to data maintenance (creating empty shapefiles/feature classes, new Geodatabases, etc…) are performed using the Catalog Window.  This window acts as a ‘lite’ version of the more fully featured ArcCatalog component of the ArcGIS Suite.
* Tables, Imagery Analysis Window, etc… - There are a few other windows that can be ‘Tabbed’ in ArcMap.  We will cover these as needed in the tutorials.
* Toolbars – There are literally dozens of Toolbars in ArcMap.  Each of these toolbars is composed of a set of buttons that launch tools that are related to a GIS task of some sort.  For example, the oh-so creatively named “Tools” Toolbar is composed of the most often used tools for navigating in the Data Frame and basic selection and querying of data layers.  Toolbars can be enabled in several ways, but the easiest is to simply right-click in an empty area of the toolbar part of ArcMap and select the toolbar you need.

##Enabling and Rearranging the User Interface/Toolbars
###Enable Effects Toolbar
1. On the Main Menu, go to Customize>Toolbars>Effects Toolbar to enable the Effects Toolbar.
2. Click and Drag the Effects Toolbar just to the right of the Standard Toolbar, and note that you can “dock” toolbars at the top, bottom and sides of the ArcMap interface. 
3. We will make use of this toolbar later in the tutorial.

###Interacting with Tabbed Windows

1. Move your cursor over the Catalog Tab, just to the right side of the Data Frame.  Note that the Catalog Window expands.
2. Click on the Auto Hide Pushpin Icon at the top of the Catalog Window to ‘pin’ the window open.
3. Now, move your cursor over the Search Tab to expand the Search Window.
4. Click on the Auto Hide Pushpin Icon at the top of the Search Window to ‘pin’ the window open.
5. Using the Search Window’s Title Bar, Click and Drag the Search Window away from it’s docked position.  Note the ‘Docking Arrows’ that appear as you move the window.  
6. Drag the Search Window around to each of the Docking Arrows and note the effect on the blue Docking Preview rectangle.
7. Finally, drop the Search Window on the bottom Docking Arrow of the “Flower” that appears when you drag it over the Catalog Window.
###Explore the “Windows” (Catalog)

1. Using Windows Explorer, browse to the \Introduction to ArcGIS\EX01_World folder, where you extracted the EX01_World.zip file and browse into the EX01_World\Data Folder.

__Note that, while there are 23 files in this folder, there are actually only 3 Shapefiles and a DBF Table here, as far as ArcGIS is concerned.  This is because a Shapefile isn’t really a file but a collection of files.  You are looking at this folder in Windows Explorer in order to illustrate a very important point about many types of geographic data formats: Geographic datasets are often not easily manageable using software not specifically designed for handling GIS data.  In the case of the Shapefile, for example, if you wish to rename or move a shapefile, you must move or rename ALL of its component files in exactly the same way, or you can corrupt the shapefile.__
  
2. Return to ArcMap and right-click on the Folder Connections item in the Catalog Window and select Connect Folder. 
3. Select the Desktop icon at the top and click OK.
4. Expand the resulting Folder Connection in the Catalog Window, and then expand the Workshop Data Folder. 
Note that the Shapefile is much simplified in the ArcMap Catalog Window.  Although the Shapefile is still made up of several files, ArcMap seems to know that it’s not a good idea to make you deal with all that, so it simplifies things by only showing you the .shp file.  You can copy, paste, rename and many other “Explorer” tasks in Catalog without having to manage a half dozen or more files per dataset. 

###Finally, let’s open a Map Document!
You should, in addition to a Data Folder full of shapefiles, have a Map Document in your \Introduction to ArcGIS\EX01_World \EX01_World Folder called… EX01_World.mxd.  The extension is hidden in Catalog, but the icon looks like this:  

1. Drag the EX01_World Map Document into the Data Frame of ArcMap to open it. 
Take a look at the Change to the Top Level “Home” Folder in Catalog.  It has changed from the Application Default, to the Folder when the Map Document you are working with is stored. Handy, eh!? 

___But Wait!___
Has something gone awry? Do you see something that looks like this: 

You are experiencing the dreaded “Absolute Paths” problem, endemic to ArcMap. To fix this issue, do the following:

1. Right-click on one of the layers and select Data>Repair Data Source…
2. Browse into the Data Folder of the tutorial dataset and select the shapefile that corresponds to the layer you right-clicked. Click OK


You should find that (because they are all in the same ‘workspace’) all of your layers have been repaired and you should see something like the image on the right.
How to keep broken data links from happening…
Set Relative Paths (In Options)
Before explaining how to set the Relative Paths Option in ArcGIS, it is instructive to explain a bit more about what exactly a Map Document (.MXD) is, and is not.  When you open ArcMap and begin adding [with emphasis] datasets and creating symbologies, labeling schemes, etc…, you are creating a Map Document.  I emphasize the word “adding” here because you don’t really “add” data to a map document.  What you are really doing is linking to the datasets you are interested in.  Because you are sometimes working with datasets that are hundreds of megabytes, if not gigabytes, in size, it would be impractical to actually add the data to a map document.  So unlike, say, a Word Document, a Map Document doesn’t contain most of the objects that you add to it, but only links to them. 
This is where the distinction between Absolute and Relative Paths becomes critical, especially if you want to move your project from one machine to another, or keep it on some portable storage device.  By default, ArcGIS uses Absolute Paths to record the location of data that is referenced in a Map Document.  This means that if a Map Document in the folder C:\GIS refers to a dataset in the same folder, the map and dataset cannot be moved to ANY other location (even if they are moved together) without breaking the Map Document, since it will be looking for it’s data in the C:\GIS folder.  Setting ArcMap to save references to data as Relative Paths alleviates this problem.  In the case of the previous example, the Relative Path would discard the part of the data path that was identical to the path to the Map Document (in this case, the C:\GIS\ part), keeping only what was necessary to get from the Map Document  to the dataset.  This means that, as long as the Map Document and dataset remain in the same location relative to one another you can move the them without breaking the references to the data recorded in the Map document.  That is, you can move the entire GIS Folder (containing the Map Document and Dataset) to any other path, drive or machine and open the Map Document without issue.  While it is possible to set this option for individual Map Documents, it is really best to set the option for all Map Documents created with your installation of ArcGIS. 
1. On the Main Menu, go to Customize>ArcMap Options
2. Check the Option to “Make Relative Paths the default for new map documents”
3. Click OK


The Data Frame and its Properties 
Now take a look at the Table of Contents.  You should see a “Layers” item, followed by 3 Layers corresponding to the shapefiles in your Data Folder.  The “Layers” item at the top of the TOC represents the Data Frame, within which all of your layers are contained.  What you don’t see is that DBF Table, although it is actually included in the Map Document, too.  This is because you are currently looking at the “List by Drawing Order” view of the TOC.  Since the Table doesn’t have an explicit geographic component (it’s just a table of data), it isn’t shown in this view.
1. Click on the List By Source button (the second button from the left at the top of the TOC).
Note that the World_Population_2007 table is now listed at the bottom of the TOC. Note, also, that the layers are organized underneath the path at which they are located.  If this Map Document contained links to datasets in other locations, they would be listed under that path or network address.
Projections and Coordinate Systems in ArcMap

The datasets in this Map Document are all in the same Projection/Geographic Coordinate System, though it is not the one being used to display the data in the Data Frame, currently.  In ArcMap, datasets can (and in most cases, must) have their own explicitly defined Projection/Coordinate Systems, while the Data Frame can have a completely different Projection/Coordinate System.  This allows you to add geographic datasets with different Projection/Coordinate Systems to ArcMap, by treating the Data Frame’s Projection/Coordinate System as the Map Document’s Lingua Franca, projecting (on the fly) all of the datasets to the Data Frame Projection.  While this may seem convenient, it comes at a cost:  Map Documents that make use of this type of on-the-fly projection render the data in the Data Frame at a much slower rate than those in which the datasets and the Data Frame all share the same Projection/Coordinate Systems.  Additionally, disparate Projection/Coordinate Systems can cause major issues and errors when analyzing across layers such as in geoprocessing that requires overlay and transfer of attributes across layers.  For this reason, it is best to select a Projection/Coordinate System that is suitable for your particular analysis and geographic scale, and project all of your data to the same.
Change Coordinate System to GCS WGS 1984
1. Right-click on the Layers Item at the top of the Table of Contents and select Properties…
2. Click on the Coordinate system Tab and expand the Layers Folder in the “Select a Coordinate System:” panel.
3. Expand the Layers Folder and select the GCS_WGS_1984 Projection file.  Click OK.
4. Click Save 
What you have just done is reassigned the coordinate system of the Data Frame to that of the Cities Layer in your Map Document.  This (GCS WGS 1984) is actually the coordinate system of all of the layers in your Map Document, so you should experience an increase in drawing performance, since ArcMap is no longer projecting these layers on-the-fly to the World from Space projection (which was chosen for its extremity, in this case).  The result of this change should be a fairly substantial change to the view on the Data Frame.

Explore Navigations Tools and Visibility in Data Frames
Before we begin to explore the properties of individual layer in the Map Document, we will first spend some time getting familiar with the navigation tools in ArcMap.  Most of these tools can be found on the “Tools” toolbar, though some of the more useful ones involve right-click context menus of the layers.
Zoom to Layer
1. Right-click on the Lat_Lon_30 Layer, in the TOC, and select Zoom to Layer. 
Note that this should present you with the entirety of the Lat_Lon_30 Layer’s extent.
Tools Toolbar Navigation
The Tools Toolbar provides the bulk of the tools for navigation in the Data Frame.  Most of them are fairly obvious.  Take a moment to explore each of these tools, and how it works.
1.  The Zoom Tool works exactly as you would expect.  Click on the Zoom Tool, and drag a box to enclose the Continental United States. You can also single-click with this tool to use it as a Fixed Zoom Tool.
2.  The Zoom Out Tool isn’t quite as intuitive as the Zoom Tool.  Click on the Zoom Out Tool and Drag a Box over the State of Texas.  ArcMap will fit the current extent of the Data Frame into the box you just defined.  You can also single-click with this tool to use it as a Fixed Zoom Tool.
3.  The Pan Tool changes the Extent of your Data Frame, without changing the scale.  Click on the Pan Tool and use it to move around the Data Frame.
4.  The Full Extent Button zooms you to the full extent of the layer in your Map Document with the largest spatial extent.  This can sometimes be problematic if you are working at a local leve, but using one or more layers that are global in extent (for example, many of the network basemap services).
5.  The Fixed Zoom In Tool works as expected.  Click on the Fixed Zoom In Tool and take a look at the Scale Dropdown on the Standard Toolbar and note that the Fixed Zoom In Tool is tied to the Scale Values in this dropdown.
6.  The Fixed Zoom Out Tool works as expected.  Click on the Fixed Zoom Out Tool and take a look at the Scale Dropdown on the Standard Toolbar and note that the Fixed Zoom In Tool is tied to the Scale Values in this dropdown.
7.  The Back Button works much like its analogous tool in your browser, allowing you to step back through previous changes in Scale/Extent.  This tool is particularly useful if you change your Data Frame Extent inadvertently.
8.  Again, the Forward Tool is analogous to the browser forward button, stepping forward through the Scale/Extents in your project history.
Bookmarks
One of the most useful navigation tools is the ability to create spatial Bookmarks. 
1. Using the Zoom Tools on the Tools Toolbar, Zoom your Data Frame view to the European/Asian Landmass.
2. On the Main Menu, go to Bookmarks>Create…
3. Name your Bookmark “Europe & Asia” and click OK.
4. Click on the Full Extent Button .
5. Return to Main Menu>Bookmarks and select your Europe & Asia bookmark.
These can even be easily shared or moved from one Map Document to another, too.   Returning to the Bookmarks Menu item, you will find a Manage… option, which opens the Bookmark Manager.   This manager provided option for reordering, deleting, creating and saving your bookmarks, or selected subsets.  Bookmarks are saved as .dat files that can be loaded in other Map Documents.





Display Order
The Layer Order in the Table of Contents determines the order of display in your Data Frame, when it is in the List by Drawing Order Mode.
1. If you haven’t already, change your Table of Contents view from “List by Source” to “List by Drawing Order” using the View Buttons at the top of the Table of Contents.
2. Click and Drag the Lat_Lon_30 layer to the top of the Table of Contents.  Note that the other layers in your Map Document are now obscured.
Working with Layers & Their Properties
Layer Visibility
The Table of Contents also controls Layer Visibility.  You can toggle the Layer Visibility using the checkbox next to each Layer in the Table of Contents.
1. Use the Visibility Checkbox next to the Lat_Long_30 Layer to turn off the visibility of the layer and reveal the other layers again.
Examining and Selecting by Attributes
The most basic method of analysis in GIS is selection and sub-setting of data by attribute values.  Now that the Cities Layer is visible again, we can begin to address the fact that this layer is a bit overpopulated for our purposes.  Let’s say we are interested in visualizing the global distribution of cities with populations greater than or equal to 1 million.  First we need to see if the data necessary to do this exists in our dataset.
1. Right-Click on the Cities Layer and select “Open Attribute Table” to open the Attribute Table of the layer.
2. Click and Drag the resulting Table Window to the Docking Arrow at the bottom of the Data Frame so that it spans the entire width of the ArcMap Application Window.
3. Scroll to the right until you can see the POP, POP_RANK and POP_CLASS Attribute Fields
4. Right-click on the POP Field Header and select Sort Descending.
5. Scroll down through the Attribute table to examine the relationship between these three variables.
Selecting By Attributes
What we would like to do is select all of the cities in this dataset that have a population of 1 million or greater.  This can be accomplished using any one of these three of these variables, but we will use the POP_RANK variable for the sake of simplicity.  
1. On the Upper left corner of the Attribute Table, find the Select by Attributes button  and click on it.
2. Leave the Method: “Create a new selection”
3. Scroll through the list of Attribute Fields and Double-click on the “POP_RANK” value to place it into the SELECT Argument textbox, at the bottom of the window.
4. Click on the “<=” Button to enter the operator into the SELECT Argument.
5. With the “POP_RANK” value still highlighted in the Field List, click on the Get Unique Values button and double-click on 2 to complete the SELECT argument.
Note that you could also simply type any of the components of the SELECT argument, manually, using SQL syntax.
6. Click Apply and Close to apply the selection to your Cities Layer.
7. Scroll through the Attribute Table and note the records that are selected.
8. Unpin or close the Attribute Table so that you can observe that the selection from the Attribute Table is also reflected in the Data Frame.
Exporting Data
Notice that the Selection looks more manageable that the full dataset.  Now you will export this selection as a new shapefile, and bring it back into ArcMap as a new Layer.  As you do this, you will take advantage of a sort of “universal” in ArcMap.  Anytime you have selected a subset of one of your data layers ArcMap will only act on that subset while it is active.  This means that Geoprocessing, attribute calculations, data exports, etc… act as if the active selection is the whole of the dataset.  This can come in quite handy.
1. Right-click on the Cities Layer in the Table of Contents and select Data>Export Data…
2. Note that the Export: Default is Selected Features
3. Click on the Browse Button for the Output feature class.
4. Click on the Home Button and Browse into the Data Folder to save the Output Feature Class as Major_Cities.shp
5. Change the Save as type to Shapefile and Click Save and OK to Export the Selected Subset.
6. Click Yes when prompted to add the exported data as a layer in ArcMap.
7. Right-click on the original Cities Layer and select Remove.
Change City Symbology
Now we have two classes of POP_RANK to work with, and would like to distinguish them from one another, visually.
1. Right-Click on the new Major_Cities Layer and Open it’s Properties
2. Click on the Symbology Tab and Select Categories in the Show Options panel.
3. Change the Value Field to POP_CLASS and click on the Add All Values button.
4. Uncheck the <all other values> item and double-click on symbol to the left of the “1,000,000 to 4,999,999” item.
5. In the resulting Symbol Selector, select Circle 1 and change its size to 4 points. Click OK.
6. Using the same method, change the symbol for the “5,000,000 and greater” item to Circle 1 with a size of 10 points.
7. Click OK to close the Properties Window and commit the changes to symbology.
8. Click Save

Label Cities
Another property of the layers in our Map Document that we might want to enable is the labeling of features.  This can be accomplished, based upon an attribute value for each of the features.  In many cases, this might be the name, or some other identifying attribute of the feature, but in some cases it might be a quantitative value associated with the features.  It is even possible to use VB Scripting to assemble labels from several attributes and text elements.  In this example, we will label only the cities with a POP_RANK value of 1.
1. Right-Click on the Major_Cities Layer and select Label Features.
Note that this turns on labels for all features and, by ArcMap selects a field containing names, by default.  Because there are so many visible features in this layer, this creates an unreadable labeling scheme.  To remedy this, we will limit labeling to the largest cities in the Major Cities Layer.
2. Right-click on the Major_Cities Layer and select Properties.  Click on the Labels Tab.
3. Change the Method to “Define classes of features and label each class differently”
4. Click on the SQL Query… button.
5. In the SQL Query window, create a SELECT argument as follows:
“POP_RANK”=1
6. Click OK 
7. Change the Label Size to 12 points and Click OK to apply this labeling scheme to the Data Frame.

Join a Table to a Layer 
Now we will turn our attention to the World_Countries Layer.  Ultimately, we would like to visualize the layer based upon population density.  However, the attribute table for this layer doesn’t contain data on population.  Fortunately we have a table in our Map Document with the necessary population attribute.  
1. Change the Table of Contents to the List by Source view so that the World_Population_2007 Table is visible.
2. Right-click on the World_Population_2007 Table and select Open.
3. Scroll through the attributes and note the FIPS_CNTRY Attribute Field.  Close the table
4. Open the Attribute Table for the World_Countries Layer and note that it also has a FIPS_CNTRY Attribute Field.  
Since this attribute exists in both of these attribute tables, and its values are identical across the two datasets, we can use this attribute as the “Key Field” for our table join.
5. Close the Attribute Table for the World_Countries Layer.
6. Right Click on the World_Countries Layer and Select Joins and Relates>Join…
7. Select FIPS_CNTRY as the Join Field for the World_Countries Layer.
8. If it is not selected automatically, select World_Population_2007 as the Table to join to the World_Countries Layer, and FIPS_CNTRY as the Join Field for this table.
9. Click OK to create the Join.
10. Open the Attribute Table for the World_Countries Layer and note the POP2007 Attribute (along with all other attributes from the World_Population_2007 table).
Definition Querys
You may have noticed that many of the features in the World_Countries Layer had values of -99999 for the POP2007 attribute.  This normally indicates NODATA for the particular feature in demographic datasets.  In this case, we would like to exclude this value from our Map Document.  We could use the method used to subset the Cities layer earlier in the tutorial, but this time we will use another method called Definition Query.  Definition Queries “define” a dataset, based upon a SQL Query, like the ones we have used to create the selection by attributes and the labeling class.  In this case, the Definition Query “defines” a subset of the data layer that ArcMap treats as the entirety of the dataset.  It does not, however, require creating a new dataset (preventing redundancy in data storage) and does not alter the dataset being referenced, only our view of it in ArcMap.
1. Right-click the World_Countries Layer and open its Properties.
2. Click on the Definition Query Tab.
3. Click on the Query Builder Button and create a SELECT Argument as follows:

“World_Population_2007.POP2007”<>-99999

4. Click OK Twice to apply the Definition Query. 
5. Open the Attribute Table for the World_Countries Layer and note that the POP2007 Field no longer contains records with -99999 as a value.  
Because most of the features with this value are lesser countries (in terms of area) it may not be apparent that the corresponding geographic features have also been removed from the Layer, as well.

Symbolize Countries by Population Density
We can now use the POP2007 attribute to visualize population density.  Even though the POP2007 variable is a raw counts variable, we can use the Symbology Tabs Normalization capability to divide the POP2007 variable by the area of the features to create the density value on-the-fly.
1. Open the Properties for the World_Countries Layer and click on the Symbology Tab.
2. Select Quantities and set the Value to the POP2007 variable.
3. Set the Normalization Field to the SQMI field.
4. Click on the Classify… Button and set the Classification Method to Quantiles with 5 Classes. 
5. Click OK.
6. Select a Color Ramp and Click OK to apply the Symbology.
Note: When selecting your color ramp, be careful about selecting anything other than monochrome color ramps. This is because you want your map to “read well” in grayscale. In some of the 2-3 color ramps, the Intensity value of the colors at each end of the spectrum is the same, so that they produce identical grayscale values when converted, Xeroxed or printed in black & white.
Adding “Cloud” Data
Often, you will want to provide a cartographic basemap for your data in order to give it geographic context.  Cartographic design can be quite time consuming.  Fortunately, ArcMap leverages “Cloud” technologies to make a wide variety of pre-designed cartographic basemap layer available over the internet for use in your Map document.
1. On the Main Menu, go to File>Add Data>Add Basemap.
2. In the resulting window, select the “Oceans” basemap, and click Add.
3. Uncheck the Reference Layer that is added to the top of the Table of Contents.
4. Wait for the basemap to render and save your work.
Layout Mode
The Layout Mode Navigation Tools
1. Using the View Toolbar at the bottom left corner of the Data Frame, switch to Layout Mode.
Note that the Layout Toolbar is now active and that many of the tools on this toolbar look similar to those on the Tools Toolbar, with one very important difference.  Now that you are in Layout Mode, your view has changes so that your Data Frame is now superimposed upon piece of paper (the size of which is determined by the default printer paper size for the printer connected to your machine).  The tools on Tools Toolbar act (as they did in the Data View) within the Data Frame, while the analogous tools on the Layout Toolbar act upon the Page Layout (without effecting the Data Frame extent or scale). 
2. Take a moment to explore the differences between how the Layout Toolbar behaviors differ from the Tools Toolbar navigation tools. 
Resize Data Frame
For the time being, we will not concern ourselves with the Page Orientation of our Map Document.  In this case, we will assume we are creating a map image, not for printing, but for inclusion in a Word Document or Presentation.  In that case, we will want to alter the size of the Data Frame to the size we desire for our final image.
1. Right-click on the Layers item at the top of the Table of Contents and open the Properties for the Data Frame.
2. Click on the Size and Position Tab and set the Frame Size as 7 in wide by 4 in.
3. Click on the Frame Tab and set the Border weight to 4 points.  
4. Assign a Gap of 10 pts for both the X and Y axes. 
5. Click OK to apply the changes
6. On the Main Menu, go to Bookmarks and select your Europe & Asia bookmark
7. Use the Tools Toolbar navigation tools to zoom and pan until Africa and the Eurasian continents fill the Data Frame. 
Adding Map Elements
Legend
1. On the Main Menu, go to Insert>Legend
2. Select and remove all EXCEPT the Major_Cities and World_Countries layers from the Legend Items list and click Next> twice.
3. Give the Legend a Border and Background (white is a good choice).
4. Click Next> to accept all remaining default settings and insert the Legend.
5. Use the Select Elements Tool to resize and reposition the Legend using the blue resize handles.
6. Click once on the Major_Cities Layer, wait a few seconds, and then click again to highlight the Layer Name for Editing.  Rename the Layer “Major Cities” removing the underscore, and hit the Enter key to commit the change.
Note that the change you have made to the name of the Layer is also reflected in the Legend.
7. Make changes to the other Text Elements of your Layers so that your Legend contains properly formatted and reasonable text descriptions and labels.



Scale Bar
1. On the Main Menu, go to Insert>Scale Bar
2. Select Scale Line 1 from the Scale Bar Selector and click on the Properties Button.
3. Set the Number of Divisions to 1 and the Subdivisions to 0.
4. Change the Division Units to Miles.
5. Click on the Numbers and Marks Tab.
6. Set the Numbers and Marks Frequencies to “ends (and zero)”
7. Click OK twice to add the scale bar to the Map Layout.
8. Use the Select Elements Tool to resize and reposition the Scale Bar.
Neat Line
1. On the Main Menu, go to Insert>Neatline.
2. Be sure that the “Place around all elements” option is checked.
3. Set the Border Size to 4 points.
4. Click OK to add the neatline.
Exporting Your Map
1. Save your Work.
2. On the Main Menu, go to File>Export Map…
3. Click on the Home Button to browse to the Workshop Folder.
4. Change the Save as type to PNG(*.png)
5. Change the Resolution to 200 dpi
6. Check the option to “Clip Output to Graphics Extent”
7. Click Save.
8. Browse to the Workshop Folder and double click on the EX01_World.png file to view it in the default image viewer.
