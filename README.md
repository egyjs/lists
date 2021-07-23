# lists
repository contains a large lists that i have generated and its source


```javascript
function download(content, fileName, contentType='text/plain') {
    var a = document.createElement("a");
    var file = new Blob([content], {type: contentType});
    a.href = URL.createObjectURL(file);
    a.download = fileName;
    a.click();
}
download(JSON.stringify(ARRAYNAME), 'ARRAYNAME.json');
```
