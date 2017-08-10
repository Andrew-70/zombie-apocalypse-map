## Choose your icon

Rather than always having a red marker, it would be good to be able to place emojis on the map to show different points of interest. Perhaps you might want to mark a hospital where you could go for refuge from the zombies, a weapons cache to help you fight off the zombies, or even the location of the zombies themselves!

To do this, you will need some emojis. You could draw your own emojis if you are feeling creative, or there are plenty to choose from on [Wikimedia commons](https://commons.wikimedia.org/wiki/Emoji). Save your emojis as 32px x 32px PNG files for best results.

Here are the emojis we will use in this guide, but you can use as many different emojis as you like.
![Hospital](images/hospital.png) ![Weapons](images/weapons.png) ![Zombie](images/zombie.png)

+ Decide on the emojis you will use and save the PNG image files into the same folder as your `index.html` file. Make sure the file names of your emoji pictures do not contain any spaces.

+ Locate the line of code `<div id="zombie_map"></div>` and on a blank line immediately after it, add in the HTML tags to begin and end a form:

```html
<form>
</form>
```

+ Between the `<form>` tags, add a `<select>` element. This creates a drop down box where you can select an emoji.

```html
Select an emoji
<select id="icon_to_use">
  <option value="zombie.png">Zombie</option>
  <option value="hospital.png">Hospital</option>
</select>
```

+ Save the file and refresh your internet browser. You should see a drop down with only two options - zombie or hospital.

![Zombie or hospital](images/zombie-or-hospital.png)

+ Add options to your `<select>` for every emoji you have chosen to use. Save and check that all of the options appear properly in your drop down box.


--- hints ---
--- hint ---
Add another line that looks like this for each emoji
`<option value="hospital.png">Hospital</option>`
--- /hint ---

--- hint ---
Make sure that you set the correct file name of each emoji picture as the `value` in the option, and that each emoji picture is saved in the same folder as your `index.html` page.
--- /hint ---

--- /hints ---

+ Now let's tell the map to display the chosen emoji instead of the red marker when we click the map. Here is a line of code which will get the currently selected emoji.

```javascript
var emoji = document.getElementById('***').value;
```
However, you need to replace *** with the ID of the `<select>` element, to tell the code where to get the data from.

Add this line of code here:
![Add your code here](images/add-code-here.png)

+ Finally, add a comma at the end of the line `map: zombie_map`, then add the line `icon: emoji` below it to set the displayed icon to be whichever emoji was selected in the drop down at the time.

![All the icons](images/zombies-oh-my.png)