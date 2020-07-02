# templator-document-generation-module-for-mendix
Templator - a document generation module for Mendix

Templator is a Mendix module that lets developers generate PDF files using standard Mendix components. Because normal pages are used to generate the documents all styling (rounded corners ✅) and all built-in & app store widgets (charts ✅) are supported out of the box.

This makes Templator the perfect fit for creating reports and other documents with complex styling requirements where using the standard Mendix Document generation is not suitable. 

Finally, your users will be able to get the same experience regardless if they are looking at your app or a PDF file generated from your app.

Your developers will love it too because they can reuse existing pages, widgets, and styling, and only need to build standard pages which thanks to Mendix, is super fast and easy.

Find out more by visiting [https://www.notion.so/gajduk/Templator-d35db3ba165346e3b243d6695636ccd4](https://www.notion.so/gajduk/Templator-d35db3ba165346e3b243d6695636ccd4)

## Installation

1. Download the module from [the downloads page](https://www.notion.so/gajduk/Resources-2b245840946949eeb1a32d678ff5ad35)
2. Import the module in your Mendix project [(help?)](https://docs.mendix.com/howto/integration/importing-and-exporting-objects#2-2-importing-module-packages)

## Generate PDF

1. Build a standard Mendix page using the `DocumentLayout`. You can use any Mendix standard or app store widgets and any styling when designing the page.
2. Declare a microflow that opens the page from step1.
3. Use the microflow action `Generate PDF` to get a beautiful looking PDF file!

    
    ## Troubleshooting

**Having trouble generating a PDF?**
Error messages from Templator can give you important hints about what is going wrong. When testing use custom error handling and show the error message.

### Invalid microflow/parameter

The microflow should only have either exactly zero or exactly one object parameter. Lists or variables such as String are not allowed. Also the object needs to be persistent.

### Security/No access

Check that you have assigned the module role `Templator.User` to the correct project role. The same user role needs rights to 1) execute the microflow that opens the page and 2) read access rights to the object parameter if one is being passed.

### Options header/footer

Page styling does not apply to the custom header/footer. Therefore all styling for the header/footer needs to be embedded in the header/footer HTML. The default font-size for the header/footer is very small so to see anything make sure to set the `font-size`.
[https://github.com/puppeteer/puppeteer/issues/5345#issuecomment-613023667](https://github.com/puppeteer/puppeteer/issues/5345#issuecomment-613023667)
