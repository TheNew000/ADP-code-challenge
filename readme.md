#####Created Post Time Limit for cleanliness and quickness

###Problem:
Using Javascript, given an array of n integers (example: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 100, 112, 113]), remove all odd numbers, leaving only the even numbers.

###Solution:

```javascript
function onlyEven(array){
    if (Array.isArray(array)) {
        var arr = [];
        function checkEvens(array){
            if (array.length > 0){
                var curr = array.shift();
                if (curr % 2 === 0) arr.push(curr);
                checkEvens(array);
            } else {
                return arr;
            }
        };
        checkEvens(array);
        return arr;
    }else{
        return console.log(array + " is not an array!");
    }
};
```
