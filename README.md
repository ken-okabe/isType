isType
======

js isType



```
var isType = function(obj, type)
{
    var clas =
        Object
        .prototype
        .toString
        .call(obj)
        .slice(8, -1);
    return obj !== undefined && obj !== null && clas === type;
}

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




var mapMem = function(src)
{
    var val = [];

    if (isType(src[0], 'Array'))
    {
        val[0] = mapMem(src[0]);
    }
    else
    {
        val[0] = src[0];
    }

    for (var i = 1; i < src.length; i++)
    {
        val[i] = src[i][0](val[i - 1], src[i][1]);
    }

    return val[src.length - 1];
};

```
