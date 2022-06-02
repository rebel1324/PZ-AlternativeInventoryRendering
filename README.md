# Alternative Inventory Rendering

![](./Contents/mods/001_invqol/aposter00_inv-fs8.png)

## Summary

[STEAM Workshop Item Page](https://steamcommunity.com/sharedfiles/filedetails/?id=2809595776)

This repository stores the code about the mod for the game called "Project Zomboid". 

This mod overrides existing game's Inventory User Interface Code to provide fast and efficient way to interact with User Interface.

## Features

* Restructured Rendering Code
  * This mod provides more efficient way to iterate and render the player's character inventory.
  * This feature is achieved with understanding the fundamental of Lua and Native-Script Interface.
    * Mainly, Most of restructure is focusing on caching "Infrequent Update Data" into Lua Scope. Getting data through Java to Lua Binding is very inefficient when it comes to frequent method call.
    * After that, other portion of effort went to the localizing the variables and method for making lua interpreter to find referenced variable more faster. This has been done based on the lua documentation.
    * Finally, Optimizing interation / variable assignment is the last thing I've focused on.   Since `pairs` and `ipairs` are painful when it comes to large scale iteration, I've managed to utilize the count storage from the Project Zomboid's other UI code. Nothing is better than Vanilla for stability. 
* Additional Quality of Life Feature
  * Displaying the Magazine's Content.
  * Displaying the Weapon's Attachment Status.
    * Displaying whether the weapon has the attachment or not.
    * Displaying the all the icons of the attachments on the weapon.
  * Displaying the verbose status about the Drainable Items.
  * Displaying the verbose status about the Cookable Items.
  * Displaying whether the character has read the book or not.
    * Illiterate trait will disable this feature, ignoring the ModOption Integration.
  * Displaying whether the character has watched the media or not.
    * Illiterate trait will disable this feature, ignoring the ModOption Integration.

## Contribution

* This project is mainly developed as a hobby project. To sustain the development of the addon, I've decided to put the repository to the Github.

  Mostly, I take the reports from the steam workshop page but If you want to let me know more detailed information about the issue, The Issue tab is where you want to be.

* Feel free to submitting the Pull Request. I will review the code and merge as soon as possible if I see fit.

## License

* This project is under MIT License.
* You can do anything you want even not crediting me at all. But, adding me to the credit would be nice.
  `TLDR: Don't ask, I can't answer. Just do It.`

## Credit

* Modulz

   https://icons.modulz.app/

## Contact

* STEAM Profile: https://steamcommunity.com/id/GSTM/
* E-mail: rebel1324@gmail.com
  *As i stated above, I will not answer any kind of "asking for permission" mails. You're good to go.*