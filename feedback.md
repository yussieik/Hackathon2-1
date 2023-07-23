Hello Svetlana,

Congratulations on developing this comprehensive script that fetches and processes data from the OpenTripMap API. Your code is generally well-structured and clean. I appreciate how you have separated functionality into different functions for better readability and maintenance. Here are my comments and suggestions:

**JavaScript (script.js):**

1. **Securing API Keys:** Your `apiKey` variable is openly declared in your script, which is a security risk as anyone who views your source code can misuse it. Consider storing it in a secure environment file or some sort of back-end configuration that cannot be accessed publicly.

2. **Error Handling:** While you handle network errors in your fetch function, you could provide a more robust error handling process. Specifically, it would be useful to handle API errors, such as if the API returns a non-200 status code. Remember, fetch() only rejects a promise when a network error is encountered. 

3. **Template Literals:** For the sake of readability, you might want to utilize template literals (backticks) for string concatenation in your `otmAPI` and other similar lines.

4. **Promises:** The use of Promises is well executed, but you can enhance it by using async/await syntax, which makes your asynchronous code look more like traditional synchronous code.

5. **querySelector and getElementById:** I noticed that you are using both `document.getElementById` and `document.querySelector`. While both can be used interchangeably, you might want to keep it consistent across the application for code uniformity and better readability.

**HTML (index.html):**

1. **Header Outside Body:** I noticed that the `<header>` is outside the `<body>` tag. According to HTML5 semantics, the `<header>` should be inside the `<body>`. 

2. **Semantic HTML:** Consider making use of more semantic HTML elements like `<section>`, `<article>`, etc. Semantic elements make it easier for screen readers and search engine crawlers to understand the meaning of the layout.

3. **Title Attribute for iFrame:** You have an iFrame commented out with a `title` attribute in the style tag. It's good for accessibility, but ensure it describes the content of the iframe.

**CSS:**

1. **Inline Styles:** Avoid using inline styles like `height: 36%;` in the `#map` class, instead define them in your CSS files for better organization and maintainability.

2. **Media Query:** Your media query for images is well implemented. It enhances the responsiveness of your webpage, good job on that.

3. **CSS Commenting:** Some of your commented-out styles might cause confusion in the future when revisiting the code or for other developers. You should remove them if they're not necessary.

Overall, your work is commendable and these suggestions are meant to improve the effectiveness of your code. Keep up the good work! 

Best,
Yossi.