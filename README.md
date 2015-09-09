# container-avltree
AvlTree implementation in Javascript

To manage a pool of sorted elements. **Complexity in O(log2(n)) for addition and removal**.

To **instantiate** a new tree:
``` javascript
// In this example, myTree will hold elements sorted by zIndex
function myComparisonFunction(a, b) {
	return a.zIndex - b.zIndex;
}

var myTree = new AvlTree(myComparisonFunction);
```

To **add** an element:
``` javascript
var myObjectReference = myTree.add(myObject); // O(log2(n))
```

To **remove** an element:
``` javascript
myTree.removeByReference(myObjectReference); // O(log2(n))
```

To **apply a treatment** on all the elements in sorted ordered:
``` javascript
myTree.forEach(function (object) {
	console.log(object);
});
```

To **apply a treatment** on all the elements in opposite sorted ordered:
``` javascript
myTree.forEachReverse(function (object) {
	console.log(object);
});
```

To **get the smallest element greater or equal to a given object**:
``` javascript
var myObjectAbove = myTree.getSmallestAbove({ zIndex: 4 }); // O(log2(n))
```

To **get the greatest element smaller or equal to a given object**:
``` javascript
var myObjectBelow = myTree.getGreatestBelow({ zIndex: 4 }); // O(log2(n))
```

To **convert into an array**:
``` javascript
var myArray = myTree.toArray(); // O(n)
```

To **get the number of elements in the tree**:
``` javascript
var nbElements = myTree.length;
```