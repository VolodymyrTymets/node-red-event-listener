event-listener
==============

event-listener

## About
Test node-red event listener
## Install
> first make sure that you have installed node-red

`npm ryn start`

#### Task 1  
New Record Event
The user would like to define a workflow in the nodeRED UI that accomplish the following task:


After a record was created wait for 5 minutes. Afterwards get the Process value (GET /Processes/<id>/value) for the fieldId urn:service-manager:record:vars.datum_bescheid and perform a filter on the date result. If the date is <= (today - 1 month) perform a update action with the post data {"value": "lead_only" to the Process resource (PATCH /Processes/<id>/value). To get the Process find one with the filter fieldD=urn:service-manager:record:vars.lead_to_conversion and foreignKey=<recordId>.

![](https://github.com/VolodymyrTymets/node-red-event-listener/blob/origin/private/event-listener-task-1.gif?raw=true)

#### Task 2  
Scheduled Job
The user would like to define a workflow in the nodeRED UI that accomplish the following task:

Every day at 11 pm the workflow should be triggered automatically. The workflow should filter all Processes for the fieldId=urn:service-manager:record:vars.lead_to_conversion and remak=unterlagen_fehlen and record.createdAt < today -1 month. For all these Processes the workflow should set the value of the urn:service-manager:record:vars.lead_to_conversion Process to {"value": "tot" }

![](https://github.com/VolodymyrTymets/node-red-event-listener/blob/origin/private/event-listener-task-2.gif?raw=true)
