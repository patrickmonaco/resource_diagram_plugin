# resource_diagram_plugin
An Oracle APEX plugin which displays data as a VIS timeline resource diagram
cf http://visjs.org/docs/timeline/

"The VIS Timeline module is an interactive visualization chart to visualize data in time. The data items can take place on a single date, or have a start and end date (a range). You can freely move and zoom in the timeline by dragging and scrolling in the Timeline. Items can be created, edited, and deleted in the timeline. The time scale on the axis is adjusted automatically, and supports scales ranging from milliseconds to years."

## Usage
Import this plugin
In any page, add a new region based on "Resource Diagram plugin"
Then, provide the following informations:
- a regular query which must return:
   - resource name
   - start date (DATE datatype only)
   - task name
   - End_date (optionnaly)

- Group name column
- Task name column
- Start Date column

## Edit Mode
If the edit mode is set, this gives opportunity to call a detail page.
In this case, the plugin passes some contextual parameters and the target fields must be set:
- Id field
- Resource field
- start date field
- date format which is in use in the detail page (ie: MM-DD-YYYY HH24:MI:SS)

For the resource field, it's possible to pass an internal column name instead the label of resource name.

After applying changes on the detail page and once the modal window is closed, the diagram is automatically refreshed in order to reflect the actual values from database.

Each time a user double clicks on a task or move it in an another lane or time slot, the plugin triggers the detail page (cf above).
If a double click occurs in a blank area of the diagramm, a detail page in displayed with only the resource name filled.

## Limitations

Doesn't work with TIMESTAMP datatype, yet
It will be added soon. 

- VIS.js module will be in end of life status as of March 2019.
https://github.com/almende/vis/issues/4259

