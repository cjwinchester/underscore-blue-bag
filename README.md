# Blue bag: underscore.js

### Sample data
```javascript
var data = [
    {
        "name": "Cody Winchester",
        "home_state": "Wyoming",
        "job": "reporter",
        "age":30
    },
    {
        "name": "Matt Wynn",
        "home_state": "Kurdistan",
        "job": "reporter",
        "age":31
    },
    {
        "name": "Graham Archer",
        "home_state": "Nebraska",
        "job": "editor",
        "age":97
    },
    {
        "name": "Emily Nohr",
        "home_state": "Nebraska",
        "job": "reporter",
        "age":24
    }
];
```

<hr>

### Return array of objects matching condition
**vanilla javascript**
```javascript
// get all records where employee is from Nebraska
var getNE = function(d) {
    var ls = [];
    for (i=0; i<data.length; i++) {
        if (data[i].home_state === "Nebraska") {
            ls.append(data[i]);
        };
    };
    return ls;
};
getNE(data);
```
**underscore**
```javascript
// get all records where employee is from Nebraska
_.where(data, {"home_state": "Nebraska"});
```