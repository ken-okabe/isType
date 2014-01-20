isType
======

js isType



```
var is = function(obj, type)
{
    var clas =
        Object
        .prototype
        .toString
        .call(obj)
        .slice(8, -1);
    return obj !== undefined && obj !== null && clas === type;
}


```
type:''

String
Number
Boolean
Date
Error
Array
Function
RegExp
Object
