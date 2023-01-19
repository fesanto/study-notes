### What does a doctype do?
It's the HTML document type declaration, the instruction to the web browser about what version of HTML the page is written in.

### How do you serve a page with content in multiple languages?
To change the language, just simply set the lang attribute. 
<p>French "<span lang="fr">Bonjour</span>" </p>
But, first of all, you will need to choose the primary language at the beginning of the page. 
<html lang="en">

### What kind of things must you be wary of when designing or developing for multilingual sites?
Be sure to use lang attribute in the HTML. Colours are perceived differently across languages and cultures. Be careful with formatting dates and currencies, and with language reading direction.

### What are data- attributes good for?
It serves to customize and manipulate data.

### Consider HTML5 as an open web platform. What are the building blocks of HTML5?
Semantics: allowing you to describe more precisely what your content is. 
Connectivity: allowing you to communicate with the server in new and innovative ways.
Offline and storage: allowing webpages to store data on the client-side locally and operate offline more efficiently.

### Describe the difference between a cookie, sessionStorage and localStorage.
Session and local storage are web storage methods and can only be read on client-side. Session's data is lost when the browser or the tab are closed. Local's data need to be deleted via JS or manually.
Cookies are primarily for server-side reading (can also be read on client-side). It can be session or persistent. 
SessionLocal storage helps store data that the user will need to access later, such as offline data. Session storage is a great way to improve the performance of your web applications. Cookies are a good choice for storing data that should not be persisted for a long time, such as session IDs.

### Describe the difference between <script>, <script async> and <script defer>.
*<script> Normal execution is the default behavior of the <script> element. Parsing of the HTML code pauses while the script is executing. For slow servers and heavy scripts this means that displaying the webpage will be delayed.
*<script defer> Deferred script execution until the HTML parser has finished. A positive effect of this attribute is that the DOM will be available for your script. However, since not every browser supports defer yet, don’t rely on it!
*<script async> Asynchronous execution is the best of both worlds: HTML parsing may continue and the script will be executed as soon as it’s ready. I’d recommend this for scripts such as Google Analytics.

### Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions?
In a nutshell, such a placement of CSS <link>s and JavaScript <script>s allows for faster rendering of the page and better overall performance because when a page first loads, HTML and CSS are being parsed simultaneously and placing CSS <link>s in the <head> ensures that the stylesheets are loaded and ready for use when the browser starts rendering the page.
<script> tags block HTML parsing while they are being downloaded and executed, which can slow down the display of your page. Placing the <script>s at the bottom will allow the HTML to be parsed and displayed to the user first. If you need to put <script>s in the <head>, use the defer attribute, which will achieve the same effect of running the script only after the HTML is parsed but the browser can kick off the network request earlier to download the script.