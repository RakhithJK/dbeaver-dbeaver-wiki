By default database navagator show all database objects including system objects, all schemas, tables, indexes, administrative and other utility objects.

If you want to change database navigator contentsm simolify or customize it then there are several options. There are 3 modes:

- Simple - minimalistic view for people who mostly wotk with tables
- Advanced - shows all database objects supported by DBeaver
- Custom - manually customized view

When you change view mode you must recovvect to a database (because DBeaver will read different database metadata)

### Simple view

- Shows only schemas and tables
- Hides all system objects
- Hides all utility objects
- Hides all intermediate object folders

### Advanced view

- Shows all system objects
- Hides all utility objects
- Show all folders and all supported database objects

### Custom view

You can configure custom view by setting the following options:

- Show system objects (e.g. system schema pg_catalog or SYSTEM)
- Show utility objects (e.g. internal template databases needed for new database cvreation)
- Show only schemas and tables. It hides all database objects except databases, schemas and tables in these schemas.
- Hide folders. It hides all intermediate logical folders, e.g. "Tables", "Indexes", "Foreign keys". In shows folders contents instead. If there are multiole subfolders then it merges them into a single list.

