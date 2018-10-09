## Localization (i18n + l10n)

DBeaver uses standard properties-based i18n model.
All translatable resources reside in *.properties file. Each plugin (bundle) has its own set of resources.
Almost all plugins have at least `bundles.properties` resource. Bigger plugins have additional resources in src folder.
See full list of property files below.

bundle.properties contains original string in English language.
All translated resources are placed in bundle_XX.properties files where XX is two-letter language code.

### Localizing tools
#### Eclipse IDE
https://marketplace.eclipse.org/content/properties-editor-java-i18n-tool

#### Intellij IDEA Community

#### Other tools 

### Properties

Module|Purpose|File
---|---|---
Core| Commands, properties | [[https://github.com/dbeaver/dbeaver/tree/devel/plugins/org.jkiss.dbeaver.core/OSGI-INF/l10n/bundle.properties]]
Core|Messages,UI strings | [[https://github.com/dbeaver/dbeaver/tree/devel/plugins/org.jkiss.dbeaver.core/src/org/jkiss/dbeaver/core/CoreResources.properties]]
