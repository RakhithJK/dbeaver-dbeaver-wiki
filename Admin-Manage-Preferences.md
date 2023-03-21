This guide describes a way to set up application preferences through configuration files without even booting it up.

### Locating preference files

Preference files have the extension `.prefs` and can be found in the [workspace](Workspace-Location) directory under the
following path:
`.metadata/.plugins/org.eclipse.core.runtime/.settings`

You might not find a preference file you're interested in if it hasn't been created yet. In that case, you will need to
create one yourself. See the examples below to figure out which preference file you need.

### Reading and modifying preference files

Preference files consist of key-value pairs glued together with `=` and separated with a line break:

```properties
# file org.jkiss.dbeaver.test.prefs
some.key=value1
some.other.key=value2
```

### Configuring default navigator view for new connections

You can place the following preferences in the `org.jkiss.dbeaver.core.prefs` file:

|Name|Type|Default Value|Allowed Values|Description|
|----|----|-------------|--------------|-----------|
|`navigator.settings.default.preset`|string|`simple`|`simple`, `advanced`, `custom`|Sets the default view mode for new connections|
|`navigator.settings.default.showSystemObjects`|boolean|N/A|`true`, `false`|Controls whether system objects must be shown.<br>Used if preset is set to `custom`.|
|`navigator.settings.default.showUtilityObjects`|boolean|N/A|`true`, `false`|Controls whether utility objects must be shown.<br>Used if preset is set to `custom`.|
|`navigator.settings.default.showOnlyEntities`|boolean|N/A|`true`, `false`|Controls whether only schemas and tables must be shown.<br>Used if preset is set to `custom`.|
|`navigator.settings.default.mergeEntities`|boolean|N/A|`true`, `false`|Controls whether all tables must be shown in a single list.<br>Used if preset is set to `custom`.|

For more information, please see [Simple and Advanced View](Simple-and-Advanced-View).