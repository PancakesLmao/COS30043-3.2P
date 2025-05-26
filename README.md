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

## How data is filtered:
- I used the `filter()` method of Javascript to filter the data based on the search query. The `filter()` method creates a new array with all elements that pass the test implemented by the provided function. Each unit is tested against three different conditions:

   - codeMatch: Checks if the unit's code contains the text in this.codeFilter. If this.codeFilter is empty, all units pass this check.

   - descMatch: Checks if the unit's description contains the text in this.descFilter. If this.descFilter is empty, all units pass this check.

   - typeMatch: Checks if the unit's type exactly matches this.typeFilter. If this.typeFilter is set to 'All', all units pass this check.

- The `toLowerCase()` method is used to make the search case-insensitive.
- The `includes()` method is used to check if the search query is present in the name or description of the resource.
- Sorting is done using the `sort()` method, which sorts the filtered resources based on their code in ascending order.
