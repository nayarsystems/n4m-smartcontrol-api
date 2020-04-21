# Introduction

This is an example of request to our API for Smart Control:

```
curl -X POST --data '{"jsonrpc":"2.0","id":1,"method": "task.push", "params":{"method":"nayar.net4machines.facilities.get","params":true}}' http://x.x.x.x:xxxx -u "user:pass"
```


Also available an access with API_KEY


The common objects of our API are listed below:



```
Facilities:

type Facility struct {
	ID             bson.ObjectId `bson:"_id" js:"-" json:"_id"`
	Revision       int
	Owner          string
	Reference      string
	Address        string
	Coordinates    *Coordinates
	ObeliskDevices []ObeliskDevice `bson:"obelisk_devices"`
	Elements       []Element
	Alerts         []Alert

	TemporalOwner *TemporalOwner `bson:"temporal_owner"`

	DiscardedAlerts map[string]int `bson:"discarded_alerts"`
}


Devices (Obelisk):

type ObeliskDevice struct {
	ID          string `js:"-" json:"id"`
	Reference   string
	Phone       string
	Battery     float64
	Coverage    float64
	Consumption float64
	LastUpdated *time.Time
}


Elements:

type Element struct {
	ID         bson.ObjectId `js:"-" json:"id"`
	Reference  string
	Type       string
	Model      string
	Parameters interface{}
	Inactive   bool
}


Events:

type Event struct {
	ID         bson.ObjectId `bson:"_id" js:"-" json:"_id"`
	Date       time.Time     `bson:"date" json:"date"`
	OriginID   OriginID
	Name       string               `bson:"name" json:"name"`
	SubElement string               `bson:"sub_element" json:"sub_element"`
	Data       map[string][]float64 `bson:"data" json:"data"`
	Log        interface{}          `bson:"log" json:"log"`

	ConsolidatedData map[string][]*float64 `bson:"-" json:"consolidated_data"`
}


Alerts:

type Alert struct {
	ID       bson.ObjectId `bson:"_id" js:"-" json:"_id"`
	OriginID OriginID
	Date     time.Time
	Message  map[string]interface{}
	Content  AlertContent
}
```