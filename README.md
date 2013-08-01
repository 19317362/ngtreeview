# Description

Pure [angularjs](http://www.angularjs.org) based tree menu directive.


# Installation

Copy the script into your project and add a script tag to your page.

```html
<script src="/angular.treeview.js"></script>
```

Add a dependency to your application module.

```javascript
angular.module('myApp', ['angularTreeview']);
```

Add a tree to your application. See [Usage](#usage).

# Usage

Attributes of angular treeview are below.

- angular-treeview: the treeview directive
- tree-model : the tree model on $scope.
- node-id : each node's id
- node-label : each node's label
- node-children: each node's children

Here is a simple example.


```html
<div
    data-angular-treeview="true"
    data-tree-model="treedata"
    data-node-id="id"
    data-node-label="label"
    data-node-children="children" >
</div>
```

Example model:

```javascript
$scope.treedata = 
[
    { "label" : "User", "id" : "role1", "children" : [
        { "label" : "subUser1", "id" : "role11", "children" : [] },
        { "label" : "subUser2", "id" : "role12", "children" : [
            { "label" : "subUser2-1", "id" : "role121", "children" : [
                { "label" : "subUser2-1-1", "id" : "role1211", "children" : [] },
                { "label" : "subUser2-1-2", "id" : "role1212", "children" : [] }
            ]}
        ]}
    ]},
    { "label" : "Admin", "id" : "role2", "children" : [] },
    { "label" : "Guest", "id" : "role3", "children" : [] }
];     
```

