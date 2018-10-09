## Localization (i18n + l10n)

DBeaver uses standard properties-based i18n model.
All translatable resources reside in *.properties file. Each plugin (bundle) has its own set of resources.
Almost all plugins have at least `bundles.properties` resource. Bigger plugins have additional resources in src folder.
See full list of property files below.

bundle.properties contains original string in English language.
All translated resources are placed in bundle_XX.properties files where XX is two-letter language code.

### Localizing tools
#### Eclipse IDE
- Clone DBeaver repository
- Install Eclipse (any version, any package)
- Install [[ResourceBundle Editor|http://essiembre.github.io/eclipse-rbe/]] plugin.
  - `Install New Software` from this URL: https://raw.githubusercontent.com/essiembre/eclipse-rbe/master/eclipse-rbe-update-site/site.xml
- Import all DBeaver plugins in workspace
- Open some properties file (e.g. bundle.properties) in ResourceBundle editor:
![Open resource in Properties Editor](images/ug/Open-Properties-Bundle.png)
- Edit properties:
![](images/ug/Localize-Bundle-Editor.png)

#### Intellij IDEA Community
![](images/ug/Localize-Bundle-IDEA.png)

#### Other tools 

### Push your changes

Create a Pull Request with your changes (in branch `devel`)
https://help.github.com/articles/creating-a-pull-request-from-a-fork/

### Properties

Module|Purpose|File
---|---|---
Core| Commands, properties | [[https://github.com/dbeaver/dbeaver/tree/devel/plugins/org.jkiss.dbeaver.core/OSGI-INF/l10n/bundle.properties]]
Core|Messages,UI strings | [[https://github.com/dbeaver/dbeaver/tree/devel/plugins/org.jkiss.dbeaver.core/src/org/jkiss/dbeaver/core/CoreResources.properties]]
