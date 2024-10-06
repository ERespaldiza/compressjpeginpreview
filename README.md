# compressjpeginpreview

## Fork changes with testing purposes
Changed quality ratio from 0,4 to 0,6.

With an original file of 340MB, a 0,4 value reduces the file to 90MB and is still legible except for parts with small fonts. Changing to 0,6 reduces the file size to 102,2MB with better quality.

This quartz filter compresses the JPEG in a PDF, while maintaining usable resolution.  The purpose of this quartz filter is to use it with Apple's Preview.app to quickly reduce the file size of images in PDF's while maintaining legibility.  macOS does have a built-in filter called "Reduce File Size" that has the same purpose, however this filter is too aggressive and converts images to a resolution that is too low.
## Install

To install this filter for the currently logged-in user, run the below command in Terminal:
```
mkdir -p ~/Library/Filters/ && curl -o ~/Library/Filters/Compress\ Images\ in\ PDF.qfilter https://raw.githubusercontent.com/ERespaldiza/compressjpeginpreview/master/Compress%20Images%20in%20PDF.qfilter
```

## Usage
After this the filter can be used in Preview.app (and other apps that support quartz filters).
1. Open the PDF in Preview.app
2. Select _File_ and _Export..._
3. Choose _Format_ to be _PDF_
4. Choose _Quartz Filter_ to _Compress Images in PDF_
5. Choose your prefered destination and click _Save_

## Uninstall
To uninstall simply run:
```
rm ~/Library/Filters/Compress\ Images\ in\ PDF.qfilter
```
