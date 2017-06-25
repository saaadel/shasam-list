# shasam-list
Get your list of shazams

1. Log in Shazam.com (via email link for FB account).
2. Click on "My Shazam" link in top menu (Go to https://www.shazam.com/ru/myshazam )
3. Scroll to bottom, wait and repeat this item until you reach the end of list. [Will be automated with script later]
4. Paste following code in your browser addressline:
```javascript
javascript: console.log('Your Shazam List: =====================================================================\r\n', Array.prototype.slice.apply(document.querySelector('.panel-bd.panel-bd-wide').children).reduce(function(list, li){list.push(li.querySelector('.title').textContent.trim() + '  -  ' +  li.querySelector('.artist').textContent.trim()); return list}, []).join('\r\n'));
```
NOTE: Some browsers (Chrome?) cut "javascript:" left part of your paste, so you need add this manually in this case.
5. Open Browser console, select output and copy it in clipboard to paste it then somewhere in text file.
