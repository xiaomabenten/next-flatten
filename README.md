# next-flatten
> Flattens `array` a single or multiple level deep.


## usage:
```js
var rs = nx.flatten([[1, 2, 3], [4, 5]]); 
// [1, 2, 3, 4, 5]
```


## resources:
+ https://stackoverflow.com/questions/10865025/merge-flatten-an-array-of-arrays-in-javascript


## other solution:
```js
function flattenArrayOfArrays(a, r){
    if(!r){ r = []}
    for(var i=0; i<a.length; i++){
        if(a[i].constructor == Array){
            r.concat(flattenArrayOfArrays(a[i], r));
        }else{
            r.push(a[i]);
        }
    }
    return r;
}
```
