<h1 align="center">
  <br>
<img src="https://preview.ibb.co/iBeasd/banner_logo.png" alt="OfflineBay">
<br>
OfflineBay Themes
</h1>

This is the dedicated repository for [OfflineBay](https://github.com/techtacoriginal/offlinebay) themes. All updated themes will be backwards compatible and match all versions of OfflineBay after `2.0.0`.

# How to Download?
If you want to import a theme to OfflineBay, you should download the ZIP file inside the dist folder of any theme above and import them directly using the **Import** button on themes window. For an example **`Default > dist > Default.zip`**

# How to create themes?
If you're interested in creating themes first thing you should know is that all the colors used in OfflineBay UI is stored inside CSS variables. It will be very easy to edit them live because you can simply hit **`ctrl + shift + D`** on OfflineBay to access the developer console. If you scroll down on the styles section you'll be able to see all the variables in one place.

## Structure
Themes can contain following files inside the package.

**`theme.json`** [*Mandatory*] :<br>
Contains all the colors that needed to replace CSS variables. Should contain the theme name and theme title. Theme name can only contain lowercase letters and it should be unique. Take a look at [this file](Default/theme.json) to  get an idea about the structure of theme.json.

**`custom.css`** [*Optional*] :<br>
Can contain any CSS style. These styles will override all the default styles of OfflineBay. Make sure to be careful when adding heavy CSS styles because those could affect the performance of the application.

**`titlebar.png`** [*Optional*] :<br>
This image will replace the original title bar image. For an example, if your theme is light colored the original title bar image may not be visible because it's also light colored. You can add your own dark colored title logo in this file.

**Why both theme.json and custom.css? Isn't it useless?**<br>
There are multiple reasons. For one, data in the theme.json would be loaded before the DOM is loaded and custom.css would be loaded after the DOM is complete. Reason for this is because data inside the theme.json is validated and will not affect the application startup. Data inside the custom.css is not validated because it's a resource hogging process. So it's loaded later via JS. Another reason is that colors inside the theme.json will be used to create the previews in Themes window.

## Packaging

After you created these files you should create a zip file containing all these files in the root of the zip file. Then that zip file should be moved to `dist` folder inside you theme's folder. Take a look at few original themes to further understand this structure.

If your theme is ready to share as mentioned above, you can create a Pull request to this repository or you can share it on the [Suprbay thread](#Suprbay). I would recommend the pull request since it's much cleaner.

**NOTE:** Make sure to keep your themes up to date with future OfflineBay updates. GUI structure could change and theme structure could change with those updates.
