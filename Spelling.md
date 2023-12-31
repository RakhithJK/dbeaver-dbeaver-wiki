**Note: This feature is available
in [Lite](Lite-Edition), [Enterprise](Enterprise-Edition), [Ultimate](Ultimate-Edition)
and <a href="https://dbeaver.com/dbeaver-team-edition">Team</a> editions only.**

DBeaver's spelling function is a feature designed to detect spelling errors. It allows you to change the incorrect words, upload custom dictionaries in any language and it provides you with advanced options for a more refined text management experience.

## Usage

The spelling function is accessible in your SQL script files. Words that are not spelled correctly are underlined, which will alert you to potential inaccuracies.

To change these incorrect words, open the context menu by right-clicking on the word and selecting **Quick Fix** or by using the <kbd>Ctrl+1</kbd> (or <kbd>⌘1</kbd> for Mac OS). 

![](images/spelling_context_menu.png)

The context menu offers several options:

* Change the incorrect word with to a suggested word.
* Add the word to the dictionary.
* Ignore the word during the current session.
* Disable the spell checking entirely.


To apply any of these changes, you need to double-click on the chosen option with the left mouse button or press the
<kbd>Tab</kbd> key.

## Settings


To open the settings for the spelling page, navigate through the following steps: **Window** -> **Preferences** -> **Editors** ->
**Text Editors** -> **Spelling**.

![](images/spelling.png)

### Activation

The spelling function is enabled by default but can be customized to your requirements.

You can disable the spelling function by unchecking the box next to **Enable spell checking** in Preferences.



### Options

DBeaver's spelling settings provide specific options for this feature that can be tailored to your needs.

 Option name                             | Description                                                          
-----------------------------------------|----------------------------------------------------------------------
 **Ignore words with digits**            | Skips words containing numbers.                                      
 **Ignore mix case words**               | Skips words with combined upper and lower case letters.              
 **Ignore sentence capitalization**      | Skips words starting with a lowercase letter at sentence beginnings. 
 **Ignore URLs**                         | Excludes web addresses from spell checking.                          
 **Ignore words shorter than 4 letters** | Disregards shorter words from spell checking.                        

### Custom Dictionaries

DBeaver includes an integrated English dictionary. However, you can choose to disable it and connect your custom
dictionary, or use both simultaneously, according to your needs.

In DBeaver's spelling settings you can add your own custom dictionary by specifying the path to it in the **User defined
dictionary** field. This dictionary should be a **.txt** file with one word per line.

To disable the custom dictionary, clear the **User defined dictionary** field and apply the changes.

### Advanced Settings

You can adjust the **Maximum number of correction proposals**. This setting controls the number of suggested
substitutions that appear in the context menu for each misspelled word.

Also, you can specify the **Maximum number of problems reported per file**. This setting determines the total number of
words, starting from the first one, that the system will flag for replacement in each file.