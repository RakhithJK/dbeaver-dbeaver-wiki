
### Command line parameters

Option | Meaning
---|---
`-Ddbeaver.debug.skip-version-check=true` | Disable new version release check.<br>Always shows new version update dialog 
`-Ddbeaver.debug.override-product-version=major.minor.micro` | Override current product version.<br>Used only for version update dialog
`-Ddbeaver.debug.disable-data-transfer-settings-save=true` | Cancels export data transfer format specific settings saving. Like `Header position` for CSV or `Keyword case` for SQL export.<br>Can be used for UI tests.
`-Ddbeaver.trace.enabled=true` | Enable additional log level for printing _finest_ messages