# About
SimpleConfig is a config system for Java to locally store values resource- and user-friendly.

# How To Use
```
import de.keksuccino.config.*;

public static Config config;

//Can also be used to update the config after changing values in the config file by hand.
public static void initConfig() {

   config = new Config("path/to/config.cfg");

   config.registerValue("valuename", true, "category", "A description for this value.");
   config.registerValue("another_value", "string value", "category");

   config.syncConfig();

   config.clearUnusedValues();

}

public static String getValue() {
   return config.getOrDefault("another_value", "default value to return if value not found");
}
```

# Licensing
SimpleConfig is licensed under MIT.<br>
See LICENSE.md for more information.

# Copyright
- SimpleConfig<br>
Copyright (c) 2020 Keksuccino
