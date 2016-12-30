## How to run this project?

Open the `index.html` in browser or anyone appropriate editor


## Update notes

1. I added some codes to ensure allFeeds object has valid url

	```javascript
	it('urls are valid',function() {
            allFeeds.forEach(function(feed){
                expect(feed.url).toBeDefined();
                expect(feed.url.length).not.toBe(0);
            });
        });
    ```
2. Some new codes to check if allFeeds object has some valid names

	```javascript
	it('all has a name',function() {
        allFeeds.forEach(function(feed){
            expect(feed.name).toBeDefined();
            expect(feed.name).not.toBeNull();
        });
    });
    ```

3. I added a new test suite named `"The menu"`, it judged whether the menu is valid by testing for the presence or absence of class `'menu-hidden'` in `'body'`.

4. In order to ensure the feeds is loaded successfully, which means function `loadFeed()` is called and completes its work, I added a new test suite named `"Initial Entries"` to check it.

5. A new test suite named `"New Feed Selection"` was added to ensure the content of feeds actually changes when a new feed is loaded.

6. At line 39 in `index.html`, I changed `<p>{{contextSnippet}}</p>` into

	```html
	<p>{{description}}</p>
    ```
    so that context snippets can loaded successfully.