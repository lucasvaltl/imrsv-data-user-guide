# imrsv.data User Manual

imrsv.data was built from the start to allow the anyone to visualise data in 3-dimensions. As such, we hope that it helps you understand and find patterns in your data.The app itself was made to be self-explanatory, however here are some tips to get you started.

<p class="warning">
 
**Important:** The app is only useable if you have a filepicker installed on your Hololens. [OneDrive](https://www.microsoft.com/en-gb/store/p/onedrive/9wzdncrfj1p3?wa=wsignin1.0) is a great choice.

</p>


### Accepted File Formats

Missing data values should be left empty. The following file formats are accepted:
- CSV: files using commas as separators will work. Do not use an index. The first line defines the column names and hence needs to consist of strings. [Here](https://1drv.ms/u/s!ArSq-hTe1BlYgQtmPZfea8iSWcj-) is an example.
- JSON: the file needs to be formatted as follows: one key/value pair per data column/dimension containing the column name as the key and an array of data as the value. All dimensions/columns need to have the same length and the values need to be of the same type. [Here](https://1drv.ms/u/s!ArSq-hTe1BlYgQ0YYcdVFaJA97SW) is an example. 

<p class="tip">
Side note: Files exported using the pandas [`pandas.DataFrame.to_json`](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.to_json.html) method without any parameters can be used. 
</p>

### Application Start
The application welcomes you with a screen that prompts you to load a file. Upon pressing the load file button, the app will switch to the file picker installed on your device. Choose the file you want to load and press "open".

### Placing The Graph

As soon as you select a file you will be able to place the graph anywhere in the room. The graph will then appear at that exact location. Placement will look like this:

![UI](https://github.com/lucasvaltl/imrsv.data-documentation/raw/master/TapToPlaceScreenshot.jpg?raw=true "UI")

### Visualising Data

As soon as you place the graph, your data will be plotted. It may look like this:

![UI](https://github.com/lucasvaltl/imrsv.data-documentation/raw/master/GraphScreenshot.png?raw=true "UI")

### Data Manipulation

You can now manipulate the dimensions being displayed using the UI that was created based on the headers of the data you loaded. The UI is made of three main sections:

![UI](https://github.com/lucasvaltl/imrsv.data-documentation/raw/master/UIScreenshot.png?raw=true "UI")

- The leftmost section controls how your data is grouped. The data will be grouped along this dimension - think of it like the x axis of your graph.
- The middle section allows you to add a secondary / sub-grouping category. Each group created will be sub-grouped using this dimension. Sub-groups are displayed as tip-tools when gazing at a data point. 
- The rightmost section allows you to select the dimensions that are displayed. You can choose which dimensions are displayed and how they are aggregated by clicking the `Count`, `Sum` and `Avg` buttons. Pressing any button visualises the corresponding dimension, and pressing it again deletes said dimension from the visualisation. 

Use these buttons to change how and which data is being displayed - then walk around the graph to see it from different angles. This will hopefully allow you to understand the data better and find new patterns between different dimensions.

### Changing The Data Loaded

To change the data you are visualising, just press the `Load Data` button at the top of the UI panel. The app will switch to your file picker and you can select a different data set to visualise. 
