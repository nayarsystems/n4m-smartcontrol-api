[Index](./README.md)

# Facilities

```
method: "nayar.net4machines.facilities.get"
parameters:
    {
        "id" <string, optional>: Facility ID,
        "pager" <map[string], optional>,
    }
return: list[]: Contains facilities
description: returns a list of the owner facilities, can be paged, if "id" is provided returns the specific facility.
```


```
method: "nayar.net4machines.facilities.get_tree"
parameters:
    {
        "id" <string>: Facility ID
    }
return: map[string]interface{
    "forest": Multiple facility trees of the instalation
    "unlinked": Unlinked elements of the instalation
}
description: returns a map with the forest representation of the facility
```

An example of facility tree representation would be the following:
![Facility tree](/images/facility-tree.png "Facility tree t 1")


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
        "obelisk_id" <string>: Device ID
    }
return: map[string]interface{}
description: returns a map with the facility associated to the specific device
```

Next: [Element](./02-elements.md)