**Note: since version 6.2 MockData generator extension is available only in [[Enterprise-Edition]].**

Sometimes in software development we need to generate mock, but valid, data for testing. Populating a database manually is a time-consuming and exhausting process. It can be very complicated when you need to generate not just 5–10 users, but thousands of entities of different types. DBeaver Mock Data generator helps you generate test data much easier.

![](images/mockdata_menu.png) ![](images/mockdata_button.png)

> _Disclaimer:_ The idea behind Mock Data is to generate mock data in a table but it should **NOT TO BE USED IN PRODUCTION ENVIRONMENTS**. Please make sure you have a backup of your database before running the Mock Data generation process.

Th following are features of DBeaver Mock Data generator:

* Works for all the RDBMS that are supported by DBeaver (DB2, MS SQL Server, MySQL, Oracle, PostgreSQL, SQLite, etc.)
* Generates data that matches your database schema:
    * Generated data matches the database column types.
    * All base data types are supported.
    * Constraints (PK, FK, multi-column FK, unique) are supported.
* Supports over 20 configurable data generators (constants, randoms, sequences, names, domains, addresses, prices, regex based, etc.)
* Automatically associates a column with a generator based on the column characteristics
* Saves or overwrites old database data

![](images/mockdata_wizard_2.png)

The following are mock data generators for data types with their configurable parameters:

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
    * Template with parametrized directives for other generators <sup>*</sup>:
        * address() - US postal address
        * city() - one of the world largest cities
        * country() - country
        * domain() - one of the top Internet domains
        * email(gender,surname) - e-mail address (gender is ALL|FEMALE|MALE, surname is true|false)
        * name(gender,surname) - personal name (gender is ALL|FEMALE|MALE, surname is true|false)
        * random(minimum,maximum) - random integer
        * regex(pattern) - regex based value for the pattern
        * sequence(start,step) - sequence of integers
* NULL values
* FK - data from the referenced table according to the constraint

![](images/mockdata_template.png)

![](images/mockdata_progress.png)

***
<sup>*</sup> These features are available in the [DBeaver Enterprise Edition](https://dbeaver.com/) only.
