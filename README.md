## Demo

You can see this in action at https://radar.thoughtworks.com. If you plug in [this data](https://docs.google.com/spreadsheets/d/18A7oDuavlh89rAmqcaXpqle8QLqIvlAkoEUxcObzuUM/edit#gid=1985253373) you'll see [this visualization](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fdocs.google.com%2Fspreadsheets%2Fd%2F18A7oDuavlh89rAmqcaXpqle8QLqIvlAkoEUxcObzuUM%2Fedit%23gid%3D1985253373). 

## How To Use

The easiest way to use the app out of the box is to provide a *public* Google Sheet ID from which all the data will be fetched. You can enter that ID into the input field on the first page of the application, and your radar will be generated. The data must conform to the format below for the radar to be generated correctly.

### Setting up your data

You need to make your data public in a form we can digest.

Create a Google Sheet. Give it at least the below column headers, and put in the content that you want:

| name          | ring   | quadrant               | isNew | description                                             |
|---------------|--------|------------------------|-------|---------------------------------------------------------|
| Composer      | adopt  | tools                  | TRUE  | Although the idea of dependency management ...          |
| Canary builds | trial  | techniques             | FALSE | Many projects have external code dependencies ...       |
| Apache Kylin  | assess | platforms              | TRUE  | Apache Kylin is an open source analytics solution ...   |
| JSF           | hold   | languages & frameworks | FALSE | We continue to see teams run into trouble using JSF ... |

### Sharing the sheet

* In Google sheets, go to 'File', choose 'Publish to the web...' and then click 'Publish'.
* Close the 'Publish to the web' dialog.
* Copy the URL of your editable sheet from the browser (Don't worry, this does not share the editable version). 

The URL will be similar to [https://docs.google.com/spreadsheets/d/1waDG0_W3-yNiAaUfxcZhTKvl7AUCgXwQw8mdPjCz86U/edit](https://docs.google.com/spreadsheets/d/1waDG0_W3-yNiAaUfxcZhTKvl7AUCgXwQw8mdPjCz86U/edit). In theory we are only interested in the part between '/d/' and '/edit' but you can use the whole URL if you want.

### Using CSV data
The other way to provide your data is using CSV document format.
You can enter any URL that responds CSV data into the input field on the first page.
The format is just the same as that of the Google Sheet, the example is as follows:

```
name,ring,quadrant,isNew,description  
Composer,adopt,tools,TRUE,"Although the idea of dependency management ..."  
Canary builds,trial,techniques,FALSE,"Many projects have external code dependencies ..."  
Apache Kylin,assess,platforms,TRUE,"Apache Kylin is an open source analytics solution ..."  
JSF,hold,languages & frameworks,FALSE,"We continue to see teams run into trouble using JSF ..."  
```

***Note:*** The CSV file parsing is using D3 library, so consult the D3 documentation for the data format details.

### Building the radar

Paste the URL in the input field on the home page.

That's it!

***Note:*** The quadrants of the radar, and the order of the rings inside the radar will be drawn in the order they appear in your data.

Check [this page](https://www.thoughtworks.com/radar/how-to-byor) for step by step guidance.


