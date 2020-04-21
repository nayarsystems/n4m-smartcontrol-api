# Devices


This command allows various actions to be performed on the specified GSR device.
Commands like `sys.cmd.restart` are used to restart the device.
The `report.cmd.generate` command generates a report from the GSR device.

```
method: "nayar.net4machines.permissions.device.rpc": true
parameters:
    {
		"device_id" <string>: Device ID
		"path"      <string>: Command (e.g. sys.cmd.restart)
		"value"     <string>: Value of the command
		"type"      <string>: Type of input (e.g. str)
		"timeout"   <int>: Action timeout (default to 100) 
	}
return: map[string]interface{}
description: this command allows executing actions from the GSR device
```
