# Design-Web

(This page is under construction)

A list of practices for optimizing the workflow from design to software implementation.

## Designer

### Links

* [Ink](http://ink.chrometaphore.com/) - A photoshop documentor plugin.

### Grid
* Use the bootstrap grid for websites.

### Fonts
* List of all fonts
* Provide files for the fonts:
    * in the common storage. File extensions: *.eot, *svg, *.ttf, *.woff, *.css
    * or as a downloadable link.
* Font size:
    * Provide default font size.

### Headings
* Define how headings should be visualized: h1, h2, h3, h4, h5, h6. Font, Size (px), Weight (Bold, Italic), Color (RGB), Letter-Spacing (if needed).

### Colors
All colors should have:
* name
* RGB value.
The colors should be **referenced and communicated by name** (not by value).

### Image and Logos
* Make sure that **all** logos and image are saved in separate files.
* Use only optimized for the Web images: compression, less colors, transparency. Sprite?

### Icons
* Well known icons (like heart, menu), should be done with a well known CSS/Font by the software developer. The designer should 
    * TODO: Software devs should choose CSS/Font and make sure that the designers can use it.
* Use open source icons:
    * http://weloveiconfonts.com/
    * http://entypo.com/ - Entypo is a set of 250+ carefully crafted pictograms. The package contains an icon font — OpenType, TrueType and @font-face — EPS, PDF and PSD files. All released for free under the license CC BY-SA 3.0.

### Borders, Shadows, etc
e.g.
* ```box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.1)``` (default values). Optionally provide specific height, width and color values.

### Buttons

* Needs agreement with the software devs - what values are needed.
* Design for hover, click, disabled state.

### Lists
* Sometimes there are designed icons for unordered list items. How exactly to share them to the developers?

## File Formats
The web developer should receive logos and images in one of the following file formats:
* JPG, PNG, GIF.
* Logos should be transparent.

## Common Storage
* **Uniqueness**: All files should be saved in a common storage. Exchange of files between people should happen only through links or references to the files in the common storage.
* **Completenes**: Every design iteration should contain **all** files needed to implement the project.

## Mobile Design
* Sizing of the components? How should we do it correctly? Experience from FlashPoll?
