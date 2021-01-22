# The past presetn and future of local storage for web applications

### history

It was a struggle in the past having a unified web storage capacity. Whether it was dedicated browser plugins or flash adding its own storage uniting under one common storage flag was on ongoing debate. Thi is to say only for web applications.


### html 5 storage (local storage)

Finally a browser native way to save state for an enduring amount of time, accross different instances of the browser. 

How to get info in or out of local storage 
1. getItem()
2. setItem('key-name', 'value')

We can keep track of changes to local storage programmatically by using the storage event

Your browser may or may not support addEventListener for this action. 
```if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};
```

The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer where the event object is stored in window.event.

```
function handle_storage(e) {
  if (!e) { e = window.event; }
}
```

At this point, the variable e will be a StorageEvent object, which has the following useful properties.

key -- (type) string --- the named key that was added, removed or modified

oldValue -- (type) any -- the previous value (now overwritten) or null if a new item was added

newValue -- (type) any -- the new value or null if an item was removed

url* -- (type) string -- the page which called a method that triggered this change 

* Note: the url property was originally called uri. Some browsers shipped with that property before the specification changed. For maximum compatibility, you should check whether the url property exists, and if not, check for the uri property instead.

### limitations

each origin is maxed out at 5mb of space

“QUOTA_EXCEEDED_ERR” is the exception that will get thrown if you exceed your storage quota of 5 megabytes. “No” is the answer to the next obvious question, “Can I ask the user for more storage space?”

#### here is an example of saving the state of a web game in local storage

```
function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}
```

#### and an example of resuming the game when the user returns 

```
function resumeGame() {
    if (!supportsLocalStorage()) { return false; }
    gGameInProgress = (localStorage["halma.game.in.progress"] == "true");
    if (!gGameInProgress) { return false; }
    gPieces = new Array(kNumPieces);
    for (var i = 0; i < kNumPieces; i++) {
	var row = parseInt(localStorage["halma.piece." + i + ".row"]);
	var column = parseInt(localStorage["halma.piece." + i + ".column"]);
	gPieces[i] = new Cell(row, column);
    }
    gNumPieces = kNumPieces;
    gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);
    gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";
    gMoveCount = parseInt(localStorage["halma.movecount"]);
    drawBoard();
    return true;
}
```



