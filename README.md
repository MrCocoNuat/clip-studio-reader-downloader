# clip-studio-reader-downloader
Tampermonkey userscript to download books from the browser version of Clip Studio Reader as a zip file

## Install this script

You must have a userscript browser extension installed (any will do):
- [GreaseMonkey](https://www.greasespot.net/)
- [Tampermonkey](http://tampermonkey.net/)
- [Violentmonkey](https://violentmonkey.github.io/)
  
Once that is done, simply...
- [Install from GreasyFork](https://github.com/MrCocoNuat/clip-studio-reader-downloader/raw/main/clip-studio-reader-downloader.js)](https://greasyfork.org/en/scripts/481576-clip-studio-reader-downloader)

## How to Use
1. Open a book in Clip Studio Reader (the URL should match https://mbj-bs.pf.mobilebook.jp/*)
2. Click the cool-looking purple download button
3. Sit back, each 100 pages takes approximately 1 minute to download
4. Save your book, now as a zip file
   
![image](https://github.com/MrCocoNuat/clip-studio-reader-downloader/assets/28863780/e8541293-31e2-49a3-ab62-c9b7efe80afd)

## Mechanism
This userscript extracts rendered canvases from the book reader, packages them into a zip file with [JSZip](https://github.com/Stuk/jszip), and presents the zip file to you with [FileSaver.js](https://github.com/eligrey/FileSaver.js).

## Something Went Wrong?
This userscript logs to the console (Developer Tools) with lines beginning with `[CSRD]:`. Take a look there to see if anything immediately obvious happened, otherwise feel free to open an issue here!

### Memory Usage
This userscript holds the entire zip file in memory. While this should typically not present any problems, exceptionally large books (4GB+, or over 2000 pages) and low system memory may result in `Out Of Memory` Errors. Please open an issue and tell me if you ever see this happening!

This userscript was developed and tested on Firefox.
