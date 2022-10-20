You can install a lot of optional extensions (plugins) in DBeaver.
Most of the extensions can be found on the [Eclipse Marketplace](https://marketplace.eclipse.org/) website.

## DBeaver-specific extensions
- [Office formats support (XLSX)](https://marketplace.eclipse.org/content/dbeaver-office-integration)
- [Vector graphics support (SVG)](https://marketplace.eclipse.org/content/dbeaver-svg-support)
- SSHJ and advanced cryptography (since version 21 it is included in the base distribution)
- [Git support](https://marketplace.eclipse.org/content/dbeaver-git-support) - Git version control integration
- [SQL debugger](https://marketplace.eclipse.org/content/dbeaver-sql-debugger)

## Popular 3rd party extensions for Eclipse and DBeaver

- [Darkest Dark theme](https://marketplace.eclipse.org/content/darkest-dark-theme-devstyle) - the best Dark theme for DBeaver
- [Eclipse Color Theme](https://marketplace.eclipse.org/content/eclipse-color-theme) - if for some reason you do not like the Darkest Dark theme, you can use this one
- [Subversion support](https://marketplace.eclipse.org/content/subclipse) - Subversion integration
- [Embedded Shell](https://marketplace.eclipse.org/content/easyshell) - Allows you to run shell commands directly from DBeaver
- [Editor vertical indents](https://marketplace.eclipse.org/content/indent-guide) - Adds vertical indents to all text editors


# Install Process

In DBeaver EE you can use drag-n-drop from the Marketplace web site (see button `Install`) in the DBeaver main window. This will launch the Marketplace installation wizard automatically.
In the DBeaver Community or other DBeaver-based products which do not include marketplace clients, you can use the following instructions:

## Extension installation in CE version:

1. Copy URL of extension update site:
![](images/marketplace/copy-p2-url.png)
1. In the DBeaver main menu open `Help -> Install New Software`
1. Paste update site URL into `Work with` field and press <kbd>Enter</kbd>
1. Check items you wish to install (in most cases just all items)
![](images/marketplace/install-new-software.png)
1. Click Next. You may need to accept the extension license before installing
![](images/marketplace/accept-license.png)
1. Some extensions may contain unsigned bundles. Only install such extensions if you really trust the author.
![](images/marketplace/unisgned-bundles.png)
1. Click Next->Finish. The installation will take some time. Restart DBeaver.
