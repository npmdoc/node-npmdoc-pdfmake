# api documentation for  [pdfmake (v0.1.27)](http://pdfmake.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-pdfmake.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pdfmake) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pdfmake.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pdfmake)
#### Client/server side PDF printing in pure JavaScript

[![NPM](https://nodei.co/npm/pdfmake.png?downloads=true)](https://www.npmjs.com/package/pdfmake)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pdfmake/build/screenCapture.buildApidoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-pdfmake%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pdfmake/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pdfmake/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pdfmake/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Bartek Pampuch",
        "email": "bartosz.pampuch@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/bpampuch/pdfmake/issues"
    },
    "config": {
        "blanket": {
            "pattern": "src",
            "data-cover-never": [
                "node_modules",
                "tests"
            ]
        }
    },
    "dependencies": {
        "linebreak": "^0.3.0",
        "lodash": "^4.17.4",
        "pdfkit": "^0.8.0"
    },
    "description": "Client/server side PDF printing in pure JavaScript",
    "devDependencies": {
        "brfs": "^1.4.3",
        "expose-loader": "^0.7.3",
        "gulp": "^3.9.1",
        "gulp-each": "^0.5.0",
        "gulp-file-contents-to-json": "^0.2.1",
        "gulp-header": "^1.8.8",
        "gulp-jshint": "^2.0.4",
        "gulp-rename": "^1.2.2",
        "gulp-replace": "^0.5.4",
        "gulp-sourcemaps": "^2.4.1",
        "gulp-spawn-mocha": "^3.1.0",
        "gulp-uglify": "^2.1.2",
        "gulp-util": "^3.0.8",
        "iconv-lite": "^0.4.15",
        "jshint": "^2.9.4",
        "json-loader": "^0.5.4",
        "mocha": "^3.2.0",
        "sinon": "^2.1.0",
        "string-replace-webpack-plugin": "^0.1.3",
        "transform-loader": "^0.2.4",
        "webpack": "^2.3.2",
        "webpack-stream": "^3.2.0"
    },
    "directories": {
        "test": "tests"
    },
    "dist": {
        "shasum": "7c146dabb20a28724fdb56bfd3d42f89bc7c431b",
        "tarball": "https://registry.npmjs.org/pdfmake/-/pdfmake-0.1.27.tgz"
    },
    "gitHead": "ebf896bb1d75c0da62a1cf46892478c6480cceb6",
    "homepage": "http://pdfmake.org",
    "keywords": [
        "pdf",
        "javascript",
        "printing",
        "layout"
    ],
    "license": "MIT",
    "main": "src/printer.js",
    "maintainers": [
        {
            "name": "bpampuch",
            "email": "bartosz.pampuch@gmail.com"
        },
        {
            "name": "danawoodman",
            "email": "dana@danawoodman.com"
        },
        {
            "name": "liborm85",
            "email": "liborm85@gmail.com"
        },
        {
            "name": "miltador",
            "email": "miltador@yandex.ua"
        }
    ],
    "name": "pdfmake",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/bpampuch/pdfmake.git"
    },
    "scripts": {
        "build": "gulp build",
        "test": "gulp"
    },
    "version": "0.1.27"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pdfmake](#apidoc.module.pdfmake)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>docMeasure (fontProvider, styleDictionary, defaultStyle, imageMeasure, tableLayouts, images)](#apidoc.element.pdfmake.docMeasure)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>documentContext (pageSize, pageMargins)](#apidoc.element.pdfmake.documentContext)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>elementWriter (context, tracker)](#apidoc.element.pdfmake.elementWriter)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>fontProvider (fontDescriptors, pdfKitDoc)](#apidoc.element.pdfmake.fontProvider)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>imageMeasure (pdfKitDoc, imageDictionary)](#apidoc.element.pdfmake.imageMeasure)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>layoutBuilder (pageSize, pageMargins, imageMeasure)](#apidoc.element.pdfmake.layoutBuilder)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>line (maxWidth)](#apidoc.element.pdfmake.line)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>pageElementWriter (context, tracker)](#apidoc.element.pdfmake.pageElementWriter)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>styleContextStack (styleDictionary, defaultStyle)](#apidoc.element.pdfmake.styleContextStack)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>tableProcessor (tableNode)](#apidoc.element.pdfmake.tableProcessor)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>textTools (fontProvider)](#apidoc.element.pdfmake.textTools)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>traversalTracker ()](#apidoc.element.pdfmake.traversalTracker)
1.  object <span class="apidocSignatureSpan">pdfmake.</span>columnCalculator
1.  object <span class="apidocSignatureSpan">pdfmake.</span>docMeasure.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>documentContext.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>elementWriter.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>fontProvider.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>helpers
1.  object <span class="apidocSignatureSpan">pdfmake.</span>imageMeasure.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>layoutBuilder.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>line.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>pageElementWriter.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>qrEnc
1.  object <span class="apidocSignatureSpan">pdfmake.</span>styleContextStack.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>tableProcessor.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>textDecorator
1.  object <span class="apidocSignatureSpan">pdfmake.</span>textTools.prototype
1.  object <span class="apidocSignatureSpan">pdfmake.</span>traversalTracker.prototype

#### [module pdfmake.columnCalculator](#apidoc.module.pdfmake.columnCalculator)
1.  [function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>buildColumnWidths (columns, availableWidth)](#apidoc.element.pdfmake.columnCalculator.buildColumnWidths)
1.  [function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>isAutoColumn (column)](#apidoc.element.pdfmake.columnCalculator.isAutoColumn)
1.  [function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>isStarColumn (column)](#apidoc.element.pdfmake.columnCalculator.isStarColumn)
1.  [function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>measureMinMax (columns)](#apidoc.element.pdfmake.columnCalculator.measureMinMax)

#### [module pdfmake.docMeasure](#apidoc.module.pdfmake.docMeasure)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>docMeasure (fontProvider, styleDictionary, defaultStyle, imageMeasure, tableLayouts, images)](#apidoc.element.pdfmake.docMeasure.docMeasure)

#### [module pdfmake.docMeasure.prototype](#apidoc.module.pdfmake.docMeasure.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>buildOrderedMarker (counter, styleStack, type, separator)](#apidoc.element.pdfmake.docMeasure.prototype.buildOrderedMarker)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>buildUnorderedMarker (styleStack, gapSize, type)](#apidoc.element.pdfmake.docMeasure.prototype.buildUnorderedMarker)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>convertIfBase64Image (node)](#apidoc.element.pdfmake.docMeasure.prototype.convertIfBase64Image)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>gapSizeForList ()](#apidoc.element.pdfmake.docMeasure.prototype.gapSizeForList)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureCanvas (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureCanvas)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureColumns (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureColumns)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureDocument (docStructure)](#apidoc.element.pdfmake.docMeasure.prototype.measureDocument)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureImage (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureImage)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureLeaf (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureLeaf)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureNode (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureNode)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureOrderedList (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureOrderedList)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureQr (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureQr)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureTable (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureTable)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureUnorderedList (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureUnorderedList)
1.  [function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureVerticalContainer (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureVerticalContainer)

#### [module pdfmake.documentContext](#apidoc.module.pdfmake.documentContext)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>documentContext (pageSize, pageMargins)](#apidoc.element.pdfmake.documentContext.documentContext)

#### [module pdfmake.documentContext.prototype](#apidoc.module.pdfmake.documentContext.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>addMargin (left, right)](#apidoc.element.pdfmake.documentContext.prototype.addMargin)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>addPage (pageSize)](#apidoc.element.pdfmake.documentContext.prototype.addPage)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>beginColumn (width, offset, endingCell)](#apidoc.element.pdfmake.documentContext.prototype.beginColumn)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>beginColumnGroup ()](#apidoc.element.pdfmake.documentContext.prototype.beginColumnGroup)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>beginDetachedBlock ()](#apidoc.element.pdfmake.documentContext.prototype.beginDetachedBlock)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>calculateBottomMost (destContext)](#apidoc.element.pdfmake.documentContext.prototype.calculateBottomMost)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>completeColumnGroup ()](#apidoc.element.pdfmake.documentContext.prototype.completeColumnGroup)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>endDetachedBlock ()](#apidoc.element.pdfmake.documentContext.prototype.endDetachedBlock)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>getCurrentPage ()](#apidoc.element.pdfmake.documentContext.prototype.getCurrentPage)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>getCurrentPosition ()](#apidoc.element.pdfmake.documentContext.prototype.getCurrentPosition)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>initializePage ()](#apidoc.element.pdfmake.documentContext.prototype.initializePage)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>markEnding (endingCell)](#apidoc.element.pdfmake.documentContext.prototype.markEnding)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>moveDown (offset)](#apidoc.element.pdfmake.documentContext.prototype.moveDown)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>moveTo (x, y)](#apidoc.element.pdfmake.documentContext.prototype.moveTo)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>moveToNextPage (pageOrientation)](#apidoc.element.pdfmake.documentContext.prototype.moveToNextPage)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>pageSnapshot ()](#apidoc.element.pdfmake.documentContext.prototype.pageSnapshot)
1.  [function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>saveContextInEndingCell (endingCell)](#apidoc.element.pdfmake.documentContext.prototype.saveContextInEndingCell)

#### [module pdfmake.elementWriter](#apidoc.module.pdfmake.elementWriter)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>elementWriter (context, tracker)](#apidoc.element.pdfmake.elementWriter.elementWriter)

#### [module pdfmake.elementWriter.prototype](#apidoc.module.pdfmake.elementWriter.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addFragment (block, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)](#apidoc.element.pdfmake.elementWriter.prototype.addFragment)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addImage (image, index)](#apidoc.element.pdfmake.elementWriter.prototype.addImage)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addLine (line, dontUpdateContextPosition, index)](#apidoc.element.pdfmake.elementWriter.prototype.addLine)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addQr (qr, index)](#apidoc.element.pdfmake.elementWriter.prototype.addQr)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addVector (vector, ignoreContextX, ignoreContextY, index)](#apidoc.element.pdfmake.elementWriter.prototype.addVector)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>alignImage (image)](#apidoc.element.pdfmake.elementWriter.prototype.alignImage)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>alignLine (line)](#apidoc.element.pdfmake.elementWriter.prototype.alignLine)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>getCurrentPositionOnPage ()](#apidoc.element.pdfmake.elementWriter.prototype.getCurrentPositionOnPage)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>popContext ()](#apidoc.element.pdfmake.elementWriter.prototype.popContext)
1.  [function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>pushContext (contextOrWidth, height)](#apidoc.element.pdfmake.elementWriter.prototype.pushContext)

#### [module pdfmake.fontProvider](#apidoc.module.pdfmake.fontProvider)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>fontProvider (fontDescriptors, pdfKitDoc)](#apidoc.element.pdfmake.fontProvider.fontProvider)

#### [module pdfmake.fontProvider.prototype](#apidoc.module.pdfmake.fontProvider.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.fontProvider.prototype.</span>provideFont (familyName, bold, italics)](#apidoc.element.pdfmake.fontProvider.prototype.provideFont)

#### [module pdfmake.helpers](#apidoc.module.pdfmake.helpers)
1.  [function <span class="apidocSignatureSpan">pdfmake.helpers.</span>fontStringify (key, val)](#apidoc.element.pdfmake.helpers.fontStringify)
1.  [function <span class="apidocSignatureSpan">pdfmake.helpers.</span>isFunction (functionToCheck)](#apidoc.element.pdfmake.helpers.isFunction)
1.  [function <span class="apidocSignatureSpan">pdfmake.helpers.</span>offsetVector (vector, x, y)](#apidoc.element.pdfmake.helpers.offsetVector)
1.  [function <span class="apidocSignatureSpan">pdfmake.helpers.</span>pack ()](#apidoc.element.pdfmake.helpers.pack)

#### [module pdfmake.imageMeasure](#apidoc.module.pdfmake.imageMeasure)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>imageMeasure (pdfKitDoc, imageDictionary)](#apidoc.element.pdfmake.imageMeasure.imageMeasure)

#### [module pdfmake.imageMeasure.prototype](#apidoc.module.pdfmake.imageMeasure.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.imageMeasure.prototype.</span>measureImage (src)](#apidoc.element.pdfmake.imageMeasure.prototype.measureImage)

#### [module pdfmake.layoutBuilder](#apidoc.module.pdfmake.layoutBuilder)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>layoutBuilder (pageSize, pageMargins, imageMeasure)](#apidoc.element.pdfmake.layoutBuilder.layoutBuilder)

#### [module pdfmake.layoutBuilder.prototype](#apidoc.module.pdfmake.layoutBuilder.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addBackground (background)](#apidoc.element.pdfmake.layoutBuilder.prototype.addBackground)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addDynamicRepeatable (nodeGetter, sizeFunction)](#apidoc.element.pdfmake.layoutBuilder.prototype.addDynamicRepeatable)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addHeadersAndFooters (header, footer)](#apidoc.element.pdfmake.layoutBuilder.prototype.addHeadersAndFooters)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addStaticRepeatable (headerOrFooter, sizeFunction)](#apidoc.element.pdfmake.layoutBuilder.prototype.addStaticRepeatable)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addWatermark (watermark, fontProvider, defaultStyle)](#apidoc.element.pdfmake.layoutBuilder.prototype.addWatermark)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>buildNextLine (textNode)](#apidoc.element.pdfmake.layoutBuilder.prototype.buildNextLine)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>layoutDocument (docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images, watermark, pageBreakBeforeFct )](#apidoc.element.pdfmake.layoutBuilder.prototype.layoutDocument)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processCanvas (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processCanvas)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processColumns (columnNode)](#apidoc.element.pdfmake.layoutBuilder.prototype.processColumns)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processImage (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processImage)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processLeaf (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processLeaf)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processList (orderedList, node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processList)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processNode (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processNode)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processQr (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processQr)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processRow (columns, widths, gaps, tableBody, tableRow)](#apidoc.element.pdfmake.layoutBuilder.prototype.processRow)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processTable (tableNode)](#apidoc.element.pdfmake.layoutBuilder.prototype.processTable)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processVerticalContainer (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processVerticalContainer)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>registerTableLayouts (tableLayouts)](#apidoc.element.pdfmake.layoutBuilder.prototype.registerTableLayouts)
1.  [function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>tryLayoutDocument (docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images, watermark, pageBreakBeforeFct )](#apidoc.element.pdfmake.layoutBuilder.prototype.tryLayoutDocument)

#### [module pdfmake.line](#apidoc.module.pdfmake.line)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>line (maxWidth)](#apidoc.element.pdfmake.line.line)

#### [module pdfmake.line.prototype](#apidoc.module.pdfmake.line.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>addInline (inline)](#apidoc.element.pdfmake.line.prototype.addInline)
1.  [function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>getAscenderHeight ()](#apidoc.element.pdfmake.line.prototype.getAscenderHeight)
1.  [function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>getHeight ()](#apidoc.element.pdfmake.line.prototype.getHeight)
1.  [function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>getWidth ()](#apidoc.element.pdfmake.line.prototype.getWidth)
1.  [function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>hasEnoughSpaceForInline (inline)](#apidoc.element.pdfmake.line.prototype.hasEnoughSpaceForInline)

#### [module pdfmake.pageElementWriter](#apidoc.module.pdfmake.pageElementWriter)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>pageElementWriter (context, tracker)](#apidoc.element.pdfmake.pageElementWriter.pageElementWriter)

#### [module pdfmake.pageElementWriter.prototype](#apidoc.module.pdfmake.pageElementWriter.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addFragment (fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)](#apidoc.element.pdfmake.pageElementWriter.prototype.addFragment)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addImage (image, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addImage)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addLine (line, dontUpdateContextPosition, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addLine)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addQr (qr, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addQr)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addVector (vector, ignoreContextX, ignoreContextY, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addVector)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>beginUnbreakableBlock (width, height)](#apidoc.element.pdfmake.pageElementWriter.prototype.beginUnbreakableBlock)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>commitUnbreakableBlock (forcedX, forcedY)](#apidoc.element.pdfmake.pageElementWriter.prototype.commitUnbreakableBlock)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>context ()](#apidoc.element.pdfmake.pageElementWriter.prototype.context)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>currentBlockToRepeatable ()](#apidoc.element.pdfmake.pageElementWriter.prototype.currentBlockToRepeatable)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>moveToNextPage (pageOrientation)](#apidoc.element.pdfmake.pageElementWriter.prototype.moveToNextPage)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>popFromRepeatables ()](#apidoc.element.pdfmake.pageElementWriter.prototype.popFromRepeatables)
1.  [function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>pushToRepeatables (rep)](#apidoc.element.pdfmake.pageElementWriter.prototype.pushToRepeatables)

#### [module pdfmake.qrEnc](#apidoc.module.pdfmake.qrEnc)
1.  [function <span class="apidocSignatureSpan">pdfmake.qrEnc.</span>measure (node)](#apidoc.element.pdfmake.qrEnc.measure)

#### [module pdfmake.styleContextStack](#apidoc.module.pdfmake.styleContextStack)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>styleContextStack (styleDictionary, defaultStyle)](#apidoc.element.pdfmake.styleContextStack.styleContextStack)

#### [module pdfmake.styleContextStack.prototype](#apidoc.module.pdfmake.styleContextStack.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>auto (item, callback)](#apidoc.element.pdfmake.styleContextStack.prototype.auto)
1.  [function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>autopush (item)](#apidoc.element.pdfmake.styleContextStack.prototype.autopush)
1.  [function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>clone ()](#apidoc.element.pdfmake.styleContextStack.prototype.clone)
1.  [function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>getProperty (property)](#apidoc.element.pdfmake.styleContextStack.prototype.getProperty)
1.  [function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>pop (howMany)](#apidoc.element.pdfmake.styleContextStack.prototype.pop)
1.  [function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>push (styleNameOrOverride)](#apidoc.element.pdfmake.styleContextStack.prototype.push)

#### [module pdfmake.tableProcessor](#apidoc.module.pdfmake.tableProcessor)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>tableProcessor (tableNode)](#apidoc.element.pdfmake.tableProcessor.tableProcessor)

#### [module pdfmake.tableProcessor.prototype](#apidoc.module.pdfmake.tableProcessor.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>beginRow (rowIndex, writer)](#apidoc.element.pdfmake.tableProcessor.prototype.beginRow)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>beginTable (writer)](#apidoc.element.pdfmake.tableProcessor.prototype.beginTable)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>drawHorizontalLine (lineIndex, writer, overrideY)](#apidoc.element.pdfmake.tableProcessor.prototype.drawHorizontalLine)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>drawVerticalLine (x, y0, y1, vLineIndex, writer)](#apidoc.element.pdfmake.tableProcessor.prototype.drawVerticalLine)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>endRow (rowIndex, writer, pageBreaks)](#apidoc.element.pdfmake.tableProcessor.prototype.endRow)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>endTable (writer)](#apidoc.element.pdfmake.tableProcessor.prototype.endTable)
1.  [function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>onRowBreak (rowIndex, writer)](#apidoc.element.pdfmake.tableProcessor.prototype.onRowBreak)

#### [module pdfmake.textDecorator](#apidoc.module.pdfmake.textDecorator)
1.  [function <span class="apidocSignatureSpan">pdfmake.textDecorator.</span>drawBackground (line, x, y, pdfKitDoc)](#apidoc.element.pdfmake.textDecorator.drawBackground)
1.  [function <span class="apidocSignatureSpan">pdfmake.textDecorator.</span>drawDecorations (line, x, y, pdfKitDoc)](#apidoc.element.pdfmake.textDecorator.drawDecorations)

#### [module pdfmake.textTools](#apidoc.module.pdfmake.textTools)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>textTools (fontProvider)](#apidoc.element.pdfmake.textTools.textTools)

#### [module pdfmake.textTools.prototype](#apidoc.module.pdfmake.textTools.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.textTools.prototype.</span>buildInlines (textArray, styleContextStack)](#apidoc.element.pdfmake.textTools.prototype.buildInlines)
1.  [function <span class="apidocSignatureSpan">pdfmake.textTools.prototype.</span>sizeOfString (text, styleContextStack)](#apidoc.element.pdfmake.textTools.prototype.sizeOfString)

#### [module pdfmake.traversalTracker](#apidoc.module.pdfmake.traversalTracker)
1.  [function <span class="apidocSignatureSpan">pdfmake.</span>traversalTracker ()](#apidoc.element.pdfmake.traversalTracker.traversalTracker)

#### [module pdfmake.traversalTracker.prototype](#apidoc.module.pdfmake.traversalTracker.prototype)
1.  [function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>auto (event, cb, innerBlock)](#apidoc.element.pdfmake.traversalTracker.prototype.auto)
1.  [function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>emit (event)](#apidoc.element.pdfmake.traversalTracker.prototype.emit)
1.  [function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>startTracking (event, cb)](#apidoc.element.pdfmake.traversalTracker.prototype.startTracking)
1.  [function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>stopTracking (event, cb)](#apidoc.element.pdfmake.traversalTracker.prototype.stopTracking)



# <a name="apidoc.module.pdfmake"></a>[module pdfmake](#apidoc.module.pdfmake)

#### <a name="apidoc.element.pdfmake.docMeasure"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>docMeasure (fontProvider, styleDictionary, defaultStyle, imageMeasure, tableLayouts, images)](#apidoc.element.pdfmake.docMeasure)
- description and source-code
```javascript
function DocMeasure(fontProvider, styleDictionary, defaultStyle, imageMeasure, tableLayouts, images) {
	this.textTools = new TextTools(fontProvider);
	this.styleStack = new StyleContextStack(styleDictionary, defaultStyle);
	this.imageMeasure = imageMeasure;
	this.tableLayouts = tableLayouts;
	this.images = images;
	this.autoImageIndex = 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.documentContext"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>documentContext (pageSize, pageMargins)](#apidoc.element.pdfmake.documentContext)
- description and source-code
```javascript
function DocumentContext(pageSize, pageMargins) {
	this.pages = [];

	this.pageMargins = pageMargins;

	this.x = pageMargins.left;
	this.availableWidth = pageSize.width - pageMargins.left - pageMargins.right;
	this.availableHeight = 0;
	this.page = -1;

	this.snapshots = [];

	this.endingCell = null;

	this.tracker = new TraversalTracker();

	this.addPage(pageSize);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.elementWriter"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>elementWriter (context, tracker)](#apidoc.element.pdfmake.elementWriter)
- description and source-code
```javascript
function ElementWriter(context, tracker) {
	this.context = context;
	this.contextStack = [];
	this.tracker = tracker;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.fontProvider"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>fontProvider (fontDescriptors, pdfKitDoc)](#apidoc.element.pdfmake.fontProvider)
- description and source-code
```javascript
function FontProvider(fontDescriptors, pdfKitDoc) {
	this.fonts = {};
	this.pdfKitDoc = pdfKitDoc;
	this.fontCache = {};

	for (var font in fontDescriptors) {
		if (fontDescriptors.hasOwnProperty(font)) {
			var fontDef = fontDescriptors[font];

			this.fonts[font] = {
				normal: fontDef.normal,
				bold: fontDef.bold,
				italics: fontDef.italics,
				bolditalics: fontDef.bolditalics
			};
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.imageMeasure"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>imageMeasure (pdfKitDoc, imageDictionary)](#apidoc.element.pdfmake.imageMeasure)
- description and source-code
```javascript
function ImageMeasure(pdfKitDoc, imageDictionary) {
	this.pdfKitDoc = pdfKitDoc;
	this.imageDictionary = imageDictionary || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.layoutBuilder"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>layoutBuilder (pageSize, pageMargins, imageMeasure)](#apidoc.element.pdfmake.layoutBuilder)
- description and source-code
```javascript
function LayoutBuilder(pageSize, pageMargins, imageMeasure) {
	this.pageSize = pageSize;
	this.pageMargins = pageMargins;
	this.tracker = new TraversalTracker();
	this.imageMeasure = imageMeasure;
	this.tableLayouts = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.line"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>line (maxWidth)](#apidoc.element.pdfmake.line)
- description and source-code
```javascript
function Line(maxWidth) {
	this.maxWidth = maxWidth;
	this.leadingCut = 0;
	this.trailingCut = 0;
	this.inlineWidths = 0;
	this.inlines = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.pageElementWriter"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>pageElementWriter (context, tracker)](#apidoc.element.pdfmake.pageElementWriter)
- description and source-code
```javascript
function PageElementWriter(context, tracker) {
	this.transactionLevel = 0;
	this.repeatables = [];
	this.tracker = tracker;
	this.writer = new ElementWriter(context, tracker);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.styleContextStack"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>styleContextStack (styleDictionary, defaultStyle)](#apidoc.element.pdfmake.styleContextStack)
- description and source-code
```javascript
function StyleContextStack(styleDictionary, defaultStyle) {
	this.defaultStyle = defaultStyle || {};
	this.styleDictionary = styleDictionary;
	this.styleOverrides = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.tableProcessor"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>tableProcessor (tableNode)](#apidoc.element.pdfmake.tableProcessor)
- description and source-code
```javascript
function TableProcessor(tableNode) {
	this.tableNode = tableNode;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.textTools"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>textTools (fontProvider)](#apidoc.element.pdfmake.textTools)
- description and source-code
```javascript
function TextTools(fontProvider) {
	this.fontProvider = fontProvider;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.traversalTracker"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>traversalTracker ()](#apidoc.element.pdfmake.traversalTracker)
- description and source-code
```javascript
function TraversalTracker() {
	this.events = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.columnCalculator"></a>[module pdfmake.columnCalculator](#apidoc.module.pdfmake.columnCalculator)

#### <a name="apidoc.element.pdfmake.columnCalculator.buildColumnWidths"></a>[function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>buildColumnWidths (columns, availableWidth)](#apidoc.element.pdfmake.columnCalculator.buildColumnWidths)
- description and source-code
```javascript
function buildColumnWidths(columns, availableWidth) {
	var autoColumns = [],
		autoMin = 0, autoMax = 0,
		starColumns = [],
		starMaxMin = 0,
		starMaxMax = 0,
		fixedColumns = [],
		initial_availableWidth = availableWidth;

	columns.forEach(function (column) {
		if (isAutoColumn(column)) {
			autoColumns.push(column);
			autoMin += column._minWidth;
			autoMax += column._maxWidth;
		} else if (isStarColumn(column)) {
			starColumns.push(column);
			starMaxMin = Math.max(starMaxMin, column._minWidth);
			starMaxMax = Math.max(starMaxMax, column._maxWidth);
		} else {
			fixedColumns.push(column);
		}
	});

	fixedColumns.forEach(function (col) {
		// width specified as %
		if (typeof col.width === 'string' && /\d+%/.test(col.width)) {
			col.width = parseFloat(col.width) * initial_availableWidth / 100;
		}
		if (col.width < (col._minWidth) && col.elasticWidth) {
			col._calcWidth = col._minWidth;
		} else {
			col._calcWidth = col.width;
		}

		availableWidth -= col._calcWidth;
	});

	// http://www.freesoft.org/CIE/RFC/1942/18.htm
	// http://www.w3.org/TR/CSS2/tables.html#width-layout
	// http://dev.w3.org/csswg/css3-tables-algorithms/Overview.src.htm
	var minW = autoMin + starMaxMin * starColumns.length;
	var maxW = autoMax + starMaxMax * starColumns.length;
	if (minW >= availableWidth) {
		// case 1 - there's no way to fit all columns within available width
		// that's actually pretty bad situation with PDF as we have no horizontal scroll
		// no easy workaround (unless we decide, in the future, to split single words)
		// currently we simply use minWidths for all columns
		autoColumns.forEach(function (col) {
			col._calcWidth = col._minWidth;
		});

		starColumns.forEach(function (col) {
			col._calcWidth = starMaxMin; // starMaxMin already contains padding
		});
	} else {
		if (maxW < availableWidth) {
			// case 2 - we can fit rest of the table within available space
			autoColumns.forEach(function (col) {
				col._calcWidth = col._maxWidth;
				availableWidth -= col._calcWidth;
			});
		} else {
			// maxW is too large, but minW fits within available width
			var W = availableWidth - minW;
			var D = maxW - minW;

			autoColumns.forEach(function (col) {
				var d = col._maxWidth - col._minWidth;
				col._calcWidth = col._minWidth + d * W / D;
				availableWidth -= col._calcWidth;
			});
		}

		if (starColumns.length > 0) {
			var starSize = availableWidth / starColumns.length;

			starColumns.forEach(function (col) {
				col._calcWidth = starSize;
			});
		}
	}
}
```
- example usage
```shell
...
	var availableWidth = this.writer.context().availableWidth;
	var gaps = gapArray(columnNode._gap);

	if (gaps) {
		availableWidth -= (gaps.length - 1) * columnNode._gap;
	}

	ColumnCalculator.buildColumnWidths(columns, availableWidth);
	var result = this.processRow(columns, columns, gaps);
	addAll(columnNode.positions, result.positions);


	function gapArray(gap) {
		if (!gap) {
			return null;
...
```

#### <a name="apidoc.element.pdfmake.columnCalculator.isAutoColumn"></a>[function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>isAutoColumn (column)](#apidoc.element.pdfmake.columnCalculator.isAutoColumn)
- description and source-code
```javascript
function isAutoColumn(column) {
	return column.width === 'auto';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.columnCalculator.isStarColumn"></a>[function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>isStarColumn (column)](#apidoc.element.pdfmake.columnCalculator.isStarColumn)
- description and source-code
```javascript
function isStarColumn(column) {
	return column.width === null || column.width === undefined || column.width === '*' || column.width === 'star';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.columnCalculator.measureMinMax"></a>[function <span class="apidocSignatureSpan">pdfmake.columnCalculator.</span>measureMinMax (columns)](#apidoc.element.pdfmake.columnCalculator.measureMinMax)
- description and source-code
```javascript
function measureMinMax(columns) {
	var result = {min: 0, max: 0};

	var maxStar = {min: 0, max: 0};
	var starCount = 0;

	for (var i = 0, l = columns.length; i < l; i++) {
		var c = columns[i];

		if (isStarColumn(c)) {
			maxStar.min = Math.max(maxStar.min, c._minWidth);
			maxStar.max = Math.max(maxStar.max, c._maxWidth);
			starCount++;
		} else if (isAutoColumn(c)) {
			result.min += c._minWidth;
			result.max += c._maxWidth;
		} else {
			result.min += ((c.width !== undefined && c.width) || c._minWidth);
			result.max += ((c.width !== undefined && c.width) || c._maxWidth);
		}
	}

	if (starCount) {
		result.min += starCount * maxStar.min;
		result.max += starCount * maxStar.max;
	}

	return result;
}
```
- example usage
```shell
...
	var columns = node.columns;
	node._gap = this.styleStack.getProperty('columnGap') || 0;

	for (var i = 0, l = columns.length; i < l; i++) {
		columns[i] = this.measureNode(columns[i]);
	}

	var measures = ColumnCalculator.measureMinMax(columns);

	node._minWidth = measures.min + node._gap * (columns.length - 1);
	node._maxWidth = measures.max + node._gap * (columns.length - 1);

	return node;
};
...
```



# <a name="apidoc.module.pdfmake.docMeasure"></a>[module pdfmake.docMeasure](#apidoc.module.pdfmake.docMeasure)

#### <a name="apidoc.element.pdfmake.docMeasure.docMeasure"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>docMeasure (fontProvider, styleDictionary, defaultStyle, imageMeasure, tableLayouts, images)](#apidoc.element.pdfmake.docMeasure.docMeasure)
- description and source-code
```javascript
function DocMeasure(fontProvider, styleDictionary, defaultStyle, imageMeasure, tableLayouts, images) {
	this.textTools = new TextTools(fontProvider);
	this.styleStack = new StyleContextStack(styleDictionary, defaultStyle);
	this.imageMeasure = imageMeasure;
	this.tableLayouts = tableLayouts;
	this.images = images;
	this.autoImageIndex = 1;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.docMeasure.prototype"></a>[module pdfmake.docMeasure.prototype](#apidoc.module.pdfmake.docMeasure.prototype)

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.buildOrderedMarker"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>buildOrderedMarker (counter, styleStack, type, separator)](#apidoc.element.pdfmake.docMeasure.prototype.buildOrderedMarker)
- description and source-code
```javascript
buildOrderedMarker = function (counter, styleStack, type, separator) {
	function prepareAlpha(counter) {
		function toAlpha(num) {
			return (num >= 26 ? toAlpha((num / 26 >> 0) - 1) : '') + 'abcdefghijklmnopqrstuvwxyz'[num % 26 >> 0];
		}

		if (counter < 1) {
			return counter.toString();
		}

		return toAlpha(counter - 1);
	}

	function prepareRoman(counter) {
		if (counter < 1 || counter > 4999) {
			return counter.toString();
		}
		var num = counter;
		var lookup = {M: 1000, CM: 900, D: 500, CD: 400, C: 100, XC: 90, L: 50, XL: 40, X: 10, IX: 9, V: 5, IV: 4, I: 1}, roman = '',
i;
		for (i in lookup) {
			while (num >= lookup[i]) {
				roman += i;
				num -= lookup[i];
			}
		}
		return roman;
	}

	function prepareDecimal(counter) {
		return counter.toString();
	}

	var counterText;
	switch (type) {
		case 'none':
			counterText = null;
			break;

		case 'upper-alpha':
			counterText = prepareAlpha(counter).toUpperCase();
			break;

		case 'lower-alpha':
			counterText = prepareAlpha(counter);
			break;

		case 'upper-roman':
			counterText = prepareRoman(counter);
			break;

		case 'lower-roman':
			counterText = prepareRoman(counter).toLowerCase();
			break;

		case 'decimal':
		default:
			counterText = prepareDecimal(counter);
			break;
	}

	if (counterText === null) {
		return {};
	}

	if (separator) {
		if (Array.isArray(separator)) {
			if (separator[0]) {
				counterText = separator[0] + counterText;
			}

			if (separator[1]) {
				counterText += separator[1];
			}
			counterText += ' ';
		} else {
			counterText += separator + ' ';
		}
	}

	var textArray = {text: counterText};
	var markerColor = styleStack.getProperty('markerColor');
	if (markerColor) {
		textArray.color = markerColor;
	}

	return {_inlines: this.textTools.buildInlines(textArray, styleStack).items};
}
```
- example usage
```shell
...
	node._maxWidth = 0;

	var counter = node.start;
	for (var i = 0, l = items.length; i < l; i++) {
		var item = items[i] = this.measureNode(items[i]);

		if (!item.ol && !item.ul) {
			item.listMarker = this.buildOrderedMarker(item.counter || counter, style, node.type, node.separator);
			if (item.listMarker._inlines) {
				node._gapSize.width = Math.max(node._gapSize.width, item.listMarker._inlines[0].width);
			}
		}  // TODO: else - nested lists numbering

		node._minWidth = Math.max(node._minWidth, items[i]._minWidth);
		node._maxWidth = Math.max(node._maxWidth, items[i]._maxWidth);
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.buildUnorderedMarker"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>buildUnorderedMarker (styleStack, gapSize, type)](#apidoc.element.pdfmake.docMeasure.prototype.buildUnorderedMarker)
- description and source-code
```javascript
buildUnorderedMarker = function (styleStack, gapSize, type) {
	function buildDisc(gapSize, color) {
		// TODO: ascender-based calculations
		var radius = gapSize.fontSize / 6;
		return {
			canvas: [{
					x: radius,
					y: (gapSize.height / gapSize.lineHeight) + gapSize.descender - gapSize.fontSize / 3,
					r1: radius,
					r2: radius,
					type: 'ellipse',
					color: color
				}]
		};
	}

	function buildSquare(gapSize, color) {
		// TODO: ascender-based calculations
		var size = gapSize.fontSize / 3;
		return {
			canvas: [{
					x: 0,
					y: (gapSize.height / gapSize.lineHeight) + gapSize.descender - (gapSize.fontSize / 3) - (size / 2),
					h: size,
					w: size,
					type: 'rect',
					color: color
				}]
		};
	}

	function buildCircle(gapSize, color) {
		// TODO: ascender-based calculations
		var radius = gapSize.fontSize / 6;
		return {
			canvas: [{
					x: radius,
					y: (gapSize.height / gapSize.lineHeight) + gapSize.descender - gapSize.fontSize / 3,
					r1: radius,
					r2: radius,
					type: 'ellipse',
					lineColor: color
				}]
		};
	}

	var marker;
	var color = styleStack.getProperty('markerColor') || styleStack.getProperty('color') || 'black';

	switch (type) {
		case 'circle':
			marker = buildCircle(gapSize, color);
			break;

		case 'square':
			marker = buildSquare(gapSize, color);
			break;

		case 'none':
			marker = {};
			break;

		case 'disc':
		default:
			marker = buildDisc(gapSize, color);
			break;
	}

	marker._minWidth = marker._maxWidth = gapSize.width;
	marker._minHeight = marker._maxHeight = gapSize.height;

	return marker;
}
```
- example usage
```shell
...
	node._minWidth = 0;
	node._maxWidth = 0;

	for (var i = 0, l = items.length; i < l; i++) {
		var item = items[i] = this.measureNode(items[i]);

		if (!item.ol && !item.ul) {
			item.listMarker = this.buildUnorderedMarker(style, node._gapSize, node.type);
		}

		node._minWidth = Math.max(node._minWidth, items[i]._minWidth + node._gapSize.width);
		node._maxWidth = Math.max(node._maxWidth, items[i]._maxWidth + node._gapSize.width);
	}

	return node;
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.convertIfBase64Image"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>convertIfBase64Image (node)](#apidoc.element.pdfmake.docMeasure.prototype.convertIfBase64Image)
- description and source-code
```javascript
convertIfBase64Image = function (node) {
	if (/^data:image\/(jpeg|jpg|png);base64,/.test(node.image)) {
		var label = '$$pdfmake$$' + this.autoImageIndex++;
		this.images[label] = node.image;
		node.image = label;
	}
}
```
- example usage
```shell
...
		this.images[label] = node.image;
		node.image = label;
	}
};

DocMeasure.prototype.measureImage = function (node) {
	if (this.images) {
		this.convertIfBase64Image(node);
	}

	var imageSize = this.imageMeasure.measureImage(node.image);

	if (node.fit) {
		var factor = (imageSize.width / imageSize.height > node.fit[0] / node.fit[1]) ? node.fit[0] / imageSize.width : node.fit[1] /
imageSize.height;
		node._width = node._minWidth = node._maxWidth = imageSize.width * factor;
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.gapSizeForList"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>gapSizeForList ()](#apidoc.element.pdfmake.docMeasure.prototype.gapSizeForList)
- description and source-code
```javascript
gapSizeForList = function () {
	return this.textTools.sizeOfString('9. ', this.styleStack);
}
```
- example usage
```shell
...
	return {_inlines: this.textTools.buildInlines(textArray, styleStack).items};
};

DocMeasure.prototype.measureUnorderedList = function (node) {
	var style = this.styleStack.clone();
	var items = node.ul;
	node.type = node.type || 'disc';
	node._gapSize = this.gapSizeForList();
	node._minWidth = 0;
	node._maxWidth = 0;

	for (var i = 0, l = items.length; i < l; i++) {
		var item = items[i] = this.measureNode(items[i]);

		if (!item.ol && !item.ul) {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureCanvas"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureCanvas (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureCanvas)
- description and source-code
```javascript
measureCanvas = function (node) {
	var w = 0, h = 0;

	for (var i = 0, l = node.canvas.length; i < l; i++) {
		var vector = node.canvas[i];

		switch (vector.type) {
			case 'ellipse':
				w = Math.max(w, vector.x + vector.r1);
				h = Math.max(h, vector.y + vector.r2);
				break;
			case 'rect':
				w = Math.max(w, vector.x + vector.w);
				h = Math.max(h, vector.y + vector.h);
				break;
			case 'line':
				w = Math.max(w, vector.x1, vector.x2);
				h = Math.max(h, vector.y1, vector.y2);
				break;
			case 'polyline':
				for (var i2 = 0, l2 = vector.points.length; i2 < l2; i2++) {
					w = Math.max(w, vector.points[i2].x);
					h = Math.max(h, vector.points[i2].y);
				}
				break;
		}
	}

	node._minWidth = node._maxWidth = w;
	node._minHeight = node._maxHeight = h;

	return node;
}
```
- example usage
```shell
...
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
			return extendMargins(self.measureQr(node));
		} else {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}
	});
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureColumns"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureColumns (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureColumns)
- description and source-code
```javascript
measureColumns = function (node) {
	var columns = node.columns;
	node._gap = this.styleStack.getProperty('columnGap') || 0;

	for (var i = 0, l = columns.length; i < l; i++) {
		columns[i] = this.measureNode(columns[i]);
	}

	var measures = ColumnCalculator.measureMinMax(columns);

	node._minWidth = measures.min + node._gap * (columns.length - 1);
	node._maxWidth = measures.max + node._gap * (columns.length - 1);

	return node;
}
```
- example usage
```shell
...
	var self = this;

	return this.styleStack.auto(node, function () {
		// TODO: refactor + rethink whether this is the proper way to handle margins
		node._margin = getNodeMargin(node);

		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureDocument"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureDocument (docStructure)](#apidoc.element.pdfmake.docMeasure.prototype.measureDocument)
- description and source-code
```javascript
measureDocument = function (docStructure) {
	return this.measureNode(docStructure);
}
```
- example usage
```shell
...

	return result.pages;
};

LayoutBuilder.prototype.tryLayoutDocument = function (docStructure, fontProvider, styleDictionary, defaultStyle, background, header
, footer, images, watermark, pageBreakBeforeFct) {

	this.linearNodeList = [];
	docStructure = this.docMeasure.measureDocument(docStructure);

	this.writer = new PageElementWriter(
		new DocumentContext(this.pageSize, this.pageMargins), this.tracker);

	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureImage"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureImage (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureImage)
- description and source-code
```javascript
measureImage = function (node) {
	if (this.images) {
		this.convertIfBase64Image(node);
	}

	var imageSize = this.imageMeasure.measureImage(node.image);

	if (node.fit) {
		var factor = (imageSize.width / imageSize.height > node.fit[0] / node.fit[1]) ? node.fit[0] / imageSize.width : node.fit[1] /
imageSize.height;
		node._width = node._minWidth = node._maxWidth = imageSize.width * factor;
		node._height = imageSize.height * factor;
	} else {
		node._width = node._minWidth = node._maxWidth = node.width || imageSize.width;
		node._height = node.height || (imageSize.height * node._width / imageSize.width);
	}

	node._alignment = this.styleStack.getProperty('alignment');
	return node;
}
```
- example usage
```shell
...
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
			return extendMargins(self.measureQr(node));
		} else {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureLeaf"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureLeaf (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureLeaf)
- description and source-code
```javascript
measureLeaf = function (node) {

	// Make sure style properties of the node itself are considered when building inlines.
	// We could also just pass [node] to buildInlines, but that fails for bullet points.
	var styleStack = this.styleStack.clone();
	styleStack.push(node);

	var data = this.textTools.buildInlines(node.text, styleStack);

	node._inlines = data.items;
	node._minWidth = data.minWidth;
	node._maxWidth = data.maxWidth;

	return node;
}
```
- example usage
```shell
...
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
			return extendMargins(self.measureQr(node));
		} else {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureNode"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureNode (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureNode)
- description and source-code
```javascript
measureNode = function (node) {
	// expand shortcuts
	if (Array.isArray(node)) {
		node = {stack: node};
	} else if (typeof node === 'string' || node instanceof String) {
		node = {text: node};
	} else if (typeof node === 'number' || typeof node === 'boolean') {
		node = {text: node.toString()};
	} else if (node === null) {
		node = {text: ''};
	}

	// Deal with empty nodes to prevent crash in getNodeMargin
	if (Object.keys(node).length === 0) {
		// A warning could be logged: console.warn('pdfmake: Empty node, ignoring it');
		node = {text: ''};
	}

	var self = this;

	return this.styleStack.auto(node, function () {
		// TODO: refactor + rethink whether this is the proper way to handle margins
		node._margin = getNodeMargin(node);

		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
			return extendMargins(self.measureQr(node));
		} else {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}
	});

	function extendMargins(node) {
		var margin = node._margin;

		if (margin) {
			node._minWidth += margin[0] + margin[2];
			node._maxWidth += margin[0] + margin[2];
		}

		return node;
	}

	function getNodeMargin() {

		function processSingleMargins(node, currentMargin) {
			if (node.marginLeft || node.marginTop || node.marginRight || node.marginBottom) {
				return [
					node.marginLeft || currentMargin[0] || 0,
					node.marginTop || currentMargin[1] || 0,
					node.marginRight || currentMargin[2] || 0,
					node.marginBottom || currentMargin[3] || 0
				];
			}
			return currentMargin;
		}

		function flattenStyleArray(styleArray) {
			var flattenedStyles = {};
			for (var i = styleArray.length - 1; i >= 0; i--) {
				var styleName = styleArray[i];
				var style = self.styleStack.styleDictionary[styleName];
				for (var key in style) {
					if (style.hasOwnProperty(key)) {
						flattenedStyles[key] = style[key];
					}
				}
			}
			return flattenedStyles;
		}

		function convertMargin(margin) {
			if (typeof margin === 'number' || margin instanceof Number) {
				margin = [margin, margin, margin, margin];
			} else if (Array.isArray(margin)) {
				if (margin.length === 2) {
					margin = [margin[0], margin[1], margin[0], margin[1]];
				}
			}
			return margin;
		}

		var margin = [undefined, undefined, undefined, undefined];

		if (node.style) {
			var styleArray = (Array.isArray(node.style)) ? node.style : [node.style];
			var flattenedStyleArray = flattenStyleArray(styleArray);

			if (flattenedStyleArray) {
				margin = processSingleMargins(flattenedStyleArray, margin);
			}

			if (flattenedStyleArray.margin) {
				margin = convertMargin(flattenedStyleArray.margin);
			}
		}

		margin = processSingleMargins(node, margin);

		if (node.margin) {
			margin = convertMargin(node.margin);
		}

		if (margin[0] === undefined && margin[1] === undefined && margin[2] === undefined && margin[3] === undefined) {
			return null;
		} else {
			return margin;
		}
	}
}
```
- example usage
```shell
...
/**
 * Measures all nodes and sets min/max-width properties required for the second
 * layout-pass.
 * @param  {Object} docStructure document-definition-object
 * @return {Object}              document-measurement-object
 */
DocMeasure.prototype.measureDocument = function (docStructure) {
	return this.measureNode(docStructure);
};

DocMeasure.prototype.measureNode = function (node) {
	// expand shortcuts
	if (Array.isArray(node)) {
		node = {stack: node};
	} else if (typeof node === 'string' || node instanceof String) {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureOrderedList"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureOrderedList (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureOrderedList)
- description and source-code
```javascript
measureOrderedList = function (node) {
	var style = this.styleStack.clone();
	var items = node.ol;
	node.type = node.type || 'decimal';
	node.separator = node.separator || '.';
	node.reversed = node.reversed || false;
	if (!node.start) {
		node.start = node.reversed ? items.length : 1;
	}
	node._gapSize = this.gapSizeForList();
	node._minWidth = 0;
	node._maxWidth = 0;

	var counter = node.start;
	for (var i = 0, l = items.length; i < l; i++) {
		var item = items[i] = this.measureNode(items[i]);

		if (!item.ol && !item.ul) {
			item.listMarker = this.buildOrderedMarker(item.counter || counter, style, node.type, node.separator);
			if (item.listMarker._inlines) {
				node._gapSize.width = Math.max(node._gapSize.width, item.listMarker._inlines[0].width);
			}
		}  // TODO: else - nested lists numbering

		node._minWidth = Math.max(node._minWidth, items[i]._minWidth);
		node._maxWidth = Math.max(node._maxWidth, items[i]._maxWidth);

		if (node.reversed) {
			counter--;
		} else {
			counter++;
		}
	}

	node._minWidth += node._gapSize.width;
	node._maxWidth += node._gapSize.width;

	for (var i = 0, l = items.length; i < l; i++) {
		var item = items[i];
		if (!item.ol && !item.ul) {
			item.listMarker._minWidth = item.listMarker._maxWidth = node._gapSize.width;
		}
	}

	return node;
}
```
- example usage
```shell
...
		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureQr"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureQr (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureQr)
- description and source-code
```javascript
measureQr = function (node) {
	node = qrEncoder.measure(node);
	node._alignment = this.styleStack.getProperty('alignment');
	return node;
}
```
- example usage
```shell
...
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
			return extendMargins(self.measureQr(node));
		} else {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}
	});

	function extendMargins(node) {
		var margin = node._margin;
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureTable"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureTable (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureTable)
- description and source-code
```javascript
measureTable = function (node) {
	extendTableWidths(node);
	node._layout = getLayout(this.tableLayouts);
	node._offsets = getOffsets(node._layout);

	var colSpans = [];
	var col, row, cols, rows;

	for (col = 0, cols = node.table.body[0].length; col < cols; col++) {
		var c = node.table.widths[col];
		c._minWidth = 0;
		c._maxWidth = 0;

		for (row = 0, rows = node.table.body.length; row < rows; row++) {
			var rowData = node.table.body[row];
			var data = rowData[col];
			if (data === undefined) {
				console.error('Malformed table row ', rowData, 'in node ', node);
				throw 'Malformed table row, a cell is undefined.';
			}
			if (data === null) { // transform to object
				data = '';
			}
			if (!data._span) {
				data = rowData[col] = this.styleStack.auto(data, measureCb(this, data));

				if (data.colSpan && data.colSpan > 1) {
					markSpans(rowData, col, data.colSpan);
					colSpans.push({col: col, span: data.colSpan, minWidth: data._minWidth, maxWidth: data._maxWidth});
				} else {
					c._minWidth = Math.max(c._minWidth, data._minWidth);
					c._maxWidth = Math.max(c._maxWidth, data._maxWidth);
				}
			}

			if (data.rowSpan && data.rowSpan > 1) {
				markVSpans(node.table, row, col, data.rowSpan);
			}
		}
	}

	extendWidthsForColSpans();

	var measures = ColumnCalculator.measureMinMax(node.table.widths);

	node._minWidth = measures.min + node._offsets.total;
	node._maxWidth = measures.max + node._offsets.total;

	return node;

	function measureCb(_this, data) {
		return function () {
			if (data !== null && typeof data === 'object') {
				data.fillColor = _this.styleStack.getProperty('fillColor');
			}
			return _this.measureNode(data);
		};
	}

	function getLayout(tableLayouts) {
		var layout = node.layout;

		if (typeof node.layout === 'string' || node instanceof String) {
			layout = tableLayouts[layout];
		}

		/*jshint unused: false */
		var defaultLayout = {
			hLineWidth: function (i, node) {
				return 1;
			},
			vLineWidth: function (i, node) {
				return 1;
			},
			hLineColor: function (i, node) {
				return 'black';
			},
			vLineColor: function (i, node) {
				return 'black';
			},
			paddingLeft: function (i, node) {
				return 4;
			},
			paddingRight: function (i, node) {
				return 4;
			},
			paddingTop: function (i, node) {
				return 2;
			},
			paddingBottom: function (i, node) {
				return 2;
			},
			fillColor: function (i, node) {
				return null;
			},
			defaultBorder: true
		};

		return pack(defaultLayout, layout);
	}

	function getOffsets(layout) {
		var offsets = [];
		var totalOffset = 0;
		var prevRightPadding = 0;

		for (var i = 0, l = node.table.widths.length; i < l; i++) {
			var lOffset = prevRightPadding + layout.vLineWidth(i, node) + layout.paddingLeft(i, node);
			offsets.push(lOffset);
			totalOffset += lOffset;
			prevRightPadding = layout.paddingRight(i, node);
		}

		totalOffset += prevRightPadding + layout.vLineWidth(node.table.widths.length, node);

		return {
			total: totalOffset,
			offsets: offsets
		};
	}

	function extendWidthsForColSpans() {
		var q, j;

		for (var i = 0, l = colSpans.length; i < l; i++) {
			var span = colSpans[i];

			var currentMinMax = getMinMax(span.col, span.span, node._offsets);
			var minDifference = span.minWidth - currentMinMax.minWidth;
			var maxDifference = span.maxWidth - currentMinMax.maxWidth;

			if (minDifference > 0) {
				q = minDifference / span.span;

				for (j = 0; j < span.span; j++) {
					node.table.widths[span.col + j]._minWidth += q;
				}
			}

			if (maxDifference > 0) {
				q = maxDifference / span.span;

				for (j = 0; j < span.span; j++) {
					node.table.widths[span.col + j]._maxWidth += q;
				}
			}
		}
	}

	function getMinMax(col, span, offsets) {
		var result = {minWidth: 0, maxWidth: 0};

		for (var i = 0; i < span; i++) {
			result.minWidth += node.table.widths[col + i]._minWidth + (i ? offsets.offsets[col + i] : 0);
			result.maxWidth += node.table.widths[col + ...
```
- example usage
```shell
...
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureUnorderedList"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureUnorderedList (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureUnorderedList)
- description and source-code
```javascript
measureUnorderedList = function (node) {
	var style = this.styleStack.clone();
	var items = node.ul;
	node.type = node.type || 'disc';
	node._gapSize = this.gapSizeForList();
	node._minWidth = 0;
	node._maxWidth = 0;

	for (var i = 0, l = items.length; i < l; i++) {
		var item = items[i] = this.measureNode(items[i]);

		if (!item.ol && !item.ul) {
			item.listMarker = this.buildUnorderedMarker(style, node._gapSize, node.type);
		}

		node._minWidth = Math.max(node._minWidth, items[i]._minWidth + node._gapSize.width);
		node._maxWidth = Math.max(node._maxWidth, items[i]._maxWidth + node._gapSize.width);
	}

	return node;
}
```
- example usage
```shell
...
		node._margin = getNodeMargin(node);

		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
...
```

#### <a name="apidoc.element.pdfmake.docMeasure.prototype.measureVerticalContainer"></a>[function <span class="apidocSignatureSpan">pdfmake.docMeasure.prototype.</span>measureVerticalContainer (node)](#apidoc.element.pdfmake.docMeasure.prototype.measureVerticalContainer)
- description and source-code
```javascript
measureVerticalContainer = function (node) {
	var items = node.stack;

	node._minWidth = 0;
	node._maxWidth = 0;

	for (var i = 0, l = items.length; i < l; i++) {
		items[i] = this.measureNode(items[i]);

		node._minWidth = Math.max(node._minWidth, items[i]._minWidth);
		node._maxWidth = Math.max(node._maxWidth, items[i]._maxWidth);
	}

	return node;
}
```
- example usage
```shell
...
	return this.styleStack.auto(node, function () {
		// TODO: refactor + rethink whether this is the proper way to handle margins
		node._margin = getNodeMargin(node);

		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
		} else if (node.ul) {
			return extendMargins(self.measureUnorderedList(node));
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
...
```



# <a name="apidoc.module.pdfmake.documentContext"></a>[module pdfmake.documentContext](#apidoc.module.pdfmake.documentContext)

#### <a name="apidoc.element.pdfmake.documentContext.documentContext"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>documentContext (pageSize, pageMargins)](#apidoc.element.pdfmake.documentContext.documentContext)
- description and source-code
```javascript
function DocumentContext(pageSize, pageMargins) {
	this.pages = [];

	this.pageMargins = pageMargins;

	this.x = pageMargins.left;
	this.availableWidth = pageSize.width - pageMargins.left - pageMargins.right;
	this.availableHeight = 0;
	this.page = -1;

	this.snapshots = [];

	this.endingCell = null;

	this.tracker = new TraversalTracker();

	this.addPage(pageSize);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.documentContext.prototype"></a>[module pdfmake.documentContext.prototype](#apidoc.module.pdfmake.documentContext.prototype)

#### <a name="apidoc.element.pdfmake.documentContext.prototype.addMargin"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>addMargin (left, right)](#apidoc.element.pdfmake.documentContext.prototype.addMargin)
- description and source-code
```javascript
addMargin = function (left, right) {
	this.x += left;
	this.availableWidth -= left + (right || 0);
}
```
- example usage
```shell
...

		if (node.pageBreak === 'before') {
			self.writer.moveToNextPage(node.pageOrientation);
		}

		if (margin) {
			self.writer.context().moveDown(margin[1]);
			self.writer.context().addMargin(margin[0], margin[2]);
		}

		callback();

		if (margin) {
			self.writer.context().addMargin(-margin[0], -margin[2]);
			self.writer.context().moveDown(margin[3]);
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.addPage"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>addPage (pageSize)](#apidoc.element.pdfmake.documentContext.prototype.addPage)
- description and source-code
```javascript
addPage = function (pageSize) {
	var page = {items: [], pageSize: pageSize};
	this.pages.push(page);
	this.page = this.pages.length - 1;
	this.initializePage();

	this.tracker.emit('pageAdded');

	return page;
}
```
- example usage
```shell
...

	this.snapshots = [];

	this.endingCell = null;

	this.tracker = new TraversalTracker();

	this.addPage(pageSize);
}

DocumentContext.prototype.beginColumnGroup = function () {
	this.snapshots.push({
		x: this.x,
		y: this.y,
		availableHeight: this.availableHeight,
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.beginColumn"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>beginColumn (width, offset, endingCell)](#apidoc.element.pdfmake.documentContext.prototype.beginColumn)
- description and source-code
```javascript
beginColumn = function (width, offset, endingCell) {
	var saved = this.snapshots[this.snapshots.length - 1];

	this.calculateBottomMost(saved);

	this.endingCell = endingCell;
	this.page = saved.page;
	this.x = this.x + this.lastColumnWidth + (offset || 0);
	this.y = saved.y;
	this.availableWidth = width;	//saved.availableWidth - offset;
	this.availableHeight = saved.availableHeight;

	this.lastColumnWidth = width;
}
```
- example usage
```shell
...

			if (column.colSpan && column.colSpan > 1) {
				for (var j = 1; j < column.colSpan; j++) {
					width += widths[++i]._calcWidth + gaps[i];
				}
			}

			self.writer.context().beginColumn(width, leftOffset, getEndingCell(column, i));
			if (!column._span) {
				self.processNode(column);
				addAll(positions, column.positions);
			} else if (column._columnEndingContext) {
				// row-span ending
				self.writer.context().markEnding(column);
			}
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.beginColumnGroup"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>beginColumnGroup ()](#apidoc.element.pdfmake.documentContext.prototype.beginColumnGroup)
- description and source-code
```javascript
beginColumnGroup = function () {
	this.snapshots.push({
		x: this.x,
		y: this.y,
		availableHeight: this.availableHeight,
		availableWidth: this.availableWidth,
		page: this.page,
		bottomMost: {y: this.y, page: this.page},
		endingCell: this.endingCell,
		lastColumnWidth: this.lastColumnWidth
	});

	this.lastColumnWidth = 0;
}
```
- example usage
```shell
...
LayoutBuilder.prototype.processRow = function (columns, widths, gaps, tableBody, tableRow) {
	var self = this;
	var pageBreaks = [], positions = [];

	this.tracker.auto('pageChanged', storePageBreakData, function () {
		widths = widths || columns;

		self.writer.context().beginColumnGroup();

		for (var i = 0, l = columns.length; i < l; i++) {
			var column = columns[i];
			var width = widths[i]._calcWidth;
			var leftOffset = colLeftOffset(i);

			if (column.colSpan && column.colSpan > 1) {
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.beginDetachedBlock"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>beginDetachedBlock ()](#apidoc.element.pdfmake.documentContext.prototype.beginDetachedBlock)
- description and source-code
```javascript
beginDetachedBlock = function () {
	this.snapshots.push({
		x: this.x,
		y: this.y,
		availableHeight: this.availableHeight,
		availableWidth: this.availableWidth,
		page: this.page,
		endingCell: this.endingCell,
		lastColumnWidth: this.lastColumnWidth
	});
}
```
- example usage
```shell
...

	this.linearNodeList.push(node);
	decorateNode(node);

	applyMargins(function () {
		var absPosition = node.absolutePosition;
		if (absPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo(absPosition.x || 0, absPosition.y || 0);
		}

		var relPosition = node.relativePosition;
		if (relPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo((relPosition.x || 0) + self.writer.context().x, (relPosition.y || 0) + self.writer.context().y);
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.calculateBottomMost"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>calculateBottomMost (destContext)](#apidoc.element.pdfmake.documentContext.prototype.calculateBottomMost)
- description and source-code
```javascript
calculateBottomMost = function (destContext) {
	if (this.endingCell) {
		this.saveContextInEndingCell(this.endingCell);
		this.endingCell = null;
	} else {
		destContext.bottomMost = bottomMostContext(this, destContext.bottomMost);
	}
}
```
- example usage
```shell
...

	this.lastColumnWidth = 0;
};

DocumentContext.prototype.beginColumn = function (width, offset, endingCell) {
	var saved = this.snapshots[this.snapshots.length - 1];

	this.calculateBottomMost(saved);

	this.endingCell = endingCell;
	this.page = saved.page;
	this.x = this.x + this.lastColumnWidth + (offset || 0);
	this.y = saved.y;
	this.availableWidth = width;	//saved.availableWidth - offset;
	this.availableHeight = saved.availableHeight;
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.completeColumnGroup"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>completeColumnGroup ()](#apidoc.element.pdfmake.documentContext.prototype.completeColumnGroup)
- description and source-code
```javascript
completeColumnGroup = function () {
	var saved = this.snapshots.pop();

	this.calculateBottomMost(saved);

	this.endingCell = null;
	this.x = saved.x;
	this.y = saved.bottomMost.y;
	this.page = saved.bottomMost.page;
	this.availableWidth = saved.availableWidth;
	this.availableHeight = saved.bottomMost.availableHeight;
	this.lastColumnWidth = saved.lastColumnWidth;
}
```
- example usage
```shell
...
				addAll(positions, column.positions);
			} else if (column._columnEndingContext) {
				// row-span ending
				self.writer.context().markEnding(column);
			}
		}

		self.writer.context().completeColumnGroup();
	});

	return {pageBreaks: pageBreaks, positions: positions};

	function storePageBreakData(data) {
		var pageDesc;
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.endDetachedBlock"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>endDetachedBlock ()](#apidoc.element.pdfmake.documentContext.prototype.endDetachedBlock)
- description and source-code
```javascript
endDetachedBlock = function () {
	var saved = this.snapshots.pop();

	this.x = saved.x;
	this.y = saved.y;
	this.availableWidth = saved.availableWidth;
	this.availableHeight = saved.availableHeight;
	this.page = saved.page;
	this.endingCell = saved.endingCell;
	this.lastColumnWidth = saved.lastColumnWidth;
}
```
- example usage
```shell
...
		} else if (node.qr) {
			self.processQr(node);
		} else if (!node._span) {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}

		if (absPosition || relPosition) {
			self.writer.context().endDetachedBlock();
		}
	});

	function applyMargins(callback) {
		var margin = node._margin;

		if (node.pageBreak === 'before') {
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.getCurrentPage"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>getCurrentPage ()](#apidoc.element.pdfmake.documentContext.prototype.getCurrentPage)
- description and source-code
```javascript
getCurrentPage = function () {
	if (this.page < 0 || this.page >= this.pages.length) {
		return null;
	}

	return this.pages[this.page];
}
```
- example usage
```shell
...
	this.availableHeight -= offset;

	return this.availableHeight > 0;
};

DocumentContext.prototype.initializePage = function () {
	this.y = this.pageMargins.top;
	this.availableHeight = this.getCurrentPage().pageSize.height - this.pageMargins.top - this.pageMargins.bottom;
	this.pageSnapshot().availableWidth = this.getCurrentPage().pageSize.width - this.pageMargins.left - this.pageMargins.right;
};

DocumentContext.prototype.pageSnapshot = function () {
	if (this.snapshots[0]) {
		return this.snapshots[0];
	} else {
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.getCurrentPosition"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>getCurrentPosition ()](#apidoc.element.pdfmake.documentContext.prototype.getCurrentPosition)
- description and source-code
```javascript
getCurrentPosition = function () {
	var pageSize = this.getCurrentPage().pageSize;
	var innerHeight = pageSize.height - this.pageMargins.top - this.pageMargins.bottom;
	var innerWidth = pageSize.width - this.pageMargins.left - this.pageMargins.right;

	return {
		pageNumber: this.page + 1,
		pageOrientation: pageSize.orientation,
		pageInnerHeight: innerHeight,
		pageInnerWidth: innerWidth,
		left: this.x,
		top: this.y,
		verticalRatio: ((this.y - this.pageMargins.top) / innerHeight),
		horizontalRatio: ((this.x - this.pageMargins.left) / innerWidth)
	};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.initializePage"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>initializePage ()](#apidoc.element.pdfmake.documentContext.prototype.initializePage)
- description and source-code
```javascript
initializePage = function () {
	this.y = this.pageMargins.top;
	this.availableHeight = this.getCurrentPage().pageSize.height - this.pageMargins.top - this.pageMargins.bottom;
	this.pageSnapshot().availableWidth = this.getCurrentPage().pageSize.width - this.pageMargins.left - this.pageMargins.right;
}
```
- example usage
```shell
...
		this.addPage(pageSize);

		if (currentPageOrientation === pageSize.orientation) {
			this.availableWidth = currentAvailableWidth;
		}
	} else {
		this.page = nextPageIndex;
		this.initializePage();
	}

	return {
		newPageCreated: createNewPage,
		prevPage: prevPage,
		prevY: prevY,
		y: this.y
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.markEnding"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>markEnding (endingCell)](#apidoc.element.pdfmake.documentContext.prototype.markEnding)
- description and source-code
```javascript
markEnding = function (endingCell) {
	this.page = endingCell._columnEndingContext.page;
	this.x = endingCell._columnEndingContext.x;
	this.y = endingCell._columnEndingContext.y;
	this.availableWidth = endingCell._columnEndingContext.availableWidth;
	this.availableHeight = endingCell._columnEndingContext.availableHeight;
	this.lastColumnWidth = endingCell._columnEndingContext.lastColumnWidth;
}
```
- example usage
```shell
...

			self.writer.context().beginColumn(width, leftOffset, getEndingCell(column, i));
			if (!column._span) {
				self.processNode(column);
				addAll(positions, column.positions);
			} else if (column._columnEndingContext) {
				// row-span ending
				self.writer.context().markEnding(column);
			}
		}

		self.writer.context().completeColumnGroup();
	});

	return {pageBreaks: pageBreaks, positions: positions};
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.moveDown"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>moveDown (offset)](#apidoc.element.pdfmake.documentContext.prototype.moveDown)
- description and source-code
```javascript
moveDown = function (offset) {
	this.y += offset;
	this.availableHeight -= offset;

	return this.availableHeight > 0;
}
```
- example usage
```shell
...
	addPageItem(page, {
		type: 'line',
		item: line
	}, index);
	this.tracker.emit('lineAdded', line);

	if (!dontUpdateContextPosition) {
		context.moveDown(height);
	}

	return position;
};

ElementWriter.prototype.alignLine = function (line) {
	var width = this.context.availableWidth;
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.moveTo"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>moveTo (x, y)](#apidoc.element.pdfmake.documentContext.prototype.moveTo)
- description and source-code
```javascript
moveTo = function (x, y) {
	if (x !== undefined && x !== null) {
		this.x = x;
		this.availableWidth = this.getCurrentPage().pageSize.width - this.x - this.pageMargins.right;
	}
	if (y !== undefined && y !== null) {
		this.y = y;
		this.availableHeight = this.getCurrentPage().pageSize.height - this.y - this.pageMargins.bottom;
	}
}
```
- example usage
```shell
...
	this.linearNodeList.push(node);
	decorateNode(node);

	applyMargins(function () {
		var absPosition = node.absolutePosition;
		if (absPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo(absPosition.x || 0, absPosition.y || 0);
		}

		var relPosition = node.relativePosition;
		if (relPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo((relPosition.x || 0) + self.writer.context().x, (relPosition.y || 0) + self.writer.context().y);
		}
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.moveToNextPage"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>moveToNextPage (pageOrientation)](#apidoc.element.pdfmake.documentContext.prototype.moveToNextPage)
- description and source-code
```javascript
moveToNextPage = function (pageOrientation) {
	var nextPageIndex = this.page + 1;

	var prevPage = this.page;
	var prevY = this.y;

	var createNewPage = nextPageIndex >= this.pages.length;
	if (createNewPage) {
		var currentAvailableWidth = this.availableWidth;
		var currentPageOrientation = this.getCurrentPage().pageSize.orientation;

		var pageSize = getPageSize(this.getCurrentPage(), pageOrientation);
		this.addPage(pageSize);

		if (currentPageOrientation === pageSize.orientation) {
			this.availableWidth = currentAvailableWidth;
		}
	} else {
		this.page = nextPageIndex;
		this.initializePage();
	}

	return {
		newPageCreated: createNewPage,
		prevPage: prevPage,
		prevY: prevY,
		y: this.y
	};
}
```
- example usage
```shell
...
		}
	});

	function applyMargins(callback) {
		var margin = node._margin;

		if (node.pageBreak === 'before') {
			self.writer.moveToNextPage(node.pageOrientation);
		}

		if (margin) {
			self.writer.context().moveDown(margin[1]);
			self.writer.context().addMargin(margin[0], margin[2]);
		}
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.pageSnapshot"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>pageSnapshot ()](#apidoc.element.pdfmake.documentContext.prototype.pageSnapshot)
- description and source-code
```javascript
pageSnapshot = function () {
	if (this.snapshots[0]) {
		return this.snapshots[0];
	} else {
		return this;
	}
}
```
- example usage
```shell
...

	return this.availableHeight > 0;
};

DocumentContext.prototype.initializePage = function () {
	this.y = this.pageMargins.top;
	this.availableHeight = this.getCurrentPage().pageSize.height - this.pageMargins.top - this.pageMargins.bottom;
	this.pageSnapshot().availableWidth = this.getCurrentPage().pageSize.width - this.pageMargins.left - this.pageMargins.right;
};

DocumentContext.prototype.pageSnapshot = function () {
	if (this.snapshots[0]) {
		return this.snapshots[0];
	} else {
		return this;
...
```

#### <a name="apidoc.element.pdfmake.documentContext.prototype.saveContextInEndingCell"></a>[function <span class="apidocSignatureSpan">pdfmake.documentContext.prototype.</span>saveContextInEndingCell (endingCell)](#apidoc.element.pdfmake.documentContext.prototype.saveContextInEndingCell)
- description and source-code
```javascript
saveContextInEndingCell = function (endingCell) {
	endingCell._columnEndingContext = {
		page: this.page,
		x: this.x,
		y: this.y,
		availableHeight: this.availableHeight,
		availableWidth: this.availableWidth,
		lastColumnWidth: this.lastColumnWidth
	};
}
```
- example usage
```shell
...
	this.availableHeight = saved.availableHeight;

	this.lastColumnWidth = width;
};

DocumentContext.prototype.calculateBottomMost = function (destContext) {
	if (this.endingCell) {
		this.saveContextInEndingCell(this.endingCell);
		this.endingCell = null;
	} else {
		destContext.bottomMost = bottomMostContext(this, destContext.bottomMost);
	}
};

DocumentContext.prototype.markEnding = function (endingCell) {
...
```



# <a name="apidoc.module.pdfmake.elementWriter"></a>[module pdfmake.elementWriter](#apidoc.module.pdfmake.elementWriter)

#### <a name="apidoc.element.pdfmake.elementWriter.elementWriter"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>elementWriter (context, tracker)](#apidoc.element.pdfmake.elementWriter.elementWriter)
- description and source-code
```javascript
function ElementWriter(context, tracker) {
	this.context = context;
	this.contextStack = [];
	this.tracker = tracker;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.elementWriter.prototype"></a>[module pdfmake.elementWriter.prototype](#apidoc.module.pdfmake.elementWriter.prototype)

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.addFragment"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addFragment (block, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)](#apidoc.element.pdfmake.elementWriter.prototype.addFragment)
- description and source-code
```javascript
addFragment = function (block, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition) {
	var ctx = this.context;
	var page = ctx.getCurrentPage();

	if (!useBlockXOffset && block.height > ctx.availableHeight) {
		return false;
	}

	block.items.forEach(function (item) {
		switch (item.type) {
			case 'line':
				var l = cloneLine(item.item);

				l.x = (l.x || 0) + (useBlockXOffset ? (block.xOffset || 0) : ctx.x);
				l.y = (l.y || 0) + (useBlockYOffset ? (block.yOffset || 0) : ctx.y);

				page.items.push({
					type: 'line',
					item: l
				});
				break;

			case 'vector':
				var v = pack(item.item);

				offsetVector(v, useBlockXOffset ? (block.xOffset || 0) : ctx.x, useBlockYOffset ? (block.yOffset || 0) : ctx.y);
				page.items.push({
					type: 'vector',
					item: v
				});
				break;

			case 'image':
				var img = pack(item.item);

				img.x = (img.x || 0) + (useBlockXOffset ? (block.xOffset || 0) : ctx.x);
				img.y = (img.y || 0) + (useBlockYOffset ? (block.yOffset || 0) : ctx.y);

				page.items.push({
					type: 'image',
					item: img
				});
				break;
		}
	});

	if (!dontUpdateContextPosition) {
		ctx.moveDown(block.height);
	}

	return true;
}
```
- example usage
```shell
...
};

PageElementWriter.prototype.addVector = function (vector, ignoreContextX, ignoreContextY, index) {
	return this.writer.addVector(vector, ignoreContextX, ignoreContextY, index);
};

PageElementWriter.prototype.addFragment = function (fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition) {
	if (!this.writer.addFragment(fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)) {
		this.moveToNextPage();
		this.writer.addFragment(fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition);
	}
};

PageElementWriter.prototype.moveToNextPage = function (pageOrientation) {
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.addImage"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addImage (image, index)](#apidoc.element.pdfmake.elementWriter.prototype.addImage)
- description and source-code
```javascript
addImage = function (image, index) {
	var context = this.context;
	var page = context.getCurrentPage(),
		position = this.getCurrentPositionOnPage();

	if (context.availableHeight < image._height || !page) {
		return false;
	}

	if (image._x === undefined) {
		image._x = image.x || 0;
	}

	image.x = context.x + image._x;
	image.y = context.y;

	this.alignImage(image);

	addPageItem(page, {
		type: 'image',
		item: image
	}, index);

	context.moveDown(image._height);

	return position;
}
```
- example usage
```shell
...
	line.lastLineInParagraph = textNode._inlines.length === 0;

	return line;
};

// images
LayoutBuilder.prototype.processImage = function (node) {
	var position = this.writer.addImage(node);
	node.positions.push(position);
};

LayoutBuilder.prototype.processCanvas = function (node) {
	var height = node._minHeight;

	if (this.writer.context().availableHeight < height) {
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.addLine"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addLine (line, dontUpdateContextPosition, index)](#apidoc.element.pdfmake.elementWriter.prototype.addLine)
- description and source-code
```javascript
addLine = function (line, dontUpdateContextPosition, index) {
	var height = line.getHeight();
	var context = this.context;
	var page = context.getCurrentPage(),
		position = this.getCurrentPositionOnPage();

	if (context.availableHeight < height || !page) {
		return false;
	}

	line.x = context.x + (line.x || 0);
	line.y = context.y + (line.y || 0);

	this.alignLine(line);

	addPageItem(page, {
		type: 'line',
		item: line
	}, index);
	this.tracker.emit('lineAdded', line);

	if (!dontUpdateContextPosition) {
		context.moveDown(height);
	}

	return position;
}
```
- example usage
```shell
...
				offsetVector(vector, -marker._minWidth, 0);
				self.writer.addVector(vector);
			} else if (marker._inlines) {
				var markerLine = new Line(self.pageSize.width);
				markerLine.addInline(marker._inlines[0]);
				markerLine.x = -marker._minWidth;
				markerLine.y = line.getAscenderHeight() - markerLine.getAscenderHeight();
				self.writer.addLine(markerLine, true);
			}
		}
	}
};

// tables
LayoutBuilder.prototype.processTable = function (tableNode) {
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.addQr"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addQr (qr, index)](#apidoc.element.pdfmake.elementWriter.prototype.addQr)
- description and source-code
```javascript
addQr = function (qr, index) {
	var context = this.context;
	var page = context.getCurrentPage(),
		position = this.getCurrentPositionOnPage();

	if (context.availableHeight < qr._height || !page) {
		return false;
	}

	if (qr._x === undefined) {
		qr._x = qr.x || 0;
	}

	qr.x = context.x + qr._x;
	qr.y = context.y;

	this.alignImage(qr);

	for (var i = 0, l = qr._canvas.length; i < l; i++) {
		var vector = qr._canvas[i];
		vector.x += qr.x;
		vector.y += qr.y;
		this.addVector(vector, true, true, index);
	}

	context.moveDown(qr._height);

	return position;
}
```
- example usage
```shell
...
	return fitOnPage(this, function (self) {
		return self.writer.addImage(image, index);
	});
};

PageElementWriter.prototype.addQr = function (qr, index) {
	return fitOnPage(this, function (self) {
		return self.writer.addQr(qr, index);
	});
};

PageElementWriter.prototype.addVector = function (vector, ignoreContextX, ignoreContextY, index) {
	return this.writer.addVector(vector, ignoreContextX, ignoreContextY, index);
};
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.addVector"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>addVector (vector, ignoreContextX, ignoreContextY, index)](#apidoc.element.pdfmake.elementWriter.prototype.addVector)
- description and source-code
```javascript
addVector = function (vector, ignoreContextX, ignoreContextY, index) {
	var context = this.context;
	var page = context.getCurrentPage(),
		position = this.getCurrentPositionOnPage();

	if (page) {
		offsetVector(vector, ignoreContextX ? 0 : context.x, ignoreContextY ? 0 : context.y);
		addPageItem(page, {
			type: 'vector',
			item: vector
		}, index);
		return position;
	}
}
```
- example usage
```shell
...

	this.alignImage(qr);

	for (var i = 0, l = qr._canvas.length; i < l; i++) {
		var vector = qr._canvas[i];
		vector.x += qr.x;
		vector.y += qr.y;
		this.addVector(vector, true, true, index);
	}

	context.moveDown(qr._height);

	return position;
};
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.alignImage"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>alignImage (image)](#apidoc.element.pdfmake.elementWriter.prototype.alignImage)
- description and source-code
```javascript
alignImage = function (image) {
	var width = this.context.availableWidth;
	var imageWidth = image._minWidth;
	var offset = 0;
	switch (image._alignment) {
		case 'right':
			offset = width - imageWidth;
			break;
		case 'center':
			offset = (width - imageWidth) / 2;
			break;
	}

	if (offset) {
		image.x = (image.x || 0) + offset;
	}
}
```
- example usage
```shell
...
	if (image._x === undefined) {
		image._x = image.x || 0;
	}

	image.x = context.x + image._x;
	image.y = context.y;

	this.alignImage(image);

	addPageItem(page, {
		type: 'image',
		item: image
	}, index);

	context.moveDown(image._height);
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.alignLine"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>alignLine (line)](#apidoc.element.pdfmake.elementWriter.prototype.alignLine)
- description and source-code
```javascript
alignLine = function (line) {
	var width = this.context.availableWidth;
	var lineWidth = line.getWidth();

	var alignment = line.inlines && line.inlines.length > 0 && line.inlines[0].alignment;

	var offset = 0;
	switch (alignment) {
		case 'right':
			offset = width - lineWidth;
			break;
		case 'center':
			offset = (width - lineWidth) / 2;
			break;
	}

	if (offset) {
		line.x = (line.x || 0) + offset;
	}

	if (alignment === 'justify' &&
		!line.newLineForced &&
		!line.lastLineInParagraph &&
		line.inlines.length > 1) {
		var additionalSpacing = (width - lineWidth) / (line.inlines.length - 1);

		for (var i = 1, l = line.inlines.length; i < l; i++) {
			offset = i * additionalSpacing;

			line.inlines[i].x += offset;
		}
	}
}
```
- example usage
```shell
...
	if (context.availableHeight < height || !page) {
		return false;
	}

	line.x = context.x + (line.x || 0);
	line.y = context.y + (line.y || 0);

	this.alignLine(line);

	addPageItem(page, {
		type: 'line',
		item: line
	}, index);
	this.tracker.emit('lineAdded', line);
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.getCurrentPositionOnPage"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>getCurrentPositionOnPage ()](#apidoc.element.pdfmake.elementWriter.prototype.getCurrentPositionOnPage)
- description and source-code
```javascript
getCurrentPositionOnPage = function () {
	return (this.contextStack[0] || this.context).getCurrentPosition();
}
```
- example usage
```shell
...
	}
}

ElementWriter.prototype.addLine = function (line, dontUpdateContextPosition, index) {
	var height = line.getHeight();
	var context = this.context;
	var page = context.getCurrentPage(),
		position = this.getCurrentPositionOnPage();

	if (context.availableHeight < height || !page) {
		return false;
	}

	line.x = context.x + (line.x || 0);
	line.y = context.y + (line.y || 0);
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.popContext"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>popContext ()](#apidoc.element.pdfmake.elementWriter.prototype.popContext)
- description and source-code
```javascript
popContext = function () {
	this.context = this.contextStack.pop();
}
```
- example usage
```shell
...
		this.writer.pushContext(width, height);
	}
};

PageElementWriter.prototype.commitUnbreakableBlock = function (forcedX, forcedY) {
	if (--this.transactionLevel === 0) {
		var unbreakableContext = this.writer.context;
		this.writer.popContext();

		var nbPages = unbreakableContext.pages.length;
		if (nbPages > 0) {
			// no support for multi-page unbreakableBlocks
			var fragment = unbreakableContext.pages[0];
			fragment.xOffset = forcedX;
			fragment.yOffset = forcedY;
...
```

#### <a name="apidoc.element.pdfmake.elementWriter.prototype.pushContext"></a>[function <span class="apidocSignatureSpan">pdfmake.elementWriter.prototype.</span>pushContext (contextOrWidth, height)](#apidoc.element.pdfmake.elementWriter.prototype.pushContext)
- description and source-code
```javascript
pushContext = function (contextOrWidth, height) {
	if (contextOrWidth === undefined) {
		height = this.context.getCurrentPage().height - this.context.pageMargins.top - this.context.pageMargins.bottom;
		contextOrWidth = this.context.availableWidth;
	}

	if (typeof contextOrWidth === 'number' || contextOrWidth instanceof Number) {
		contextOrWidth = new DocumentContext({width: contextOrWidth, height: height}, {left: 0, right: 0, top: 0, bottom: 0});
	}

	this.contextStack.push(this.context);
	this.context = contextOrWidth;
}
```
- example usage
```shell
...
		y: nextPage.y
	});
};

PageElementWriter.prototype.beginUnbreakableBlock = function (width, height) {
	if (this.transactionLevel++ === 0) {
		this.originalX = this.writer.context.x;
		this.writer.pushContext(width, height);
	}
};

PageElementWriter.prototype.commitUnbreakableBlock = function (forcedX, forcedY) {
	if (--this.transactionLevel === 0) {
		var unbreakableContext = this.writer.context;
		this.writer.popContext();
...
```



# <a name="apidoc.module.pdfmake.fontProvider"></a>[module pdfmake.fontProvider](#apidoc.module.pdfmake.fontProvider)

#### <a name="apidoc.element.pdfmake.fontProvider.fontProvider"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>fontProvider (fontDescriptors, pdfKitDoc)](#apidoc.element.pdfmake.fontProvider.fontProvider)
- description and source-code
```javascript
function FontProvider(fontDescriptors, pdfKitDoc) {
	this.fonts = {};
	this.pdfKitDoc = pdfKitDoc;
	this.fontCache = {};

	for (var font in fontDescriptors) {
		if (fontDescriptors.hasOwnProperty(font)) {
			var fontDef = fontDescriptors[font];

			this.fonts[font] = {
				normal: fontDef.normal,
				bold: fontDef.bold,
				italics: fontDef.italics,
				bolditalics: fontDef.bolditalics
			};
		}
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.fontProvider.prototype"></a>[module pdfmake.fontProvider.prototype](#apidoc.module.pdfmake.fontProvider.prototype)

#### <a name="apidoc.element.pdfmake.fontProvider.prototype.provideFont"></a>[function <span class="apidocSignatureSpan">pdfmake.fontProvider.prototype.</span>provideFont (familyName, bold, italics)](#apidoc.element.pdfmake.fontProvider.prototype.provideFont)
- description and source-code
```javascript
provideFont = function (familyName, bold, italics) {
	var type = typeName(bold, italics);
	if (!this.fonts[familyName] || !this.fonts[familyName][type]) {
		throw new Error('Font \'' + familyName + '\' in style \'' + type + '\' is not defined in the font section of the document definition
.');
	}

	this.fontCache[familyName] = this.fontCache[familyName] || {};

	if (!this.fontCache[familyName][type]) {
		var def = this.fonts[familyName][type];
		if (!Array.isArray(def)) {
			def = [def];
		}
		this.fontCache[familyName][type] = this.pdfKitDoc.font.apply(this.pdfKitDoc, def)._font;
	}

	return this.fontCache[familyName][type];
}
```
- example usage
```shell
...
	watermark.color = watermark.color || 'black';
	watermark.opacity = watermark.opacity || 0.6;
	watermark.bold = watermark.bold || false;
	watermark.italics = watermark.italics || false;

	var watermarkObject = {
		text: watermark.text,
		font: fontProvider.provideFont(watermark.font, watermark.bold, watermark.italics),
		size: getSize(this.pageSize, watermark, fontProvider),
		color: watermark.color,
		opacity: watermark.opacity
	};

	var pages = this.writer.context().pages;
	for (var i = 0, l = pages.length; i < l; i++) {
...
```



# <a name="apidoc.module.pdfmake.helpers"></a>[module pdfmake.helpers](#apidoc.module.pdfmake.helpers)

#### <a name="apidoc.element.pdfmake.helpers.fontStringify"></a>[function <span class="apidocSignatureSpan">pdfmake.helpers.</span>fontStringify (key, val)](#apidoc.element.pdfmake.helpers.fontStringify)
- description and source-code
```javascript
function fontStringify(key, val) {
	if (key === 'font') {
		return 'font';
	}
	return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.helpers.isFunction"></a>[function <span class="apidocSignatureSpan">pdfmake.helpers.</span>isFunction (functionToCheck)](#apidoc.element.pdfmake.helpers.isFunction)
- description and source-code
```javascript
function isFunction(functionToCheck) {
	var getType = {};
	return functionToCheck && getType.toString.call(functionToCheck) === '[object Function]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.helpers.offsetVector"></a>[function <span class="apidocSignatureSpan">pdfmake.helpers.</span>offsetVector (vector, x, y)](#apidoc.element.pdfmake.helpers.offsetVector)
- description and source-code
```javascript
function offsetVector(vector, x, y) {
	switch (vector.type) {
		case 'ellipse':
		case 'rect':
			vector.x += x;
			vector.y += y;
			break;
		case 'line':
			vector.x1 += x;
			vector.x2 += x;
			vector.y1 += y;
			vector.y2 += y;
			break;
		case 'polyline':
			for (var i = 0, l = vector.points.length; i < l; i++) {
				vector.points[i].x += x;
				vector.points[i].y += y;
			}
			break;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.helpers.pack"></a>[function <span class="apidocSignatureSpan">pdfmake.helpers.</span>pack ()](#apidoc.element.pdfmake.helpers.pack)
- description and source-code
```javascript
function pack() {
	var result = {};

	for (var i = 0, l = arguments.length; i < l; i++) {
		var obj = arguments[i];

		if (obj) {
			for (var key in obj) {
				if (obj.hasOwnProperty(key)) {
					result[key] = obj[key];
				}
			}
		}
	}

	return result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.imageMeasure"></a>[module pdfmake.imageMeasure](#apidoc.module.pdfmake.imageMeasure)

#### <a name="apidoc.element.pdfmake.imageMeasure.imageMeasure"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>imageMeasure (pdfKitDoc, imageDictionary)](#apidoc.element.pdfmake.imageMeasure.imageMeasure)
- description and source-code
```javascript
function ImageMeasure(pdfKitDoc, imageDictionary) {
	this.pdfKitDoc = pdfKitDoc;
	this.imageDictionary = imageDictionary || {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.imageMeasure.prototype"></a>[module pdfmake.imageMeasure.prototype](#apidoc.module.pdfmake.imageMeasure.prototype)

#### <a name="apidoc.element.pdfmake.imageMeasure.prototype.measureImage"></a>[function <span class="apidocSignatureSpan">pdfmake.imageMeasure.prototype.</span>measureImage (src)](#apidoc.element.pdfmake.imageMeasure.prototype.measureImage)
- description and source-code
```javascript
measureImage = function (src) {
	var image, label;
	var that = this;

	if (!this.pdfKitDoc._imageRegistry[src]) {
		label = 'I' + (++this.pdfKitDoc._imageCount);
		try {
			image = PDFImage.open(realImageSrc(src), label);
		} catch (error) {
			image = null;
		}
		if (image === null || image === undefined) {
			throw 'invalid image, images dictionary should contain dataURL entries (or local file paths in node.js)';
		}
		image.embed(this.pdfKitDoc);
		this.pdfKitDoc._imageRegistry[src] = image;
	} else {
		image = this.pdfKitDoc._imageRegistry[src];
	}

	return {width: image.width, height: image.height};

	function realImageSrc(src) {
		var img = that.imageDictionary[src];

		if (!img) {
			return src;
		}

		var index = img.indexOf('base64,');
		if (index < 0) {
			return that.imageDictionary[src];
		}

		return new Buffer(img.substring(index + 7), 'base64');
	}
}
```
- example usage
```shell
...
		} else if (node.ol) {
			return extendMargins(self.measureOrderedList(node));
		} else if (node.table) {
			return extendMargins(self.measureTable(node));
		} else if (node.text !== undefined) {
			return extendMargins(self.measureLeaf(node));
		} else if (node.image) {
			return extendMargins(self.measureImage(node));
		} else if (node.canvas) {
			return extendMargins(self.measureCanvas(node));
		} else if (node.qr) {
			return extendMargins(self.measureQr(node));
		} else {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}
...
```



# <a name="apidoc.module.pdfmake.layoutBuilder"></a>[module pdfmake.layoutBuilder](#apidoc.module.pdfmake.layoutBuilder)

#### <a name="apidoc.element.pdfmake.layoutBuilder.layoutBuilder"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>layoutBuilder (pageSize, pageMargins, imageMeasure)](#apidoc.element.pdfmake.layoutBuilder.layoutBuilder)
- description and source-code
```javascript
function LayoutBuilder(pageSize, pageMargins, imageMeasure) {
	this.pageSize = pageSize;
	this.pageMargins = pageMargins;
	this.tracker = new TraversalTracker();
	this.imageMeasure = imageMeasure;
	this.tableLayouts = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.layoutBuilder.prototype"></a>[module pdfmake.layoutBuilder.prototype](#apidoc.module.pdfmake.layoutBuilder.prototype)

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.addBackground"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addBackground (background)](#apidoc.element.pdfmake.layoutBuilder.prototype.addBackground)
- description and source-code
```javascript
addBackground = function (background) {
	var backgroundGetter = isFunction(background) ? background : function () {
		return background;
	};

	var pageBackground = backgroundGetter(this.writer.context().page + 1);

	if (pageBackground) {
		var pageSize = this.writer.context().getCurrentPage().pageSize;
		this.writer.beginUnbreakableBlock(pageSize.width, pageSize.height);
		this.processNode(this.docMeasure.measureDocument(pageBackground));
		this.writer.commitUnbreakableBlock(0, 0);
	}
}
```
- example usage
```shell
...
	docStructure = this.docMeasure.measureDocument(docStructure);

	this.writer = new PageElementWriter(
		new DocumentContext(this.pageSize, this.pageMargins), this.tracker);

	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
	if (watermark != null) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.addDynamicRepeatable"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addDynamicRepeatable (nodeGetter, sizeFunction)](#apidoc.element.pdfmake.layoutBuilder.prototype.addDynamicRepeatable)
- description and source-code
```javascript
addDynamicRepeatable = function (nodeGetter, sizeFunction) {
	var pages = this.writer.context().pages;

	for (var pageIndex = 0, l = pages.length; pageIndex < l; pageIndex++) {
		this.writer.context().page = pageIndex;

		var node = nodeGetter(pageIndex + 1, l, this.writer.context().pages[pageIndex].pageSize);

		if (node) {
			var sizes = sizeFunction(this.writer.context().getCurrentPage().pageSize, this.pageMargins);
			this.writer.beginUnbreakableBlock(sizes.width, sizes.height);
			this.processNode(this.docMeasure.measureDocument(node));
			this.writer.commitUnbreakableBlock(sizes.x, sizes.y);
		}
	}
}
```
- example usage
```shell
...
		this.writer.beginUnbreakableBlock(pageSize.width, pageSize.height);
		this.processNode(this.docMeasure.measureDocument(pageBackground));
		this.writer.commitUnbreakableBlock(0, 0);
	}
};

LayoutBuilder.prototype.addStaticRepeatable = function (headerOrFooter, sizeFunction) {
	this.addDynamicRepeatable(function () {
		return headerOrFooter;
	}, sizeFunction);
};

LayoutBuilder.prototype.addDynamicRepeatable = function (nodeGetter, sizeFunction) {
	var pages = this.writer.context().pages;
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.addHeadersAndFooters"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addHeadersAndFooters (header, footer)](#apidoc.element.pdfmake.layoutBuilder.prototype.addHeadersAndFooters)
- description and source-code
```javascript
addHeadersAndFooters = function (header, footer) {
	var headerSizeFct = function (pageSize, pageMargins) {
		return {
			x: 0,
			y: 0,
			width: pageSize.width,
			height: pageMargins.top
		};
	};

	var footerSizeFct = function (pageSize, pageMargins) {
		return {
			x: 0,
			y: pageSize.height - pageMargins.bottom,
			width: pageSize.width,
			height: pageMargins.bottom
		};
	};

	if (isFunction(header)) {
		this.addDynamicRepeatable(header, headerSizeFct);
	} else if (header) {
		this.addStaticRepeatable(header, headerSizeFct);
	}

	if (isFunction(footer)) {
		this.addDynamicRepeatable(footer, footerSizeFct);
	} else if (footer) {
		this.addStaticRepeatable(footer, footerSizeFct);
	}
}
```
- example usage
```shell
...
	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
	if (watermark != null) {
		this.addWatermark(watermark, fontProvider, defaultStyle);
	}

	return {pages: this.writer.context().pages, linearNodeList: this.linearNodeList};
};
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.addStaticRepeatable"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addStaticRepeatable (headerOrFooter, sizeFunction)](#apidoc.element.pdfmake.layoutBuilder.prototype.addStaticRepeatable)
- description and source-code
```javascript
addStaticRepeatable = function (headerOrFooter, sizeFunction) {
	this.addDynamicRepeatable(function () {
		return headerOrFooter;
	}, sizeFunction);
}
```
- example usage
```shell
...
			height: pageMargins.bottom
		};
	};

	if (isFunction(header)) {
		this.addDynamicRepeatable(header, headerSizeFct);
	} else if (header) {
		this.addStaticRepeatable(header, headerSizeFct);
	}

	if (isFunction(footer)) {
		this.addDynamicRepeatable(footer, footerSizeFct);
	} else if (footer) {
		this.addStaticRepeatable(footer, footerSizeFct);
	}
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.addWatermark"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>addWatermark (watermark, fontProvider, defaultStyle)](#apidoc.element.pdfmake.layoutBuilder.prototype.addWatermark)
- description and source-code
```javascript
addWatermark = function (watermark, fontProvider, defaultStyle) {
	if (typeof watermark === 'string') {
		watermark = {'text': watermark};
	}

	if (!watermark.text) { // empty watermark text
		return;
	}

	watermark.font = watermark.font || defaultStyle.font || 'Roboto';
	watermark.color = watermark.color || 'black';
	watermark.opacity = watermark.opacity || 0.6;
	watermark.bold = watermark.bold || false;
	watermark.italics = watermark.italics || false;

	var watermarkObject = {
		text: watermark.text,
		font: fontProvider.provideFont(watermark.font, watermark.bold, watermark.italics),
		size: getSize(this.pageSize, watermark, fontProvider),
		color: watermark.color,
		opacity: watermark.opacity
	};

	var pages = this.writer.context().pages;
	for (var i = 0, l = pages.length; i < l; i++) {
		pages[i].watermark = watermarkObject;
	}

	function getSize(pageSize, watermark, fontProvider) {
		var width = pageSize.width;
		var height = pageSize.height;
		var targetWidth = Math.sqrt(width * width + height * height) * 0.8; /* page diagonal * sample factor */
		var textTools = new TextTools(fontProvider);
		var styleContextStack = new StyleContextStack(null, {font: watermark.font, bold: watermark.bold, italics: watermark.italics});
		var size;

		/**
		 * Binary search the best font size.
		 * Initial bounds [0, 1000]
		 * Break when range < 1
		 */
		var a = 0;
		var b = 1000;
		var c = (a + b) / 2;
		while (Math.abs(a - b) > 1) {
			styleContextStack.push({
				fontSize: c
			});
			size = textTools.sizeOfString(watermark.text, styleContextStack);
			if (size.width > targetWidth) {
				b = c;
				c = (a + b) / 2;
			} else if (size.width < targetWidth) {
				a = c;
				c = (a + b) / 2;
			}
			styleContextStack.pop();
		}
		/*
		 End binary search
		 */
		return {size: size, fontSize: c};
	}
}
```
- example usage
```shell
...
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
	if (watermark != null) {
		this.addWatermark(watermark, fontProvider, defaultStyle);
	}

	return {pages: this.writer.context().pages, linearNodeList: this.linearNodeList};
};


LayoutBuilder.prototype.addBackground = function (background) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.buildNextLine"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>buildNextLine (textNode)](#apidoc.element.pdfmake.layoutBuilder.prototype.buildNextLine)
- description and source-code
```javascript
buildNextLine = function (textNode) {
	if (!textNode._inlines || textNode._inlines.length === 0) {
		return null;
	}

	var line = new Line(this.writer.context().availableWidth);

	while (textNode._inlines && textNode._inlines.length > 0 && line.hasEnoughSpaceForInline(textNode._inlines[0])) {
		line.addInline(textNode._inlines.shift());
	}

	line.lastLineInParagraph = textNode._inlines.length === 0;

	return line;
}
```
- example usage
```shell
...
	}

	processor.endTable(this.writer);
};

// leafs (texts)
LayoutBuilder.prototype.processLeaf = function (node) {
	var line = this.buildNextLine(node);
	var currentHeight = (line) ? line.getHeight() : 0;
	var maxHeight = node.maxHeight || -1;

	while (line && (maxHeight === -1 || currentHeight < maxHeight)) {
		var positions = this.writer.addLine(line);
		node.positions.push(positions);
		line = this.buildNextLine(node);
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.layoutDocument"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>layoutDocument (docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images, watermark, pageBreakBeforeFct )](#apidoc.element.pdfmake.layoutBuilder.prototype.layoutDocument)
- description and source-code
```javascript
layoutDocument = function (docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images, watermark, pageBreakBeforeFct ) {

	function addPageBreaksIfNecessary(linearNodeList, pages) {

		if (!isFunction(pageBreakBeforeFct)) {
			return false;
		}

		linearNodeList = _.reject(linearNodeList, function (node) {
			return _.isEmpty(node.positions);
		});

		_.each(linearNodeList, function (node) {
			var nodeInfo = _.pick(node, [
				'id', 'text', 'ul', 'ol', 'table', 'image', 'qr', 'canvas', 'columns',
				'headlineLevel', 'style', 'pageBreak', 'pageOrientation',
				'width', 'height'
			]);
			nodeInfo.startPosition = _.first(node.positions);
			nodeInfo.pageNumbers = _.chain(node.positions).map('pageNumber').uniq().value();
			nodeInfo.pages = pages.length;
			nodeInfo.stack = _.isArray(node.stack);

			node.nodeInfo = nodeInfo;
		});

		return _.some(linearNodeList, function (node, index, followingNodeList) {
			if (node.pageBreak !== 'before' && !node.pageBreakCalculated) {
				node.pageBreakCalculated = true;
				var pageNumber = _.first(node.nodeInfo.pageNumbers);

				var followingNodesOnPage = _.chain(followingNodeList).drop(index + 1).filter(function (node0) {
					return _.includes(node0.nodeInfo.pageNumbers, pageNumber);
				}).value();

				var nodesOnNextPage = _.chain(followingNodeList).drop(index + 1).filter(function (node0) {
					return _.includes(node0.nodeInfo.pageNumbers, pageNumber + 1);
				}).value();

				var previousNodesOnPage = _.chain(followingNodeList).take(index).filter(function (node0) {
					return _.includes(node0.nodeInfo.pageNumbers, pageNumber);
				}).value();

				if (pageBreakBeforeFct(node.nodeInfo,
					_.map(followingNodesOnPage, 'nodeInfo'),
					_.map(nodesOnNextPage, 'nodeInfo'),
					_.map(previousNodesOnPage, 'nodeInfo'))) {
					node.pageBreak = 'before';
					return true;
				}
			}
		});
	}

	this.docMeasure = new DocMeasure(fontProvider, styleDictionary, defaultStyle, this.imageMeasure, this.tableLayouts, images);


	function resetXYs(result) {
		_.each(result.linearNodeList, function (node) {
			node.resetXY();
		});
	}

	var result = this.tryLayoutDocument(docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images
, watermark);
	while (addPageBreaksIfNecessary(result.linearNodeList, result.pages)) {
		resetXYs(result);
		result = this.tryLayoutDocument(docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images,
watermark);
	}

	return result.pages;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processCanvas"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processCanvas (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processCanvas)
- description and source-code
```javascript
processCanvas = function (node) {
	var height = node._minHeight;

	if (this.writer.context().availableHeight < height) {
		// TODO: support for canvas larger than a page
		// TODO: support for other overflow methods

		this.writer.moveToNextPage();
	}

	node.canvas.forEach(function (vector) {
		var position = this.writer.addVector(vector);
		node.positions.push(position);
	}, this);

	this.writer.context().moveDown(height);
}
```
- example usage
```shell
...
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
			self.processImage(node);
		} else if (node.canvas) {
			self.processCanvas(node);
		} else if (node.qr) {
			self.processQr(node);
		} else if (!node._span) {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}

		if (absPosition || relPosition) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processColumns"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processColumns (columnNode)](#apidoc.element.pdfmake.layoutBuilder.prototype.processColumns)
- description and source-code
```javascript
processColumns = function (columnNode) {
	var columns = columnNode.columns;
	var availableWidth = this.writer.context().availableWidth;
	var gaps = gapArray(columnNode._gap);

	if (gaps) {
		availableWidth -= (gaps.length - 1) * columnNode._gap;
	}

	ColumnCalculator.buildColumnWidths(columns, availableWidth);
	var result = this.processRow(columns, columns, gaps);
	addAll(columnNode.positions, result.positions);


	function gapArray(gap) {
		if (!gap) {
			return null;
		}

		var gaps = [];
		gaps.push(0);

		for (var i = columns.length - 1; i > 0; i--) {
			gaps.push(gap);
		}

		return gaps;
	}
}
```
- example usage
```shell
...
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo((relPosition.x || 0) + self.writer.context().x, (relPosition.y || 0) + self.writer.context().y);
		}

		if (node.stack) {
			self.processVerticalContainer(node);
		} else if (node.columns) {
			self.processColumns(node);
		} else if (node.ul) {
			self.processList(false, node);
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processImage"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processImage (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processImage)
- description and source-code
```javascript
processImage = function (node) {
	var position = this.writer.addImage(node);
	node.positions.push(position);
}
```
- example usage
```shell
...
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
			self.processImage(node);
		} else if (node.canvas) {
			self.processCanvas(node);
		} else if (node.qr) {
			self.processQr(node);
		} else if (!node._span) {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processLeaf"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processLeaf (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processLeaf)
- description and source-code
```javascript
processLeaf = function (node) {
	var line = this.buildNextLine(node);
	var currentHeight = (line) ? line.getHeight() : 0;
	var maxHeight = node.maxHeight || -1;

	while (line && (maxHeight === -1 || currentHeight < maxHeight)) {
		var positions = this.writer.addLine(line);
		node.positions.push(positions);
		line = this.buildNextLine(node);
		if (line) {
			currentHeight += line.getHeight();
		}
	}
}
```
- example usage
```shell
...
		} else if (node.ul) {
			self.processList(false, node);
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
			self.processImage(node);
		} else if (node.canvas) {
			self.processCanvas(node);
		} else if (node.qr) {
			self.processQr(node);
		} else if (!node._span) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processList"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processList (orderedList, node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processList)
- description and source-code
```javascript
processList = function (orderedList, node) {
	var self = this,
		items = orderedList ? node.ol : node.ul,
		gapSize = node._gapSize;

	this.writer.context().addMargin(gapSize.width);

	var nextMarker;
	this.tracker.auto('lineAdded', addMarkerToFirstLeaf, function () {
		items.forEach(function (item) {
			nextMarker = item.listMarker;
			self.processNode(item);
			addAll(node.positions, item.positions);
		});
	});

	this.writer.context().addMargin(-gapSize.width);

	function addMarkerToFirstLeaf(line) {
		// I'm not very happy with the way list processing is implemented
		// (both code and algorithm should be rethinked)
		if (nextMarker) {
			var marker = nextMarker;
			nextMarker = null;

			if (marker.canvas) {
				var vector = marker.canvas[0];

				offsetVector(vector, -marker._minWidth, 0);
				self.writer.addVector(vector);
			} else if (marker._inlines) {
				var markerLine = new Line(self.pageSize.width);
				markerLine.addInline(marker._inlines[0]);
				markerLine.x = -marker._minWidth;
				markerLine.y = line.getAscenderHeight() - markerLine.getAscenderHeight();
				self.writer.addLine(markerLine, true);
			}
		}
	}
}
```
- example usage
```shell
...
		}

		if (node.stack) {
			self.processVerticalContainer(node);
		} else if (node.columns) {
			self.processColumns(node);
		} else if (node.ul) {
			self.processList(false, node);
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processNode"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processNode (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processNode)
- description and source-code
```javascript
processNode = function (node) {
	var self = this;

	this.linearNodeList.push(node);
	decorateNode(node);

	applyMargins(function () {
		var absPosition = node.absolutePosition;
		if (absPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo(absPosition.x || 0, absPosition.y || 0);
		}

		var relPosition = node.relativePosition;
		if (relPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo((relPosition.x || 0) + self.writer.context().x, (relPosition.y || 0) + self.writer.context().y);
		}

		if (node.stack) {
			self.processVerticalContainer(node);
		} else if (node.columns) {
			self.processColumns(node);
		} else if (node.ul) {
			self.processList(false, node);
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
			self.processImage(node);
		} else if (node.canvas) {
			self.processCanvas(node);
		} else if (node.qr) {
			self.processQr(node);
		} else if (!node._span) {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}

		if (absPosition || relPosition) {
			self.writer.context().endDetachedBlock();
		}
	});

	function applyMargins(callback) {
		var margin = node._margin;

		if (node.pageBreak === 'before') {
			self.writer.moveToNextPage(node.pageOrientation);
		}

		if (margin) {
			self.writer.context().moveDown(margin[1]);
			self.writer.context().addMargin(margin[0], margin[2]);
		}

		callback();

		if (margin) {
			self.writer.context().addMargin(-margin[0], -margin[2]);
			self.writer.context().moveDown(margin[3]);
		}

		if (node.pageBreak === 'after') {
			self.writer.moveToNextPage(node.pageOrientation);
		}
	}
}
```
- example usage
```shell
...

	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
	if (watermark != null) {
		this.addWatermark(watermark, fontProvider, defaultStyle);
	}

	return {pages: this.writer.context().pages, linearNodeList: this.linearNodeList};
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processQr"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processQr (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processQr)
- description and source-code
```javascript
processQr = function (node) {
	var position = this.writer.addQr(node);
	node.positions.push(position);
}
```
- example usage
```shell
...
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
			self.processImage(node);
		} else if (node.canvas) {
			self.processCanvas(node);
		} else if (node.qr) {
			self.processQr(node);
		} else if (!node._span) {
			throw 'Unrecognized document structure: ' + JSON.stringify(node, fontStringify);
		}

		if (absPosition || relPosition) {
			self.writer.context().endDetachedBlock();
		}
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processRow"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processRow (columns, widths, gaps, tableBody, tableRow)](#apidoc.element.pdfmake.layoutBuilder.prototype.processRow)
- description and source-code
```javascript
processRow = function (columns, widths, gaps, tableBody, tableRow) {
	var self = this;
	var pageBreaks = [], positions = [];

	this.tracker.auto('pageChanged', storePageBreakData, function () {
		widths = widths || columns;

		self.writer.context().beginColumnGroup();

		for (var i = 0, l = columns.length; i < l; i++) {
			var column = columns[i];
			var width = widths[i]._calcWidth;
			var leftOffset = colLeftOffset(i);

			if (column.colSpan && column.colSpan > 1) {
				for (var j = 1; j < column.colSpan; j++) {
					width += widths[++i]._calcWidth + gaps[i];
				}
			}

			self.writer.context().beginColumn(width, leftOffset, getEndingCell(column, i));
			if (!column._span) {
				self.processNode(column);
				addAll(positions, column.positions);
			} else if (column._columnEndingContext) {
				// row-span ending
				self.writer.context().markEnding(column);
			}
		}

		self.writer.context().completeColumnGroup();
	});

	return {pageBreaks: pageBreaks, positions: positions};

	function storePageBreakData(data) {
		var pageDesc;

		for (var i = 0, l = pageBreaks.length; i < l; i++) {
			var desc = pageBreaks[i];
			if (desc.prevPage === data.prevPage) {
				pageDesc = desc;
				break;
			}
		}

		if (!pageDesc) {
			pageDesc = data;
			pageBreaks.push(pageDesc);
		}
		pageDesc.prevY = Math.max(pageDesc.prevY, data.prevY);
		pageDesc.y = Math.min(pageDesc.y, data.y);
	}

	function colLeftOffset(i) {
		if (gaps && gaps.length > i) {
			return gaps[i];
		}
		return 0;
	}

	function getEndingCell(column, columnIndex) {
		if (column.rowSpan && column.rowSpan > 1) {
			var endingRow = tableRow + column.rowSpan - 1;
			if (endingRow >= tableBody.length) {
				throw 'Row span for column ' + columnIndex + ' (with indexes starting from 0) exceeded row count';
			}
			return tableBody[endingRow][columnIndex];
		}

		return null;
	}
}
```
- example usage
```shell
...
	var gaps = gapArray(columnNode._gap);

	if (gaps) {
		availableWidth -= (gaps.length - 1) * columnNode._gap;
	}

	ColumnCalculator.buildColumnWidths(columns, availableWidth);
	var result = this.processRow(columns, columns, gaps);
	addAll(columnNode.positions, result.positions);


	function gapArray(gap) {
		if (!gap) {
			return null;
		}
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processTable"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processTable (tableNode)](#apidoc.element.pdfmake.layoutBuilder.prototype.processTable)
- description and source-code
```javascript
processTable = function (tableNode) {
	var processor = new TableProcessor(tableNode);

	processor.beginTable(this.writer);

	for (var i = 0, l = tableNode.table.body.length; i < l; i++) {
		processor.beginRow(i, this.writer);

		var result = this.processRow(tableNode.table.body[i], tableNode.table.widths, tableNode._offsets.offsets, tableNode.table.body
, i);
		addAll(tableNode.positions, result.positions);

		processor.endRow(i, this.writer, result.pageBreaks);
	}

	processor.endTable(this.writer);
}
```
- example usage
```shell
...
		} else if (node.columns) {
			self.processColumns(node);
		} else if (node.ul) {
			self.processList(false, node);
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
			self.processTable(node);
		} else if (node.text !== undefined) {
			self.processLeaf(node);
		} else if (node.image) {
			self.processImage(node);
		} else if (node.canvas) {
			self.processCanvas(node);
		} else if (node.qr) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.processVerticalContainer"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>processVerticalContainer (node)](#apidoc.element.pdfmake.layoutBuilder.prototype.processVerticalContainer)
- description and source-code
```javascript
processVerticalContainer = function (node) {
	var self = this;
	node.stack.forEach(function (item) {
		self.processNode(item);
		addAll(node.positions, item.positions);

		//TODO: paragraph gap
	});
}
```
- example usage
```shell
...
		var relPosition = node.relativePosition;
		if (relPosition) {
			self.writer.context().beginDetachedBlock();
			self.writer.context().moveTo((relPosition.x || 0) + self.writer.context().x, (relPosition.y || 0) + self.writer.context().y);
		}

		if (node.stack) {
			self.processVerticalContainer(node);
		} else if (node.columns) {
			self.processColumns(node);
		} else if (node.ul) {
			self.processList(false, node);
		} else if (node.ol) {
			self.processList(true, node);
		} else if (node.table) {
...
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.registerTableLayouts"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>registerTableLayouts (tableLayouts)](#apidoc.element.pdfmake.layoutBuilder.prototype.registerTableLayouts)
- description and source-code
```javascript
registerTableLayouts = function (tableLayouts) {
	this.tableLayouts = pack(this.tableLayouts, tableLayouts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.layoutBuilder.prototype.tryLayoutDocument"></a>[function <span class="apidocSignatureSpan">pdfmake.layoutBuilder.prototype.</span>tryLayoutDocument (docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images, watermark, pageBreakBeforeFct )](#apidoc.element.pdfmake.layoutBuilder.prototype.tryLayoutDocument)
- description and source-code
```javascript
tryLayoutDocument = function (docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images, watermark, pageBreakBeforeFct ) {

	this.linearNodeList = [];
	docStructure = this.docMeasure.measureDocument(docStructure);

	this.writer = new PageElementWriter(
		new DocumentContext(this.pageSize, this.pageMargins), this.tracker);

	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
	if (watermark != null) {
		this.addWatermark(watermark, fontProvider, defaultStyle);
	}

	return {pages: this.writer.context().pages, linearNodeList: this.linearNodeList};
}
```
- example usage
```shell
...

	function resetXYs(result) {
		_.each(result.linearNodeList, function (node) {
			node.resetXY();
		});
	}

	var result = this.tryLayoutDocument(docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images
, watermark);
	while (addPageBreaksIfNecessary(result.linearNodeList, result.pages)) {
		resetXYs(result);
		result = this.tryLayoutDocument(docStructure, fontProvider, styleDictionary, defaultStyle, background, header, footer, images,
watermark);
	}

	return result.pages;
};
...
```



# <a name="apidoc.module.pdfmake.line"></a>[module pdfmake.line](#apidoc.module.pdfmake.line)

#### <a name="apidoc.element.pdfmake.line.line"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>line (maxWidth)](#apidoc.element.pdfmake.line.line)
- description and source-code
```javascript
function Line(maxWidth) {
	this.maxWidth = maxWidth;
	this.leadingCut = 0;
	this.trailingCut = 0;
	this.inlineWidths = 0;
	this.inlines = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.line.prototype"></a>[module pdfmake.line.prototype](#apidoc.module.pdfmake.line.prototype)

#### <a name="apidoc.element.pdfmake.line.prototype.addInline"></a>[function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>addInline (inline)](#apidoc.element.pdfmake.line.prototype.addInline)
- description and source-code
```javascript
addInline = function (inline) {
	if (this.inlines.length === 0) {
		this.leadingCut = inline.leadingCut || 0;
	}
	this.trailingCut = inline.trailingCut || 0;

	inline.x = this.inlineWidths - this.leadingCut;

	this.inlines.push(inline);
	this.inlineWidths += inline.width;

	if (inline.lineEnd) {
		this.newLineForced = true;
	}
}
```
- example usage
```shell
...
			if (marker.canvas) {
				var vector = marker.canvas[0];

				offsetVector(vector, -marker._minWidth, 0);
				self.writer.addVector(vector);
			} else if (marker._inlines) {
				var markerLine = new Line(self.pageSize.width);
				markerLine.addInline(marker._inlines[0]);
				markerLine.x = -marker._minWidth;
				markerLine.y = line.getAscenderHeight() - markerLine.getAscenderHeight();
				self.writer.addLine(markerLine, true);
			}
		}
	}
};
...
```

#### <a name="apidoc.element.pdfmake.line.prototype.getAscenderHeight"></a>[function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>getAscenderHeight ()](#apidoc.element.pdfmake.line.prototype.getAscenderHeight)
- description and source-code
```javascript
getAscenderHeight = function () {
	var y = 0;

	this.inlines.forEach(function (inline) {
		y = Math.max(y, inline.font.ascender / 1000 * inline.fontSize);
	});
	return y;
}
```
- example usage
```shell
...

				offsetVector(vector, -marker._minWidth, 0);
				self.writer.addVector(vector);
			} else if (marker._inlines) {
				var markerLine = new Line(self.pageSize.width);
				markerLine.addInline(marker._inlines[0]);
				markerLine.x = -marker._minWidth;
				markerLine.y = line.getAscenderHeight() - markerLine.getAscenderHeight();
				self.writer.addLine(markerLine, true);
			}
		}
	}
};

// tables
...
```

#### <a name="apidoc.element.pdfmake.line.prototype.getHeight"></a>[function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>getHeight ()](#apidoc.element.pdfmake.line.prototype.getHeight)
- description and source-code
```javascript
getHeight = function () {
	var max = 0;

	this.inlines.forEach(function (item) {
		max = Math.max(max, item.height || 0);
	});

	return max;
}
```
- example usage
```shell
...
		page.items.push(item);
	} else {
		page.items.splice(index, 0, item);
	}
}

ElementWriter.prototype.addLine = function (line, dontUpdateContextPosition, index) {
	var height = line.getHeight();
	var context = this.context;
	var page = context.getCurrentPage(),
		position = this.getCurrentPositionOnPage();

	if (context.availableHeight < height || !page) {
		return false;
	}
...
```

#### <a name="apidoc.element.pdfmake.line.prototype.getWidth"></a>[function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>getWidth ()](#apidoc.element.pdfmake.line.prototype.getWidth)
- description and source-code
```javascript
getWidth = function () {
	return this.inlineWidths - this.leadingCut - this.trailingCut;
}
```
- example usage
```shell
...
	}

	return position;
};

ElementWriter.prototype.alignLine = function (line) {
	var width = this.context.availableWidth;
	var lineWidth = line.getWidth();

	var alignment = line.inlines && line.inlines.length > 0 && line.inlines[0].alignment;

	var offset = 0;
	switch (alignment) {
		case 'right':
			offset = width - lineWidth;
...
```

#### <a name="apidoc.element.pdfmake.line.prototype.hasEnoughSpaceForInline"></a>[function <span class="apidocSignatureSpan">pdfmake.line.prototype.</span>hasEnoughSpaceForInline (inline)](#apidoc.element.pdfmake.line.prototype.hasEnoughSpaceForInline)
- description and source-code
```javascript
hasEnoughSpaceForInline = function (inline) {
	if (this.inlines.length === 0) {
		return true;
	}
	if (this.newLineForced) {
		return false;
	}

	return this.inlineWidths + inline.width - this.leadingCut - (inline.trailingCut || 0) <= this.maxWidth;
}
```
- example usage
```shell
...
LayoutBuilder.prototype.buildNextLine = function (textNode) {
	if (!textNode._inlines || textNode._inlines.length === 0) {
		return null;
	}

	var line = new Line(this.writer.context().availableWidth);

	while (textNode._inlines && textNode._inlines.length > 0 && line.hasEnoughSpaceForInline(textNode._inlines[0])) {
		line.addInline(textNode._inlines.shift());
	}

	line.lastLineInParagraph = textNode._inlines.length === 0;

	return line;
};
...
```



# <a name="apidoc.module.pdfmake.pageElementWriter"></a>[module pdfmake.pageElementWriter](#apidoc.module.pdfmake.pageElementWriter)

#### <a name="apidoc.element.pdfmake.pageElementWriter.pageElementWriter"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>pageElementWriter (context, tracker)](#apidoc.element.pdfmake.pageElementWriter.pageElementWriter)
- description and source-code
```javascript
function PageElementWriter(context, tracker) {
	this.transactionLevel = 0;
	this.repeatables = [];
	this.tracker = tracker;
	this.writer = new ElementWriter(context, tracker);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.pageElementWriter.prototype"></a>[module pdfmake.pageElementWriter.prototype](#apidoc.module.pdfmake.pageElementWriter.prototype)

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.addFragment"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addFragment (fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)](#apidoc.element.pdfmake.pageElementWriter.prototype.addFragment)
- description and source-code
```javascript
addFragment = function (fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition) {
	if (!this.writer.addFragment(fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)) {
		this.moveToNextPage();
		this.writer.addFragment(fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition);
	}
}
```
- example usage
```shell
...
};

PageElementWriter.prototype.addVector = function (vector, ignoreContextX, ignoreContextY, index) {
	return this.writer.addVector(vector, ignoreContextX, ignoreContextY, index);
};

PageElementWriter.prototype.addFragment = function (fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition) {
	if (!this.writer.addFragment(fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition)) {
		this.moveToNextPage();
		this.writer.addFragment(fragment, useBlockXOffset, useBlockYOffset, dontUpdateContextPosition);
	}
};

PageElementWriter.prototype.moveToNextPage = function (pageOrientation) {
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.addImage"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addImage (image, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addImage)
- description and source-code
```javascript
addImage = function (image, index) {
	return fitOnPage(this, function (self) {
		return self.writer.addImage(image, index);
	});
}
```
- example usage
```shell
...
	line.lastLineInParagraph = textNode._inlines.length === 0;

	return line;
};

// images
LayoutBuilder.prototype.processImage = function (node) {
	var position = this.writer.addImage(node);
	node.positions.push(position);
};

LayoutBuilder.prototype.processCanvas = function (node) {
	var height = node._minHeight;

	if (this.writer.context().availableHeight < height) {
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.addLine"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addLine (line, dontUpdateContextPosition, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addLine)
- description and source-code
```javascript
addLine = function (line, dontUpdateContextPosition, index) {
	return fitOnPage(this, function (self) {
		return self.writer.addLine(line, dontUpdateContextPosition, index);
	});
}
```
- example usage
```shell
...
				offsetVector(vector, -marker._minWidth, 0);
				self.writer.addVector(vector);
			} else if (marker._inlines) {
				var markerLine = new Line(self.pageSize.width);
				markerLine.addInline(marker._inlines[0]);
				markerLine.x = -marker._minWidth;
				markerLine.y = line.getAscenderHeight() - markerLine.getAscenderHeight();
				self.writer.addLine(markerLine, true);
			}
		}
	}
};

// tables
LayoutBuilder.prototype.processTable = function (tableNode) {
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.addQr"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addQr (qr, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addQr)
- description and source-code
```javascript
addQr = function (qr, index) {
	return fitOnPage(this, function (self) {
		return self.writer.addQr(qr, index);
	});
}
```
- example usage
```shell
...
	return fitOnPage(this, function (self) {
		return self.writer.addImage(image, index);
	});
};

PageElementWriter.prototype.addQr = function (qr, index) {
	return fitOnPage(this, function (self) {
		return self.writer.addQr(qr, index);
	});
};

PageElementWriter.prototype.addVector = function (vector, ignoreContextX, ignoreContextY, index) {
	return this.writer.addVector(vector, ignoreContextX, ignoreContextY, index);
};
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.addVector"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>addVector (vector, ignoreContextX, ignoreContextY, index)](#apidoc.element.pdfmake.pageElementWriter.prototype.addVector)
- description and source-code
```javascript
addVector = function (vector, ignoreContextX, ignoreContextY, index) {
	return this.writer.addVector(vector, ignoreContextX, ignoreContextY, index);
}
```
- example usage
```shell
...

	this.alignImage(qr);

	for (var i = 0, l = qr._canvas.length; i < l; i++) {
		var vector = qr._canvas[i];
		vector.x += qr.x;
		vector.y += qr.y;
		this.addVector(vector, true, true, index);
	}

	context.moveDown(qr._height);

	return position;
};
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.beginUnbreakableBlock"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>beginUnbreakableBlock (width, height)](#apidoc.element.pdfmake.pageElementWriter.prototype.beginUnbreakableBlock)
- description and source-code
```javascript
beginUnbreakableBlock = function (width, height) {
	if (this.transactionLevel++ === 0) {
		this.originalX = this.writer.context.x;
		this.writer.pushContext(width, height);
	}
}
```
- example usage
```shell
...
		return background;
	};

	var pageBackground = backgroundGetter(this.writer.context().page + 1);

	if (pageBackground) {
		var pageSize = this.writer.context().getCurrentPage().pageSize;
		this.writer.beginUnbreakableBlock(pageSize.width, pageSize.height);
		this.processNode(this.docMeasure.measureDocument(pageBackground));
		this.writer.commitUnbreakableBlock(0, 0);
	}
};

LayoutBuilder.prototype.addStaticRepeatable = function (headerOrFooter, sizeFunction) {
	this.addDynamicRepeatable(function () {
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.commitUnbreakableBlock"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>commitUnbreakableBlock (forcedX, forcedY)](#apidoc.element.pdfmake.pageElementWriter.prototype.commitUnbreakableBlock)
- description and source-code
```javascript
commitUnbreakableBlock = function (forcedX, forcedY) {
	if (--this.transactionLevel === 0) {
		var unbreakableContext = this.writer.context;
		this.writer.popContext();

		var nbPages = unbreakableContext.pages.length;
		if (nbPages > 0) {
			// no support for multi-page unbreakableBlocks
			var fragment = unbreakableContext.pages[0];
			fragment.xOffset = forcedX;
			fragment.yOffset = forcedY;

			//TODO: vectors can influence height in some situations
			if (nbPages > 1) {
				// on out-of-context blocs (headers, footers, background) height should be the whole DocumentContext height
				if (forcedX !== undefined || forcedY !== undefined) {
					fragment.height = unbreakableContext.getCurrentPage().pageSize.height - unbreakableContext.pageMargins.top - unbreakableContext
.pageMargins.bottom;
				} else {
					fragment.height = this.writer.context.getCurrentPage().pageSize.height - this.writer.context.pageMargins.top - this.writer.
context.pageMargins.bottom;
					for (var i = 0, l = this.repeatables.length; i < l; i++) {
						fragment.height -= this.repeatables[i].height;
					}
				}
			} else {
				fragment.height = unbreakableContext.y;
			}

			if (forcedX !== undefined || forcedY !== undefined) {
				this.writer.addFragment(fragment, true, true, true);
			} else {
				this.addFragment(fragment);
			}
		}
	}
}
```
- example usage
```shell
...

	var pageBackground = backgroundGetter(this.writer.context().page + 1);

	if (pageBackground) {
		var pageSize = this.writer.context().getCurrentPage().pageSize;
		this.writer.beginUnbreakableBlock(pageSize.width, pageSize.height);
		this.processNode(this.docMeasure.measureDocument(pageBackground));
		this.writer.commitUnbreakableBlock(0, 0);
	}
};

LayoutBuilder.prototype.addStaticRepeatable = function (headerOrFooter, sizeFunction) {
	this.addDynamicRepeatable(function () {
		return headerOrFooter;
	}, sizeFunction);
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.context"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>context ()](#apidoc.element.pdfmake.pageElementWriter.prototype.context)
- description and source-code
```javascript
context = function () {
	return this.writer.context;
}
```
- example usage
```shell
...
	this.linearNodeList = [];
	docStructure = this.docMeasure.measureDocument(docStructure);

	this.writer = new PageElementWriter(
		new DocumentContext(this.pageSize, this.pageMargins), this.tracker);

	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.currentBlockToRepeatable"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>currentBlockToRepeatable ()](#apidoc.element.pdfmake.pageElementWriter.prototype.currentBlockToRepeatable)
- description and source-code
```javascript
currentBlockToRepeatable = function () {
	var unbreakableContext = this.writer.context;
	var rep = {items: []};

	unbreakableContext.pages[0].items.forEach(function (item) {
		rep.items.push(item);
	});

	rep.xOffset = this.originalX;

	//TODO: vectors can influence height in some situations
	rep.height = unbreakableContext.y;

	return rep;
}
```
- example usage
```shell
...
			this.rowSpanData[i].rowSpan--;
		}
	}

	this.drawHorizontalLine(rowIndex + 1, writer);

	if (this.headerRows && rowIndex === this.headerRows - 1) {
		this.headerRepeatable = writer.currentBlockToRepeatable();
	}

	if (this.dontBreakRows) {
		writer.tracker.auto('pageChanged',
			function () {
				if (!self.headerRows && self.layout.hLineWhenBroken !== false) {
					self.drawHorizontalLine(rowIndex, writer);
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.moveToNextPage"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>moveToNextPage (pageOrientation)](#apidoc.element.pdfmake.pageElementWriter.prototype.moveToNextPage)
- description and source-code
```javascript
moveToNextPage = function (pageOrientation) {

	var nextPage = this.writer.context.moveToNextPage(pageOrientation);

	if (nextPage.newPageCreated) {
		this.repeatables.forEach(function (rep) {
			this.writer.addFragment(rep, true);
		}, this);
	} else {
		this.repeatables.forEach(function (rep) {
			this.writer.context.moveDown(rep.height);
		}, this);
	}

	this.writer.tracker.emit('pageChanged', {
		prevPage: nextPage.prevPage,
		prevY: nextPage.prevY,
		y: nextPage.y
	});
}
```
- example usage
```shell
...
		}
	});

	function applyMargins(callback) {
		var margin = node._margin;

		if (node.pageBreak === 'before') {
			self.writer.moveToNextPage(node.pageOrientation);
		}

		if (margin) {
			self.writer.context().moveDown(margin[1]);
			self.writer.context().addMargin(margin[0], margin[2]);
		}
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.popFromRepeatables"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>popFromRepeatables ()](#apidoc.element.pdfmake.pageElementWriter.prototype.popFromRepeatables)
- description and source-code
```javascript
popFromRepeatables = function () {
	this.repeatables.pop();
}
```
- example usage
```shell
...
		lineWidth: width,
		lineColor: typeof this.layout.vLineColor === 'function' ? this.layout.vLineColor(vLineIndex, this.tableNode) : this.layout.vLineColor
	}, false, true);
};

TableProcessor.prototype.endTable = function (writer) {
	if (this.cleanUpRepeatables) {
		writer.popFromRepeatables();
	}
};

TableProcessor.prototype.endRow = function (rowIndex, writer, pageBreaks) {
	var l, i;
	var self = this;
	writer.tracker.stopTracking('pageChanged', this.rowCallback);
...
```

#### <a name="apidoc.element.pdfmake.pageElementWriter.prototype.pushToRepeatables"></a>[function <span class="apidocSignatureSpan">pdfmake.pageElementWriter.prototype.</span>pushToRepeatables (rep)](#apidoc.element.pdfmake.pageElementWriter.prototype.pushToRepeatables)
- description and source-code
```javascript
pushToRepeatables = function (rep) {
	this.repeatables.push(rep);
}
```
- example usage
```shell
...
				writer.commitUnbreakableBlock();
			}
		);
	}

	if (this.headerRepeatable && (rowIndex === (this.rowsWithoutPageBreak - 1) || rowIndex === this.tableNode.table.body.length - 1
)) {
		writer.commitUnbreakableBlock();
		writer.pushToRepeatables(this.headerRepeatable);
		this.cleanUpRepeatables = true;
		this.headerRepeatable = null;
	}

	function getLineXs() {
		var result = [];
		var cols = 0;
...
```



# <a name="apidoc.module.pdfmake.qrEnc"></a>[module pdfmake.qrEnc](#apidoc.module.pdfmake.qrEnc)

#### <a name="apidoc.element.pdfmake.qrEnc.measure"></a>[function <span class="apidocSignatureSpan">pdfmake.qrEnc.</span>measure (node)](#apidoc.element.pdfmake.qrEnc.measure)
- description and source-code
```javascript
function measure(node) {
	var cd = buildCanvas(node.qr, node);
	node._canvas = cd.canvas;
	node._width = node._height = node._minWidth = node._maxWidth = node._minHeight = node._maxHeight = cd.size;
	return node;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.styleContextStack"></a>[module pdfmake.styleContextStack](#apidoc.module.pdfmake.styleContextStack)

#### <a name="apidoc.element.pdfmake.styleContextStack.styleContextStack"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>styleContextStack (styleDictionary, defaultStyle)](#apidoc.element.pdfmake.styleContextStack.styleContextStack)
- description and source-code
```javascript
function StyleContextStack(styleDictionary, defaultStyle) {
	this.defaultStyle = defaultStyle || {};
	this.styleDictionary = styleDictionary;
	this.styleOverrides = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.styleContextStack.prototype"></a>[module pdfmake.styleContextStack.prototype](#apidoc.module.pdfmake.styleContextStack.prototype)

#### <a name="apidoc.element.pdfmake.styleContextStack.prototype.auto"></a>[function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>auto (item, callback)](#apidoc.element.pdfmake.styleContextStack.prototype.auto)
- description and source-code
```javascript
auto = function (item, callback) {
	var pushedItems = this.autopush(item);
	var result = callback();

	if (pushedItems > 0) {
		this.pop(pushedItems);
	}

	return result;
}
```
- example usage
```shell
...
	if (Object.keys(node).length === 0) {
		// A warning could be logged: console.warn('pdfmake: Empty node, ignoring it');
		node = {text: ''};
	}

	var self = this;

	return this.styleStack.auto(node, function () {
		// TODO: refactor + rethink whether this is the proper way to handle margins
		node._margin = getNodeMargin(node);

		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
...
```

#### <a name="apidoc.element.pdfmake.styleContextStack.prototype.autopush"></a>[function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>autopush (item)](#apidoc.element.pdfmake.styleContextStack.prototype.autopush)
- description and source-code
```javascript
autopush = function (item) {
	if (typeof item === 'string' || item instanceof String) {
		return 0;
	}

	var styleNames = [];

	if (item.style) {
		if (Array.isArray(item.style)) {
			styleNames = item.style;
		} else {
			styleNames = [item.style];
		}
	}

	for (var i = 0, l = styleNames.length; i < l; i++) {
		this.push(styleNames[i]);
	}

	var styleOverrideObject = {};
	var pushSOO = false;

	[
		'font',
		'fontSize',
		'bold',
		'italics',
		'alignment',
		'color',
		'columnGap',
		'fillColor',
		'decoration',
		'decorationStyle',
		'decorationColor',
		'background',
		'lineHeight',
		'noWrap',
		'markerColor'
			//'tableCellPadding'
			// 'cellBorder',
			// 'headerCellBorder',
			// 'oddRowCellBorder',
			// 'evenRowCellBorder',
			// 'tableBorder'
	].forEach(function (key) {
		if (item[key] !== undefined && item[key] !== null) {
			styleOverrideObject[key] = item[key];
			pushSOO = true;
		}
	});

	if (pushSOO) {
		this.push(styleOverrideObject);
	}

	return styleNames.length + (pushSOO ? 1 : 0);
}
```
- example usage
```shell
...
 * executes callback and then pops elements back. Returns value returned by callback
 *
 * @param  {Object}   item - an object with optional style property and/or style overrides
 * @param  {Function} function to be called between autopush and pop
 * @return {Object} value returned by callback
 */
StyleContextStack.prototype.auto = function (item, callback) {
	var pushedItems = this.autopush(item);
	var result = callback();

	if (pushedItems > 0) {
		this.pop(pushedItems);
	}

	return result;
...
```

#### <a name="apidoc.element.pdfmake.styleContextStack.prototype.clone"></a>[function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>clone ()](#apidoc.element.pdfmake.styleContextStack.prototype.clone)
- description and source-code
```javascript
clone = function () {
	var stack = new StyleContextStack(this.styleDictionary, this.defaultStyle);

	this.styleOverrides.forEach(function (item) {
		stack.styleOverrides.push(item);
	});

	return stack;
}
```
- example usage
```shell
...
	return node;
};

DocMeasure.prototype.measureLeaf = function (node) {

	// Make sure style properties of the node itself are considered when building inlines.
	// We could also just pass [node] to buildInlines, but that fails for bullet points.
	var styleStack = this.styleStack.clone();
	styleStack.push(node);

	var data = this.textTools.buildInlines(node.text, styleStack);

	node._inlines = data.items;
	node._minWidth = data.minWidth;
	node._maxWidth = data.maxWidth;
...
```

#### <a name="apidoc.element.pdfmake.styleContextStack.prototype.getProperty"></a>[function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>getProperty (property)](#apidoc.element.pdfmake.styleContextStack.prototype.getProperty)
- description and source-code
```javascript
getProperty = function (property) {
	if (this.styleOverrides) {
		for (var i = this.styleOverrides.length - 1; i >= 0; i--) {
			var item = this.styleOverrides[i];

			if (typeof item === 'string' || item instanceof String) {
				// named-style-override

				var style = this.styleDictionary[item];
				if (style && style[property] !== null && style[property] !== undefined) {
					return style[property];
				}
			} else {
				// style-overrides-object
				if (item[property] !== undefined && item[property] !== null) {
					return item[property];
				}
			}
		}
	}

	return this.defaultStyle && this.defaultStyle[property];
}
```
- example usage
```shell
...
		node._width = node._minWidth = node._maxWidth = imageSize.width * factor;
		node._height = imageSize.height * factor;
	} else {
		node._width = node._minWidth = node._maxWidth = node.width || imageSize.width;
		node._height = node.height || (imageSize.height * node._width / imageSize.width);
	}

	node._alignment = this.styleStack.getProperty('alignment');
	return node;
};

DocMeasure.prototype.measureLeaf = function (node) {

	// Make sure style properties of the node itself are considered when building inlines.
	// We could also just pass [node] to buildInlines, but that fails for bullet points.
...
```

#### <a name="apidoc.element.pdfmake.styleContextStack.prototype.pop"></a>[function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>pop (howMany)](#apidoc.element.pdfmake.styleContextStack.prototype.pop)
- description and source-code
```javascript
pop = function (howMany) {
	howMany = howMany || 1;

	while (howMany-- > 0) {
		this.styleOverrides.pop();
	}
}
```
- example usage
```shell
...
		availableHeight: this.availableHeight,
		availableWidth: this.availableWidth,
		lastColumnWidth: this.lastColumnWidth
	};
};

DocumentContext.prototype.completeColumnGroup = function () {
	var saved = this.snapshots.pop();

	this.calculateBottomMost(saved);

	this.endingCell = null;
	this.x = saved.x;
	this.y = saved.bottomMost.y;
	this.page = saved.bottomMost.page;
...
```

#### <a name="apidoc.element.pdfmake.styleContextStack.prototype.push"></a>[function <span class="apidocSignatureSpan">pdfmake.styleContextStack.prototype.</span>push (styleNameOrOverride)](#apidoc.element.pdfmake.styleContextStack.prototype.push)
- description and source-code
```javascript
push = function (styleNameOrOverride) {
	this.styleOverrides.push(styleNameOrOverride);
}
```
- example usage
```shell
...
		starMaxMin = 0,
		starMaxMax = 0,
		fixedColumns = [],
		initial_availableWidth = availableWidth;

	columns.forEach(function (column) {
		if (isAutoColumn(column)) {
			autoColumns.push(column);
			autoMin += column._minWidth;
			autoMax += column._maxWidth;
		} else if (isStarColumn(column)) {
			starColumns.push(column);
			starMaxMin = Math.max(starMaxMin, column._minWidth);
			starMaxMax = Math.max(starMaxMax, column._maxWidth);
		} else {
...
```



# <a name="apidoc.module.pdfmake.tableProcessor"></a>[module pdfmake.tableProcessor](#apidoc.module.pdfmake.tableProcessor)

#### <a name="apidoc.element.pdfmake.tableProcessor.tableProcessor"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>tableProcessor (tableNode)](#apidoc.element.pdfmake.tableProcessor.tableProcessor)
- description and source-code
```javascript
function TableProcessor(tableNode) {
	this.tableNode = tableNode;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.tableProcessor.prototype"></a>[module pdfmake.tableProcessor.prototype](#apidoc.module.pdfmake.tableProcessor.prototype)

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.beginRow"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>beginRow (rowIndex, writer)](#apidoc.element.pdfmake.tableProcessor.prototype.beginRow)
- description and source-code
```javascript
beginRow = function (rowIndex, writer) {
	this.topLineWidth = this.layout.hLineWidth(rowIndex, this.tableNode);
	this.rowPaddingTop = this.layout.paddingTop(rowIndex, this.tableNode);
	this.bottomLineWidth = this.layout.hLineWidth(rowIndex + 1, this.tableNode);
	this.rowPaddingBottom = this.layout.paddingBottom(rowIndex, this.tableNode);

	this.rowCallback = this.onRowBreak(rowIndex, writer);
	writer.tracker.startTracking('pageChanged', this.rowCallback);
	if (this.dontBreakRows) {
		writer.beginUnbreakableBlock();
	}
	this.rowTopY = writer.context().y;
	this.reservedAtBottom = this.bottomLineWidth + this.rowPaddingBottom;

	writer.context().availableHeight -= this.reservedAtBottom;

	writer.context().moveDown(this.rowPaddingTop);
}
```
- example usage
```shell
...
// tables
LayoutBuilder.prototype.processTable = function (tableNode) {
	var processor = new TableProcessor(tableNode);

	processor.beginTable(this.writer);

	for (var i = 0, l = tableNode.table.body.length; i < l; i++) {
		processor.beginRow(i, this.writer);

		var result = this.processRow(tableNode.table.body[i], tableNode.table.widths, tableNode._offsets.offsets, tableNode.table.body
, i);
		addAll(tableNode.positions, result.positions);

		processor.endRow(i, this.writer, result.pageBreaks);
	}
...
```

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.beginTable"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>beginTable (writer)](#apidoc.element.pdfmake.tableProcessor.prototype.beginTable)
- description and source-code
```javascript
beginTable = function (writer) {
	var tableNode;
	var availableWidth;
	var self = this;

	tableNode = this.tableNode;
	this.offsets = tableNode._offsets;
	this.layout = tableNode._layout;

	availableWidth = writer.context().availableWidth - this.offsets.total;
	ColumnCalculator.buildColumnWidths(tableNode.table.widths, availableWidth);

	this.tableWidth = tableNode._offsets.total + getTableInnerContentWidth();
	this.rowSpanData = prepareRowSpanData();
	this.cleanUpRepeatables = false;

	this.headerRows = tableNode.table.headerRows || 0;
	this.rowsWithoutPageBreak = this.headerRows + (tableNode.table.keepWithHeaderRows || 0);
	this.dontBreakRows = tableNode.table.dontBreakRows || false;

	if (this.rowsWithoutPageBreak) {
		writer.beginUnbreakableBlock();
	}

	// update the border properties of all cells before drawing any lines
	prepareCellBorders(this.tableNode.table.body);

	this.drawHorizontalLine(0, writer);

	function getTableInnerContentWidth() {
		var width = 0;

		tableNode.table.widths.forEach(function (w) {
			width += w._calcWidth;
		});

		return width;
	}

	function prepareRowSpanData() {
		var rsd = [];
		var x = 0;
		var lastWidth = 0;

		rsd.push({left: 0, rowSpan: 0});

		for (var i = 0, l = self.tableNode.table.body[0].length; i < l; i++) {
			var paddings = self.layout.paddingLeft(i, self.tableNode) + self.layout.paddingRight(i, self.tableNode);
			var lBorder = self.layout.vLineWidth(i, self.tableNode);
			lastWidth = paddings + lBorder + self.tableNode.table.widths[i]._calcWidth;
			rsd[rsd.length - 1].width = lastWidth;
			x += lastWidth;
			rsd.push({left: x, rowSpan: 0, width: 0});
		}

		return rsd;
	}

	// Iterate through all cells. If the current cell is the start of a
	// rowSpan/colSpan, update the border property of the cells on its
	// bottom/right accordingly. This is needed since each iteration of the
	// line-drawing loops draws lines for a single cell, not for an entire
	// rowSpan/colSpan.
	function prepareCellBorders(body) {
		for (var rowIndex = 0; rowIndex < body.length; rowIndex++) {
			var row = body[rowIndex];

			for (var colIndex = 0; colIndex < row.length; colIndex++) {
				var cell = row[colIndex];

				if (cell.border) {
					var rowSpan = cell.rowSpan || 1;
					var colSpan = cell.colSpan || 1;

					for (var rowOffset = 0; rowOffset < rowSpan; rowOffset++) {
						// set left border
						if (cell.border[0] !== undefined && rowOffset > 0) {
							setBorder(rowIndex + rowOffset, colIndex, 0, cell.border[0]);
						}

						// set right border
						if (cell.border[2] !== undefined) {
							setBorder(rowIndex + rowOffset, colIndex + colSpan - 1, 2, cell.border[2]);
						}
					}

					for (var colOffset = 0; colOffset < colSpan; colOffset++) {
						// set top border
						if (cell.border[1] !== undefined && colOffset > 0) {
							setBorder(rowIndex, colIndex + colOffset, 1, cell.border[1]);
						}

						// set bottom border
						if (cell.border[3] !== undefined) {
							setBorder(rowIndex + rowSpan - 1, colIndex + colOffset, 3, cell.border[3]);
						}
					}
				}
			}
		}

		// helper function to set the border for a given cell
		function setBorder(rowIndex, colIndex, borderIndex, borderValue) {
			var cell = body[rowIndex][colIndex];
			cell.border = cell.border || {};
			cell.border[borderIndex] = borderValue;
		}
	}
}
```
- example usage
```shell
...
	}
};

// tables
LayoutBuilder.prototype.processTable = function (tableNode) {
	var processor = new TableProcessor(tableNode);

	processor.beginTable(this.writer);

	for (var i = 0, l = tableNode.table.body.length; i < l; i++) {
		processor.beginRow(i, this.writer);

		var result = this.processRow(tableNode.table.body[i], tableNode.table.widths, tableNode._offsets.offsets, tableNode.table.body
, i);
		addAll(tableNode.positions, result.positions);
...
```

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.drawHorizontalLine"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>drawHorizontalLine (lineIndex, writer, overrideY)](#apidoc.element.pdfmake.tableProcessor.prototype.drawHorizontalLine)
- description and source-code
```javascript
drawHorizontalLine = function (lineIndex, writer, overrideY) {
	var lineWidth = this.layout.hLineWidth(lineIndex, this.tableNode);
	if (lineWidth) {
		var offset = lineWidth / 2;
		var currentLine = null;
		var body = this.tableNode.table.body;

		for (var i = 0, l = this.rowSpanData.length; i < l; i++) {
			var data = this.rowSpanData[i];
			var shouldDrawLine = !data.rowSpan;

			// draw only if the current cell requires a top border or the cell in the
			// row above requires a bottom border
			if (shouldDrawLine && i < l - 1) {
				var topBorder = false, bottomBorder = false;

				// the current cell
				if (lineIndex < body.length) {
					var cell = body[lineIndex][i];
					topBorder = cell.border ? cell.border[1] : this.layout.defaultBorder;
				}

				// the cell in the row above
				if (lineIndex > 0) {
					var cellAbove = body[lineIndex - 1][i];
					bottomBorder = cellAbove.border ? cellAbove.border[3] : this.layout.defaultBorder;
				}

				shouldDrawLine = topBorder || bottomBorder;
			}

			if (!currentLine && shouldDrawLine) {
				currentLine = {left: data.left, width: 0};
			}

			if (shouldDrawLine) {
				currentLine.width += (data.width || 0);
			}

			var y = (overrideY || 0) + offset;

			if (!shouldDrawLine || i === l - 1) {
				if (currentLine && currentLine.width) {
					writer.addVector({
						type: 'line',
						x1: currentLine.left,
						x2: currentLine.left + currentLine.width,
						y1: y,
						y2: y,
						lineWidth: lineWidth,
						lineColor: typeof this.layout.hLineColor === 'function' ? this.layout.hLineColor(lineIndex, this.tableNode) : this.layout.
hLineColor
					}, false, overrideY);
					currentLine = null;
				}
			}
		}

		writer.context().moveDown(lineWidth);
	}
}
```
- example usage
```shell
...
	if (this.rowsWithoutPageBreak) {
		writer.beginUnbreakableBlock();
	}

	// update the border properties of all cells before drawing any lines
	prepareCellBorders(this.tableNode.table.body);

	this.drawHorizontalLine(0, writer);

	function getTableInnerContentWidth() {
		var width = 0;

		tableNode.table.widths.forEach(function (w) {
			width += w._calcWidth;
		});
...
```

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.drawVerticalLine"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>drawVerticalLine (x, y0, y1, vLineIndex, writer)](#apidoc.element.pdfmake.tableProcessor.prototype.drawVerticalLine)
- description and source-code
```javascript
drawVerticalLine = function (x, y0, y1, vLineIndex, writer) {
	var width = this.layout.vLineWidth(vLineIndex, this.tableNode);
	if (width === 0) {
		return;
	}
	writer.addVector({
		type: 'line',
		x1: x + width / 2,
		x2: x + width / 2,
		y1: y0,
		y2: y1,
		lineWidth: width,
		lineColor: typeof this.layout.vLineColor === 'function' ? this.layout.vLineColor(vLineIndex, this.tableNode) : this.layout.vLineColor
	}, false, true);
}
```
- example usage
```shell
...
			// the cell from before column
			if (colIndex > 0) {
				var cell = body[rowIndex][colIndex - 1];
				rightBorder = cell.border ? cell.border[2] : this.layout.defaultBorder;
			}

			if (leftBorder || rightBorder) {
				this.drawVerticalLine(xs[i].x, y1 - hzLineOffset, y2 + this.bottomLineWidth, xs[i].index, writer);
			}

			if (i < l - 1) {
				var fillColor = body[rowIndex][colIndex].fillColor;
				if (!fillColor) {
					fillColor = typeof this.layout.fillColor === 'function' ? this.layout.fillColor(rowIndex, this.tableNode) : this.layout.fillColor
;
				}
...
```

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.endRow"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>endRow (rowIndex, writer, pageBreaks)](#apidoc.element.pdfmake.tableProcessor.prototype.endRow)
- description and source-code
```javascript
endRow = function (rowIndex, writer, pageBreaks) {
	var l, i;
	var self = this;
	writer.tracker.stopTracking('pageChanged', this.rowCallback);
	writer.context().moveDown(this.layout.paddingBottom(rowIndex, this.tableNode));
	writer.context().availableHeight += this.reservedAtBottom;

	var endingPage = writer.context().page;
	var endingY = writer.context().y;

	var xs = getLineXs();

	var ys = [];

	var hasBreaks = pageBreaks && pageBreaks.length > 0;
	var body = this.tableNode.table.body;

	ys.push({
		y0: this.rowTopY,
		page: hasBreaks ? pageBreaks[0].prevPage : endingPage
	});

	if (hasBreaks) {
		for (i = 0, l = pageBreaks.length; i < l; i++) {
			var pageBreak = pageBreaks[i];
			ys[ys.length - 1].y1 = pageBreak.prevY;

			ys.push({y0: pageBreak.y, page: pageBreak.prevPage + 1});
		}
	}

	ys[ys.length - 1].y1 = endingY;

	var skipOrphanePadding = (ys[0].y1 - ys[0].y0 === this.rowPaddingTop);
	for (var yi = (skipOrphanePadding ? 1 : 0), yl = ys.length; yi < yl; yi++) {
		var willBreak = yi < ys.length - 1;
		var rowBreakWithoutHeader = (yi > 0 && !this.headerRows);
		var hzLineOffset = rowBreakWithoutHeader ? 0 : this.topLineWidth;
		var y1 = ys[yi].y0;
		var y2 = ys[yi].y1;

		if (willBreak) {
			y2 = y2 + this.rowPaddingBottom;
		}

		if (writer.context().page != ys[yi].page) {
			writer.context().page = ys[yi].page;

			//TODO: buggy, availableHeight should be updated on every pageChanged event
			// TableProcessor should be pageChanged listener, instead of processRow
			this.reservedAtBottom = 0;
		}

		for (i = 0, l = xs.length; i < l; i++) {
			var leftBorder = false, rightBorder = false;
			var colIndex = xs[i].index;

			// the current cell
			if (colIndex < body[rowIndex].length) {
				var cell = body[rowIndex][colIndex];
				leftBorder = cell.border ? cell.border[0] : this.layout.defaultBorder;
			}

			// the cell from before column
			if (colIndex > 0) {
				var cell = body[rowIndex][colIndex - 1];
				rightBorder = cell.border ? cell.border[2] : this.layout.defaultBorder;
			}

			if (leftBorder || rightBorder) {
				this.drawVerticalLine(xs[i].x, y1 - hzLineOffset, y2 + this.bottomLineWidth, xs[i].index, writer);
			}

			if (i < l - 1) {
				var fillColor = body[rowIndex][colIndex].fillColor;
				if (!fillColor) {
					fillColor = typeof this.layout.fillColor === 'function' ? this.layout.fillColor(rowIndex, this.tableNode) : this.layout.fillColor
;
				}
				if (fillColor) {
					var wBorder = (leftBorder || rightBorder) ? this.layout.vLineWidth(colIndex, this.tableNode) : 0;
					var xf = xs[i].x + wBorder;
					var yf = this.dontBreakRows ? y1 : y1 - hzLineOffset;
					writer.addVector({
						type: 'rect',
						x: xf,
						y: yf,
						w: xs[i + 1].x - xf,
						h: y2 + this.bottomLineWidth - yf,
						lineWidth: 0,
						color: fillColor
					}, false, true, 0);
				}
			}
		}

		if (willBreak && this.layout.hLineWhenBroken !== false) {
			this.drawHorizontalLine(rowIndex + 1, writer, y2);
		}
		if (rowBreakWithoutHeader && this.layout.hLineWhenBroken !== false) {
			this.drawHorizontalLine(rowIndex, writer, y1);
		}
	}

	writer.context().page = endingPage;
	writer.context().y = endingY;

	var row = this.tableNode.table.body[rowIndex];
	for (i = 0, l = row.length; i < l; i++) {
		if (row[i].rowSpan) {
			this.rowSpanData[i].rowSpan = row[i].rowSpan;

			// fix colSpans
			if (row[i].colSpan && row[i].colSpan > 1) {
				for (var j = 1; j < row[i].rowSpan; j++) {
					this.tableNode.table.body[rowIndex + j][i]._colSpan = row[i].colSpan;
				}
			}
		}

		if (this.rowSpanData[i].rowSpan > 0) {
			this.rowSpanData[i].rowSpan--;
		}
	}

	this.drawHorizontalLine(rowIndex + 1, writer);

	if (this.headerRows && rowIndex === this.headerRows - 1) {
		this.headerRepeatable = writer.currentBlockToRepeatable();
	}

	if (this.dontBreakRows) {
		writer.tracker.auto('pageChanged',
			function () {
				if (!self.headerRows && self.layout.hLineWhenBroken !== false) {
					self.drawHorizontalL ...
```
- example usage
```shell
...

	for (var i = 0, l = tableNode.table.body.length; i < l; i++) {
		processor.beginRow(i, this.writer);

		var result = this.processRow(tableNode.table.body[i], tableNode.table.widths, tableNode._offsets.offsets, tableNode.table.body
, i);
		addAll(tableNode.positions, result.positions);

		processor.endRow(i, this.writer, result.pageBreaks);
	}

	processor.endTable(this.writer);
};

// leafs (texts)
LayoutBuilder.prototype.processLeaf = function (node) {
...
```

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.endTable"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>endTable (writer)](#apidoc.element.pdfmake.tableProcessor.prototype.endTable)
- description and source-code
```javascript
endTable = function (writer) {
	if (this.cleanUpRepeatables) {
		writer.popFromRepeatables();
	}
}
```
- example usage
```shell
...

		var result = this.processRow(tableNode.table.body[i], tableNode.table.widths, tableNode._offsets.offsets, tableNode.table.body
, i);
		addAll(tableNode.positions, result.positions);

		processor.endRow(i, this.writer, result.pageBreaks);
	}

	processor.endTable(this.writer);
};

// leafs (texts)
LayoutBuilder.prototype.processLeaf = function (node) {
	var line = this.buildNextLine(node);
	var currentHeight = (line) ? line.getHeight() : 0;
	var maxHeight = node.maxHeight || -1;
...
```

#### <a name="apidoc.element.pdfmake.tableProcessor.prototype.onRowBreak"></a>[function <span class="apidocSignatureSpan">pdfmake.tableProcessor.prototype.</span>onRowBreak (rowIndex, writer)](#apidoc.element.pdfmake.tableProcessor.prototype.onRowBreak)
- description and source-code
```javascript
onRowBreak = function (rowIndex, writer) {
	var self = this;
	return function () {
		//console.log('moving by : ', topLineWidth, rowPaddingTop);
		var offset = self.rowPaddingTop + (!self.headerRows ? self.topLineWidth : 0);
		writer.context().moveDown(offset);
	};

}
```
- example usage
```shell
...

TableProcessor.prototype.beginRow = function (rowIndex, writer) {
	this.topLineWidth = this.layout.hLineWidth(rowIndex, this.tableNode);
	this.rowPaddingTop = this.layout.paddingTop(rowIndex, this.tableNode);
	this.bottomLineWidth = this.layout.hLineWidth(rowIndex + 1, this.tableNode);
	this.rowPaddingBottom = this.layout.paddingBottom(rowIndex, this.tableNode);

	this.rowCallback = this.onRowBreak(rowIndex, writer);
	writer.tracker.startTracking('pageChanged', this.rowCallback);
	if (this.dontBreakRows) {
		writer.beginUnbreakableBlock();
	}
	this.rowTopY = writer.context().y;
	this.reservedAtBottom = this.bottomLineWidth + this.rowPaddingBottom;
...
```



# <a name="apidoc.module.pdfmake.textDecorator"></a>[module pdfmake.textDecorator](#apidoc.module.pdfmake.textDecorator)

#### <a name="apidoc.element.pdfmake.textDecorator.drawBackground"></a>[function <span class="apidocSignatureSpan">pdfmake.textDecorator.</span>drawBackground (line, x, y, pdfKitDoc)](#apidoc.element.pdfmake.textDecorator.drawBackground)
- description and source-code
```javascript
function drawBackground(line, x, y, pdfKitDoc) {
	var height = line.getHeight();
	for (var i = 0, l = line.inlines.length; i < l; i++) {
		var inline = line.inlines[i];
		if (inline.background) {
			pdfKitDoc.fillColor(inline.background)
				.rect(x + inline.x, y, inline.width, height)
				.fill();
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdfmake.textDecorator.drawDecorations"></a>[function <span class="apidocSignatureSpan">pdfmake.textDecorator.</span>drawDecorations (line, x, y, pdfKitDoc)](#apidoc.element.pdfmake.textDecorator.drawDecorations)
- description and source-code
```javascript
function drawDecorations(line, x, y, pdfKitDoc) {
	var groups = groupDecorations(line);
	for (var i = 0, l = groups.length; i < l; i++) {
		drawDecoration(groups[i], x, y, pdfKitDoc);
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.textTools"></a>[module pdfmake.textTools](#apidoc.module.pdfmake.textTools)

#### <a name="apidoc.element.pdfmake.textTools.textTools"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>textTools (fontProvider)](#apidoc.element.pdfmake.textTools.textTools)
- description and source-code
```javascript
function TextTools(fontProvider) {
	this.fontProvider = fontProvider;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.textTools.prototype"></a>[module pdfmake.textTools.prototype](#apidoc.module.pdfmake.textTools.prototype)

#### <a name="apidoc.element.pdfmake.textTools.prototype.buildInlines"></a>[function <span class="apidocSignatureSpan">pdfmake.textTools.prototype.</span>buildInlines (textArray, styleContextStack)](#apidoc.element.pdfmake.textTools.prototype.buildInlines)
- description and source-code
```javascript
buildInlines = function (textArray, styleContextStack) {
	var measured = measure(this.fontProvider, textArray, styleContextStack);

	var minWidth = 0,
		maxWidth = 0,
		currentLineWidth;

	measured.forEach(function (inline) {
		minWidth = Math.max(minWidth, inline.width - inline.leadingCut - inline.trailingCut);

		if (!currentLineWidth) {
			currentLineWidth = {width: 0, leadingCut: inline.leadingCut, trailingCut: 0};
		}

		currentLineWidth.width += inline.width;
		currentLineWidth.trailingCut = inline.trailingCut;

		maxWidth = Math.max(maxWidth, getTrimmedWidth(currentLineWidth));

		if (inline.lineEnd) {
			currentLineWidth = null;
		}
	});

	if (getStyleProperty({}, styleContextStack, 'noWrap', false)) {
		minWidth = maxWidth;
	}

	return {
		items: measured,
		minWidth: minWidth,
		maxWidth: maxWidth
	};

	function getTrimmedWidth(item) {
		return Math.max(0, item.width - item.leadingCut - item.trailingCut);
	}
}
```
- example usage
```shell
...
DocMeasure.prototype.measureLeaf = function (node) {

	// Make sure style properties of the node itself are considered when building inlines.
	// We could also just pass [node] to buildInlines, but that fails for bullet points.
	var styleStack = this.styleStack.clone();
	styleStack.push(node);

	var data = this.textTools.buildInlines(node.text, styleStack);

	node._inlines = data.items;
	node._minWidth = data.minWidth;
	node._maxWidth = data.maxWidth;

	return node;
};
...
```

#### <a name="apidoc.element.pdfmake.textTools.prototype.sizeOfString"></a>[function <span class="apidocSignatureSpan">pdfmake.textTools.prototype.</span>sizeOfString (text, styleContextStack)](#apidoc.element.pdfmake.textTools.prototype.sizeOfString)
- description and source-code
```javascript
sizeOfString = function (text, styleContextStack) {
	text = text ? text.toString().replace('\t', '    ') : '';

	//TODO: refactor - extract from measure
	var fontName = getStyleProperty({}, styleContextStack, 'font', 'Roboto');
	var fontSize = getStyleProperty({}, styleContextStack, 'fontSize', 12);
	var bold = getStyleProperty({}, styleContextStack, 'bold', false);
	var italics = getStyleProperty({}, styleContextStack, 'italics', false);
	var lineHeight = getStyleProperty({}, styleContextStack, 'lineHeight', 1);

	var font = this.fontProvider.provideFont(fontName, bold, italics);

	return {
		width: font.widthOfString(text, fontSize),
		height: font.lineHeight(fontSize) * lineHeight,
		fontSize: fontSize,
		lineHeight: lineHeight,
		ascender: font.ascender / 1000 * fontSize,
		descender: font.descender / 1000 * fontSize
	};
}
```
- example usage
```shell
...
		node._maxWidth = Math.max(node._maxWidth, items[i]._maxWidth);
	}

	return node;
};

DocMeasure.prototype.gapSizeForList = function () {
	return this.textTools.sizeOfString('9. ', this.styleStack);
};

DocMeasure.prototype.buildUnorderedMarker = function (styleStack, gapSize, type) {
	function buildDisc(gapSize, color) {
		// TODO: ascender-based calculations
		var radius = gapSize.fontSize / 6;
		return {
...
```



# <a name="apidoc.module.pdfmake.traversalTracker"></a>[module pdfmake.traversalTracker](#apidoc.module.pdfmake.traversalTracker)

#### <a name="apidoc.element.pdfmake.traversalTracker.traversalTracker"></a>[function <span class="apidocSignatureSpan">pdfmake.</span>traversalTracker ()](#apidoc.element.pdfmake.traversalTracker.traversalTracker)
- description and source-code
```javascript
function TraversalTracker() {
	this.events = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdfmake.traversalTracker.prototype"></a>[module pdfmake.traversalTracker.prototype](#apidoc.module.pdfmake.traversalTracker.prototype)

#### <a name="apidoc.element.pdfmake.traversalTracker.prototype.auto"></a>[function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>auto (event, cb, innerBlock)](#apidoc.element.pdfmake.traversalTracker.prototype.auto)
- description and source-code
```javascript
auto = function (event, cb, innerBlock) {
	this.startTracking(event, cb);
	innerBlock();
	this.stopTracking(event, cb);
}
```
- example usage
```shell
...
	if (Object.keys(node).length === 0) {
		// A warning could be logged: console.warn('pdfmake: Empty node, ignoring it');
		node = {text: ''};
	}

	var self = this;

	return this.styleStack.auto(node, function () {
		// TODO: refactor + rethink whether this is the proper way to handle margins
		node._margin = getNodeMargin(node);

		if (node.columns) {
			return extendMargins(self.measureColumns(node));
		} else if (node.stack) {
			return extendMargins(self.measureVerticalContainer(node));
...
```

#### <a name="apidoc.element.pdfmake.traversalTracker.prototype.emit"></a>[function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>emit (event)](#apidoc.element.pdfmake.traversalTracker.prototype.emit)
- description and source-code
```javascript
emit = function (event) {
	var args = Array.prototype.slice.call(arguments, 1);

	var callbacks = this.events[event];

	if (callbacks) {
		callbacks.forEach(function (cb) {
			cb.apply(this, args);
		});
	}
}
```
- example usage
```shell
...

DocumentContext.prototype.addPage = function (pageSize) {
	var page = {items: [], pageSize: pageSize};
	this.pages.push(page);
	this.page = this.pages.length - 1;
	this.initializePage();

	this.tracker.emit('pageAdded');

	return page;
};

DocumentContext.prototype.getCurrentPage = function () {
	if (this.page < 0 || this.page >= this.pages.length) {
		return null;
...
```

#### <a name="apidoc.element.pdfmake.traversalTracker.prototype.startTracking"></a>[function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>startTracking (event, cb)](#apidoc.element.pdfmake.traversalTracker.prototype.startTracking)
- description and source-code
```javascript
startTracking = function (event, cb) {
	var callbacks = (this.events[event] || (this.events[event] = []));

	if (callbacks.indexOf(cb) < 0) {
		callbacks.push(cb);
	}
}
```
- example usage
```shell
...
	this.linearNodeList = [];
	docStructure = this.docMeasure.measureDocument(docStructure);

	this.writer = new PageElementWriter(
		new DocumentContext(this.pageSize, this.pageMargins), this.tracker);

	var _this = this;
	this.writer.context().tracker.startTracking('pageAdded', function () {
		_this.addBackground(background);
	});

	this.addBackground(background);
	this.processNode(docStructure);
	this.addHeadersAndFooters(header, footer);
	/* jshint eqnull:true */
...
```

#### <a name="apidoc.element.pdfmake.traversalTracker.prototype.stopTracking"></a>[function <span class="apidocSignatureSpan">pdfmake.traversalTracker.prototype.</span>stopTracking (event, cb)](#apidoc.element.pdfmake.traversalTracker.prototype.stopTracking)
- description and source-code
```javascript
stopTracking = function (event, cb) {
	var callbacks = this.events[event];

	if (callbacks) {
		var index = callbacks.indexOf(cb);
		if (index >= 0) {
			callbacks.splice(index, 1);
		}
	}
}
```
- example usage
```shell
...
		writer.popFromRepeatables();
	}
};

TableProcessor.prototype.endRow = function (rowIndex, writer, pageBreaks) {
	var l, i;
	var self = this;
	writer.tracker.stopTracking('pageChanged', this.rowCallback);
	writer.context().moveDown(this.layout.paddingBottom(rowIndex, this.tableNode));
	writer.context().availableHeight += this.reservedAtBottom;

	var endingPage = writer.context().page;
	var endingY = writer.context().y;

	var xs = getLineXs();
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
