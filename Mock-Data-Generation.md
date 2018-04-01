Sometimes in software development we need to generate mock, but valid, data for testing. Filling in the database by hand is a time-consuming and exhausting process. It can be very complicated when you need to generate not just 5–10 users, but thousands of entities of different types. DBeaver Mock Data generator helps you generate test data much easier.

[[/images/mockdata_menu.png]] [[/images/mockdata_button.png]]

> _Disclaimer:_ The idea behind Mock Data is to generate fake data in a table and should **NOT TO BE USED IN PRODUCTION ENVIRONMENTS**. Please ensure you have a backup of your database before running the Mock Data generation process.

DBeaver Mock Data generator features:
* works for all the RDBMS that are supported by DBeaver (DB2, MS SQL Server, MySQL, Oracle, PostgreSQL, SQLite etc)
* generates data that matches your database schema
    * generated data matches the database column types
    * all base data types are supported
    * constraints (PK, FK, multi-column FK, unique) support
* over 20 configurable data generators (constants, randoms, sequences, names, domains, addresses, prices, regex based, etc)
* old database data can be saved or overwritten

[[/images/mockdata_wizard.png]]

Mock Data generators for data types with their configurable parameters:
* Boolean
    * Random
    * Sequence (initial, order)
* Date
    * Random (start, end)
    * Sequence (start, step, reverse)
* Numeric
    * Random
    * Sequence (start, step, reverse)
    * Advanced (min, max, precision, scale) <sup>*</sup>
        * Price preset <sup>*</sup>
        * Coordinate preset <sup>*</sup>
* String
    * Text (template, min length, max length)
    * UUID
    * Address <sup>*</sup>
    * City <sup>*</sup>
    * Country <sup>*</sup>
    * Domain <sup>*</sup>
    * Email (gender, with surname, numeric suffix) <sup>*</sup>
    * Name (gender, with surname) <sup>*</sup>
    * Price (country, min, max) <sup>*</sup>
    * Regex based random (regex template) <sup>*</sup>
        * Credit Card preset <sup>*</sup>
        * Email preset <sup>*</sup>
        * Gender preset <sup>*</sup>
        * HEX Color preset <sup>*</sup>
        * IP4 address preset <sup>*</sup>
        * IP6 address preset <sup>*</sup>
        * Phone Number preset <sup>*</sup>
        * Postal Code preset <sup>*</sup>
        * Price preset <sup>*</sup>
* NULL values
* FK - data from the referenced table according to the constraint

[[/images/mockdata_progress.png]]

***
<sup>*</sup> These features are available in the [DBeaver Enterprise Edition](https://dbeaver.com/) only.