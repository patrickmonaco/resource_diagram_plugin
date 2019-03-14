# resource_diagram_plugin
An Oracle APEX plugin which displays data as a VIS timeline resource diagram
cf http://visjs.org/docs/timeline/
"The VIS Timeline module is an interactive visualization chart to visualize data in time. The data items can take place on a single date, or have a start and end date (a range). You can freely move and zoom in the timeline by dragging and scrolling in the Timeline. Items can be created, edited, and deleted in the timeline. The time scale on the axis is adjusted automatically, and supports scales ranging from milliseconds to years."

## Usage
Import this plugin
In any page, add a new region based on "Resource Diagram plugin"
provide the following informations:
a regular query which must return:
   resource name
   start date
   task name
  
  and optionnaly:
  an end_date
