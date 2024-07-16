

## Standard script tag
```
<script src="script.js"></script>
```
When the browser is parsing the html and comes across this line, then it stops html parsing, downloads the script.js and executes the script file immediately. After the script is done executing then only the html parsing continues.
- Order of Execution: Scripts are executed in the order they appear in the HTML document.

## script tag with async boolean attribute
```
<script src="script.js" async></script>
```
When the browser comes across this line then, the browser will download the script asynchronously, meaning the HTML parsing will not be blocked while the script is being fetched. Once the script is downloaded, it will execute immediately, potentially before the rest of the HTML is parsed.

- Order of Execution: Scripts marked with async are executed as soon as they are downloaded, which means they may not be executed in the order they appear in the HTML document if multiple async scripts are used.
- Suitable for scripts that do not depend on other scripts or the DOM being fully parsed (e.g., analytics scripts).
    
## script tag with defer boolean attribute
```
<script src="script.js" defer></script>
```
When teh browser comes across this line then it downloads the script file asynchronously. The html parsing continues. However, unlike async, the script is not executed when the file is downloaded. The script is executed only after the html parsing finishes but before the DOMContentLoaded event fires.
- Scripts with the defer attribute maintain their order of appearance in the HTML document, ensuring they are executed sequentially.
- Suitable for scripts that depend on the DOM being fully parsed or on other scripts, ensuring they execute in the intended order.


![image](https://github.com/user-attachments/assets/44f75269-2cc9-493f-8a57-6c09169df8fe)
