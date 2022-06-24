# Manual_IPA_Share
This repo lists the steps to share ipa link without the need to use Diawi, Deployninja or other similar websites.

Follow these steps to create a sharable build link manually:

1. While exporting the .ipa file, select **_INCLUDE manifest for over-the-air installation_**, and then paste your dropbox url with **_AppName.ipa_**, and **_AppName1.png_**, **_AppName2.png_** in the respective fields.

2. Create a dropbox account.

3. Paste your .ipa file.

4. Copy link to this .ipa file. It will look like this:
	https://www.dropbox.com/s/u74ecqyuzsud32w/Avatus.ipa?dl=0

5. Now replace www with dl and remove ?dl=0 from suffix : 
	https://dl.dropbox.com/s/u74ecqyuzsud32w/Avatus.ipa

6. Copy this URL, open **_manifest.plist_**, and paste it in **_software-package_** under **_assets_**

7. Now copy this **_manifest.plist_** file and paste it in dropbox at the same location as your .ipa

8. Copy link to manifest.plist. It will look like this:
	https://www.dropbox.com/s/kb9z2d1uet15jiq/manifest.plist?dl=0

9. Repeat step 5 for this url:
	https://dl.dropbox.com/s/kb9z2d1uet15jiq/manifest.plist

10. Copy this URL and paste it at the end of:
	itms-services://?action=download-manifest&url=

11. Final url will look like:
	itms-services://?action=download-manifest&url=https://dl.dropbox.com/s/kb9z2d1uet15jiq/manifest.plist

12. Create a text file name **_AppName.html_** and paste this URL in href:
	<a href="itms-services://?action=download-manifest&url=https://dl.dropbox.com/s/kb9z2d1uet15jiq/manifest.plist">Install App</a>

13. Share this file on devices you wish to install the build.
