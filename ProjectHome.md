| 

&lt;IMG src="http://cache.smarthome.com/images/2412n.jpg/&gt;

  |
|:-------------------------------------------------------------------|
# Introduction #

The SmartLinc controller, from SmartHome, is an HTTP based controller used to control Insteon devices. This library was created to allow Java programmers to easily develop code in minutes to turn light switches on and off. 




# Examples #

**Turn Light On**
```

// Get the HTTP Client
HTTPCommandClient client = new HTTPCommandClient();

// Get a command builder instance
SmartLincCommandBuilder slcb = new SmartLincCommandBuilder("10.1.10.25", 80);

// Build the command
String command = slcb.getStandardCommand(
                    "111111", 
                    CommandType.STANDARD_COMMAND, 
                    LightCommand.ON, 
                    LightLevel.LEVEL100);

// Send the command
String sentResponse = client.sendCommand(command);

```