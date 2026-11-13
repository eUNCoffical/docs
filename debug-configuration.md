# Debug Configuration

eUNC provides configuration options for controlling certain benchmark output and execution behavior.

Configuration is supplied through the eUNCDebug table.

## Example Configuration

```lua
getgenv().eUNCDebug = {
    ["printcheckpoints"] = false,
    ["delaybetweentests"] = 0,
    ["printtesttimetaken"] = false,
    ["savetodevice"] = false,
}
```

Load the benchmark after configuring the table.

## Options

### printcheckpoints

Controls checkpoint-related output when supported by the benchmark version.

### delaybetweentests

Controls the delay between tests.

The value is expressed in seconds.

A value of 0 disables the configured delay.

### printtesttimetaken

Controls whether individual test execution times are displayed.

### savetodevice

Enables saving the benchmark report to a local file.

When enabled, eUNC attempts to save:

```
eUNC-results.json
```

The executor must provide a compatible writefile function.

The report also requires JSON encoding support.

If either requirement is unavailable, the report cannot be exported successfully.

## Example: Save Results

```lua
getgenv().eUNCDebug = {
    ["printcheckpoints"] = false,
    ["delaybetweentests"] = 0,
    ["printtesttimetaken"] = true,
    ["savetodevice"] = true,
}

loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/EnhancedUNC/eUNC/main/src/main.lua"
))()
```

## Compatibility

Configuration options may change between versions.

Always check the configuration supported by the version you are using.