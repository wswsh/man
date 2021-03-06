## basic concept 
info browse doc based on the concept of **level**, and **nodes** in the same level.
- node, a node contains text describing a specific topic at a specific level of detail.
- node header, the top line of a node.
- screen, screen  = some windows, only one active window
- window, window = view area + mode line
- 'Next', 'Prev', and 'Up' pointers which appear at the top of a node.
-cross reference, pointers which refer you to a different node, perhaps in another Info file. 

## basic commands

Cursor commands
```
ctrl-p    // prev-line
ctrl-n    // next-line
ctrl-a    // begining-of-line
ctrl-e    // end-of-line
ctrl-f    // forward-char
ctrl-b    // backward-char
alt-f
alt-b
```
Scrolling command: Moving text within a window
```
SPACE     // scrol forward
DEL       // scroll backward
```

Node commands
```
t   // goto the top node
u   // goto up level node
p   // previous node in current level
n   // next node in current level
[   // global-prev-node
]   // global-next-node
l   // history node
```

Searching commands
```
ctrl + s  // isearch-forward 
ctrl + r  // isearch-backward
} = ctrl-x n  // search-next
{ = ctrl-x N  // search-previous
```

Xref commands
```
TAB       // move-to-next-xref
Alt-Tab   // move-to-prev-xref
RET       // select-reference-this-line
```

window command
```
siwtch window：ctrl-x o
close current window：ctrl-x 0
close other window：ctrl-x 1
```

## others commands
```
Home    // go to the begining of this node
End     // to to the end of this node
ctrl-h  // get-help-window
ctrl-g    // abort-key
```
