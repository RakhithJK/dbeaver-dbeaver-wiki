DBeaver offers you the ability to use most of its features with a keyboard and screen readers. Here you will find guidelines on how to use DBeaver without a mouse in some common cases.


**Note: DBeaver is tested mainly for use with NVDA screen reader and Windows keyboard shortcuts.**

### Table of contents:
- [General](#general)
  - [Structure and navigation](#structure-and-navigation)
  - [Shortcuts](#shortcuts)
  - [Colors and fonts](#colors-and-fonts)
- [Views and Wizards](#views-and-wizards)
  - [Database Navigator](#database-navigator)
  - [New Connection](#new-connection)
  - [Object Properties](#object-properties)
  - [SQL Editor](#sql-editor)
  - [Result Set](#result-set)
  - [ER Diagrams](#er-diagrams)

## General


### Structure and navigation

DBeaver is an application consisting of many parts, so-called Views, such as [**Database Navigator**](Database-Navigator), [**SQL Editor**](SQL-Editor), [**Data Editor**](Data-Editor), etc.
A [**Toolbar**](Application-Window-Overview#toolbar) with many buttons inside each [**View**](Application-Window-Overview#workspace-views-and-editors) and horizontal and vertical tabs allows you to switch between **Views** and inside them.

**Main navigation shortcuts**
- You can switch Views by using <kbd>Ctrl</kbd>+<kbd>F7</kbd> | <kbd>⌘F7</kbd>.
- You can switch between buttons on the toolbars and menus using **Tab** and the **arrows**.

**How to switch tabs**
 - You can switch horizontal tabs by using <kbd>Ctrl</kbd>+<kbd>PageUp</kbd>/<kbd>PageDown</kbd>.
 - Sub-tabs can be switched by using <kbd>Alt</kbd>+<kbd>PageUp</kbd>/<kbd>PageDown</kbd>.
 - If there are vertical tabs inside the view, you can switch them by using <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>PageUP</kbd>/<kbd>PageDown</kbd>.

When you focus on any interface object, such as a table, column, tab, or cell, you can open the **Context menu** to see all the actions available for that object.

To open the Context menu, use <kbd>Shift</kbd> + <kbd>F10</kbd> | <kbd>⇧F10</kbd>.

### Shortcuts

Most of DBeaver's functions are accessible through special shortcuts. You can find them in **Window -> Preferences –> User Interface –> Keys**. If you mostly use the keyboard, you can switch to the **DBeaver Keyboard Only** scheme, which has additional shortcuts.

[Learn more DBeaver shortcuts](Shortcuts)

### Colors and fonts

**Themes**: If you need a high-contrast theme, the [Darkest Dark theme](https://marketplace.eclipse.org/content/darkest-dark-theme-devstyle) is the best one to use. You can [install it from the Eclipse Marketplace](Eclipse-extensions#install-process). You can also choose from three available color schemes in DBeaver: Classic, Light, or Dark. To select one of them, navigate to **Window -> Preferences –> User Interface –> Appearance**, and select **Enable theming**.

**Fonts**: To change fonts in DBeaver, navigate to **Window -> Preferences –> User Interface —> Appearance —> Color and fonts**, and open DBeaver fonts. The **Main font** allows you to change the font family, size, and color in most elements of DBeaver's interface, including the **Database Navigator** and the **Data Grid**. The Monospace font changes the font in the **SQL Editor** and other **Views** with monospaced fonts.

**Data Colorization**: You can [color rows in the **Data Grid**](Data-View-and-Format#rows-coloring) by following some rules or even by [selecting colors for particular data types](Data-View-and-Format#coloring-by-data-types).

## DBeaver Views and Wizards

Let's see some comments on using the most popular **Views** in DBeaver with the keyboard and screen reader.

### Database Navigator

In the **Database Navigator**, you can view and open all the database connections and objects inside them. You can move between database objects and open nodes using arrows.

 - To view object properties, use <kbd>F4</kbd>.
 - To open **SQL Editor** associated with the selected object, use <kbd>F3</kbd>.

[See all **Database Navigator** shortcuts](Shortcuts#database-navigator)

### New Connection

To [create a new connection](Create-Connection), open the **Wizard window** using <kbd>Ctrl+N</kbd> | <kbd>⌘N</kbd>, then type **connect** and select **Database connection**.

[See **Connection** shortcuts](Shortcuts#connection)


### Object Properties

The [**Properties Editor**](Properties-Editor) is used to see all the information about database objects. When you focus on the first row of the table, NVDA reads the contents of the row with the corresponding column names.

 - You can open object properties with <kbd>F4</kbd>.
 - To switch between left-side tabs, use <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Up</kbd> | <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Down</kbd>.  

[See **Properties Editor** shortcuts](Shortcuts#properties-entity-editor)

### SQL Editor

The [**SQL Editor**](SQL-Editor) allows you to create and execute SQL scripts associated with a database connection. To open the **SQL Editor**, focus on the connection or table in the **Database Navigator** and press <kbd>F3</kbd>. To execute the SQL script under the cursor, press <kbd>Ctrl</kbd>+<kbd>Enter</kbd>.

- [See **SQL Editor** shortcuts](Shortcuts#sql-editor)


### Result Set

When you place your focus on the first cell in the data table, the NVDA screen reader says the table name and the name of a column consisting of this cell. If you move from one cell to another, the screen reader announces the column names when you change focus.

If you need to work with columns using the keyboard, you can select an entire column, copy the column name, and resize the column using special keyboard shortcuts. Some of them are only available in the **DBeaver Keyboard Only** scheme.

[See Result Set shortcuts](Shortcuts#result-set)

### ER Diagrams

[**ER Diagrams**](ER-Diagrams) are fully accessible with the keyboard and the NVDA screen reader. You can move inside the table, move or resize it, and listen to the screen reader pronounce the table name and column names inside that table.

[Learn more about ER Diagram shortcuts](ER-Diagrams#bindings)
