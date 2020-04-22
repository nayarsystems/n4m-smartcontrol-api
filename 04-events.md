[Index](./README.md)

# Events


```
method: "nayar.net4machines.events.get"
parameters:
    {
	    "id" <string, optional>: Event ID,
        "facility_id" <string>: Facility ID,
	    "obelisk_id" <string>: Device ID,
        "element_id" <string>: Element ID,
	    "page_size" <string, optional>: Size of every page,
        "page_num" <string, optional>: Current page number,
        "sub_element" <string, optional>
	    "time_start" <date>: Initial date,
        "time_end" <date>: End date,
	    "event_name" <string>: Type of event,
    }
return: map[string]interface{
    "events"
    "total"
    "types"
    "sub_elements"
}
description: returns a map containing information about the events within the selected time range
```

```
method: "nayar.net4machines.events.consolidate"
parameters:
    {
	    "template_id" <string>: Template ID,
        "facility_id" <string>: Facility ID,
	    "obelisk_id" <string>: Device ID,
        "element_id" <string>: Element ID,
        "sub_element" <string, optional>
	    "time_start" <date>: Initial date,
        "time_end" <date>: End date,
	    "event_name" <string>: Type of event,	
    }
return: map[string]interface{
    "name"
    "sub_element"
    "data"
    "log"`
	"consolidated_data"`
}
description: consolidate is a process that merges the selected events into one
```

```
method: "nayar.net4machines.alerts.get"
parameters:
    {
	    "facility_id" <string>: Facility ID,
        "obelisk_id" <string>: Device ID,
	    "element_id" <string>: Element ID,
        "type" <string, optional>: Alert type,
	    "page_size" <string, optional>: Size of every page,
        "page_num" <string, optional>: Current page number,
    }
return: map[string]interface{
    "alerts"
    "total"
}
description: returns a list of validated alerts, paginated
```


```
method: "nayar.net4machines.alerts.stats"
parameters:
    {}
return: map[string]interface{}
description: returns an overview of the validated alerts status
```


```
method: "nayar.net4machines.alerts.pending_stats"
parameters:
    {

    }
return: map[string]interface{}
description: returns an overview of the pending alerts status
```