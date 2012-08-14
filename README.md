# Smart Images for ExactTarget
Smart Images are my attempt at creating a Live Images-like solution that allows users to interact w/ the behavior of the links/images via the API. ince all of the data is maintained within a data extension it can be easily accessed and manipulated through the API, but a handy little dashboard is included too in case you'd like to interact with it via a GUI. 

You may notice some references to deals and "good" and "expired" statuses. The origin of this project spun out of the need to drive time sensitive deal emails so a "good" deal meant it was still available, which an "expired" one was no longer available and a generic/default would be rendered. While the nominclature arould the project may still be geared towards deals the application can span many different use cases.

## Prerequisites
The only things required to get rolling are:

+		An ExactTarget account
+		Microsites (or Landing Pages)
+		Content Areas (the "My Contents" folder)
+		A Data Extension with the following structure
	+		**dealId** - Text - Primary Key
	+		**dealDescription** - Text
	+		**dealGoodImageUrl** - Text
	+		**dealExpiredImageUrl** - Text
	+		**dealGoodLinkUrl** - Text
	+		**dealExpiredLinkUrl** - Text
	+		**active** - Boolean
	+		**published** - Boolean

## Files
+		**url-getter.html** - The logic that looks up the status of an image in the DE and returned to proper link URL
+		**image-getter.html** - The logic that looks up the status of an image in the DE and returned to proper image URL
+		**dashboard.html** - The main dashboard page to view and manage all smart images
	+		**new.html** - The view which allows a user to create a new image via the GUI/dashboard
	+		**create.html** - The "controller-like" action that creates a new smart image via POST from new.html
	+		**edit.html** - The view which allows a user to edit an existing image via the GUI/dashboard
	+		**update.html** - The "controller-like" action that updates a smart image from the DE via POST from edit.html
	+		**toggle.html** - The "controller-like" action that toggles an image between "good" and "expired" from dashboard.html
	+		**delete.html** - The "controller-like" action that deletes a smart image via POST from dashboard.html
	+		**publish-ca.html** - The "controller-like" action that creates/updates a Content Area containing all the logic/mark-up necessary to use a smart image in an email from dashboard.html
+		**smart-block.html** - Generic layout file that shows an example of the smart block that's created from the publish-ca.html action


## Errata & Addenda
As you browse the files of this project you'll notice that many of them have a "Custom Account Variables" section at the top. This is where you'll define account-specific values such as data extension CustomerKeys as well as the specific URLs to other dependent landing pages, etc. It is very important that you adjust these or things won't work right. I've tried to make the comments as descriptive as possible, but when in doubt, feel free to ask.

## Questions/Issues
Please feel free to fork and submit a pull request, log issues within the Github project, or [email me](mailto:kkeesling@exacttarget.com?subject=Live Images on Github)

Kyle Keesling - [@kylekeesling](http://twitter.com/kylekeesling)

	
