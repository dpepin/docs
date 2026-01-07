When developing an application, you can use an image as the background of a panel field, of the cells in a cell-based table field, or of a form view. You can use a reference to aAR System serverimage object, or you can store the image as an embedded object in the field.

To support the Image Reference functionality for panel and cell-based table fields, Remedy AR System clients and supporting applications such as theMid Tiermust be release 7.5.00 or later. When previous clients open a form containing an image reference, the image is converted to embedded format.

Related topics

[Adding-icons-and-images-to-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Adding-icons-and-images-to-Progressive-Web-Applications/)

[Creating-and-modifying-image-objects](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Adding-icons-and-images-to-Progressive-Web-Applications/Creating-and-modifying-image-objects/)

[Adding-icons-to-UI-elements-on-forms-by-using-Developer-Studio](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Adding-icons-and-images-to-Progressive-Web-Applications/Adding-BMC-icons-to-UI-elements-on-forms-by-using-Developer-Studio/)

[Previews-of-icons-available-in-Developer-Studio-to-support-PWA](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Adding-icons-and-images-to-Progressive-Web-Applications/Previews-of-icons-available-in-Developer-Studio-to-support-PWA/)

The following video (3:54) provides a summary of adding static or SVG images inDeveloper Studiofor progressive views:

[🎥 Watch Video: https://www.youtube.com/watch?v=349xdes86qM](https://www.youtube.com/watch?v=349xdes86qM)

![icon_play.png](.attachments/Adding-background-images-to-fields-and-form-views_icon_play.png)<https://www.youtube.com/watch?v=349xdes86qM>

## Using transparent images

Developer StudioandMid Tiersupport**.gif**and**.png**images, which*can*have transparent backgrounds. You can use**.gif**and**.png**images anywhere that images are supported inAR System server, including

* Backgrounds on form views
* Backgrounds on standalone panel fields

PNG images that use*alpha transparency*are supported by Firefox and Safari. PNG and GIF images that use*binary transparency*are supported by allAR System servercompatible browsers.

To create graphics with transparent backgrounds that let the surface on which they are placed show through, use**.gif**and**.png**images with the Display as Flat Image property. For example, use such images to create borderless buttons. The following figure shows a**.gif**coffee cup image with a transparent background on a regular button and on a borderless button.

**A .gif file with transparent background on regular and borderless buttons**

![SK_Developing_Superbook-219.gif](.attachments/Adding-background-images-to-fields-and-form-views_SK_Developing_Superbook-219.gif)

To build toolbars, you can use transparent images on borderless buttons as shown in the following figure.

**Transparent images as toolbar buttons**  
![trans_image2_horizontal.GIF](.attachments/Adding-background-images-to-fields-and-form-views_trans_image2_horizontal.GIF)

**Tip**

To add decorative graphics to forms, use borderless buttons without workflow.

Most browsers always use a visual aid, such as a dotted outline, to indicate that borderless buttons have focus. Internet Explorer, however, does this only when the form has certain background colors.

## To add an image to a panel field or a cell-based table

1. Select the panel field or the working cell of the cell-based table field.
2. In the**Properties**tab, click the Background Image property, and click its**ellipsis**button.
3. In the Background Image dialog box:
   1. If necessary, click**Clear Image**to delete an existing image.
   2. Browse for the image to display on the button.  
      You can select**.bmp**,**.jpeg**,**.jpg**, .**gif**, and**.png**files. The selected image appears in the Preview area.
   3. To save the image to a different file or folder, click**Save to File**.
   4. Set the Image Type:
      * **Embedded Image**—The image is stored in the field display properties as anARByteList.  
        In this case, the image is embedded in the form and is therefore downloaded with the form whenever the form is refreshed by the client.
      * **Image Reference**—A reference to a shared image object is stored in the field display properties.  
        In this case, the image is stored as an image object inAR System server. When the form is downloaded, the image is cached separately, so the image does not have to be refreshed along with the form. This allows for faster form refresh time.
   5. Click**OK**.
4. To position the graphic horizontally in the panel or cell, select the Background Image Horizontal property, and then select one of the following options:
   * **Left**—Position the left edge of the image at the left edge of the panel or cell.
   * **Center**—Position the horizontal center of the image at the horizontal center of the panel or cell.
   * **Fill**—Resize the image horizontally to fit the width of the panel or cell.
   * **Right**—Position the right edge of the image at the right edge of the panel or cell.
   * **Tile**—If the width of the image is smaller than the width of the panel or cell, tile the image horizontally in the panel or cell. If the width of the image is larger than the width of the panel or cell, Tile has no effect.  
     This property works together with the Background Image Vertical property to control the overall position and dimensions of the image.
5. To position the graphic vertically in the pane or cell, select the Background Image Vertical property, and then select one of the following options:
   * **Top**—Position the top edge of the image at the top edge of the panel or cell.
   * **Center**—Position the vertical center of the image at the vertical center of the panel or cell.
   * **Fill**—Resize the image vertically to fit the height of the panel or cell.
   * **Bottom**—Position the bottom edge of the image at the bottom edge of the panel or cell.
   * **Tile**—If the height of the image is smaller than the height of the panel or cell, tile the image vertically in the panel or cell. If the height of the image is larger than the height of the panel or cell, Tile has no effect.  
     This property works together with the Background Image Horizontal property to control the overall position and dimensions of the image. However, the Background Image Vertical property is not available in progressive views.
6. To add a background image for each device type, namely desktop, mobile, and tablet, click the ellipsis button for the Background Image property under Progressive-Desktop, Progressive-Mobile, and Progressive-Tablet respectively.