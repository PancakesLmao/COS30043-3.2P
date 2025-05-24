# How did it work?

## Folder structure:
```
|__ framework
|   |__ js (JavaScript files)
|   |__ css (CSS files)
|   |__ assets (Image files)
|   |__ lookup1.html 
|   |__ README.md
```
## How to run:
1. Download/clone the repository
2. Install Live Server extension in Visual Studio Code (if not already installed)
   - Open Visual Studio Code
   - Go to Extensions (Ctrl+Shift+X)
   - Search for "Live Server" and install it
3. In visual studio code, choose  `Go Live`. The website will open in your default browser via port 5500.

## How data is fetched:
- I figured reading data directly from .txt file would be troublesome, so i decided to use github jsDelivr CDN, which contains a JSON object with the data.
- I then simply used the fetch() object to retrieve the data from the URL. Visit this blog for more (https://viblo.asia/p/requests-vue-nen-cho-fetch-api-hay-axios-bWrZnz1wZxw)
- This repo is public so you can visit the URL to see the data: 
`https://cdn.jsdelivr.net/gh/PancakesLmao/COS30043-3.2P@master/assets/3_2_resource.txt`