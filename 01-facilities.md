

```
method: "nayar.net4machines.facilities.get"
parameters:
    {
        id: <string, optional>,
        pager: <map[string], optional>,
    }
return: list
description: returns a list of the owner facilities, can be paged, if "id" is provided returns the specific facility.
```


```
method: "nayar.net4machines.facilities.get_tree"
parameters:
    {
        id: <string>
    }
return: map[string]interface{}
description: returns a map with the forest representation of the facility
```


```
method: "nayar.net4machines.facilities.stats"
parameters:
    {}
return: map[string]interface{}
description: returns a map with the summary of every facility owned by the user
```


```
method: "nayar.net4machines.facilities.obelisk.getfacility"
parameters:
    {

    }
return: map[string]interface{}
description: returns a map with the summary of every facility owned by the user
```

method: "nayar.net4machines.facilities.element.stats"
parameters:
    {

    }
return: map[string]interface{}
description: returns a map with the summary of the total elements