# shasam-list
Get your list of shazams

1. Log in Shazam.com (via email link for FB account).

2. Click on "My Shazam" link in top menu (Go to https://www.shazam.com/ru/myshazam )

3. Scroll to bottom, wait and repeat this item until you reach the end of list. [Will be automated with script later]
OR, You can automate it with following script: Just copy it and paste in browser address line.
```javascript
javascript: window._scrollIntervalId = setInterval(function(){ var _scrollable = document.querySelector('.root'), _lastScrollTop = window._lastScrollTop = window._lastScrollTop || _scrollable.scrollHeight; if(window._lastScrollTop != _scrollable.scrollTop) { _scrollable.scrollTop = _scrollable.scrollHeight; setTimeout(function(){window._lastScrollTop = _scrollable.scrollTop}, 100); console.log('loading next records...'); } else {clearInterval(window._scrollIntervalId); delete window._scrollIntervalId; console.log('loading finished.'); alert('Whole list loaded.');} }, 5000);
```
NOTE: Some browsers (Chrome?) cut "javascript:" left part of your paste, so you need add this manually in this case.

4. Paste following code in your browser address line:
```javascript
javascript: console.log('Your Shazam List... =====================================================================\r\n', Array.prototype.slice.apply(document.querySelector('.panel-bd.panel-bd-wide').children).reduce(function(list, li){list.push(li.querySelector('.artist').textContent.trim() + '  -  ' +  li.querySelector('.title').textContent.trim()); return list}, []).join('\r\n'), '\r\nEnd of List ========================================================================\r\n');
```
NOTE: Some browsers (Chrome?) cut "javascript:" left part of your paste, so you need add this manually in this case.

5. Open Browser console, select output and copy it in clipboard to paste it then somewhere in text file.
