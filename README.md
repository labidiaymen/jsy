### Jsy make Javascript coding more fun
There is a difference between readble code and non readble, it's easly to read and memory, Jsy make your code clean and readble.

Exemple : 

Without jsy 
```javascript
var email= "labidiaymen@outlook.com"; 
var re = /^([\w-]+(?:\.[\w-]+)*)@((?:[\w-]+\.)*\w[\w-]{0,66})\.([a-z]{2,6}(?:\.[a-z]{2})?)$/i;
if(re.test(email)){
 console.log('valid email');
}

```

With jsy
 
```javascript
var email= "labidiaymen@outlook.com"; 
if(_jsy(email).isEmail()){
  console.log('valid email');
}

```

Even more :

```javascript
var email= "labidiaymen@outlook.com";   
_jsy(email).ifisEmail().log('valid email');
```
##Installation

```javascript
<script src="//cdn.jsdelivr.net/jsy/0.0.13/jsy.min.js"></script>
```

Questions ?  contact [@labidiaymen](https://twitter.com/labidiaymen)

##Documentation

Determine the internal variable class.
```javascript
.getType()
```

```javascript
//exemple : alert the type of name
var name = "aymen";
alert(_jsy(name).getType());

```

Determine the internal variable class.
```javascript
.ifType()
```
```javascript
//example : alert name if the type is equal to 'string'
var name = "jhon";
_jsy(name).ifType('string').alert();

```

check if the internal varible is  **Array**
```javascript
.isArray()
```
```javascript
//example : alert true if numbers is Array
var numbers = [1,2,3,4];
alert(_jsy(numbers).isArray());
```

check if **x** in the internal variable (**Array**)
```javascript
.inArray(x)
```
```javascript
//example : alert true if the number 3 is in the Array
var numbers = [1,2,3,4];
alert(_jsy(numbers).inArray(3));
```

return true if the internal variable is empty
```javascript
.isEmpty()
```
```javascript
//example : alert true if the variable emptyobject is empty
var emptyobject= {};
alert(_jsy(emptyobject).isEmpty());
```

run function if the internal variable is empty
```javascript
.ifisEmpty()
```
```javascript
//example : alert 'object is empty' if the variable emptyobject is empty
var emptyobject= {};
_jsy(emptyobject).ifisEmpty().alert('object is empty');
```
return true if the internal variable is float

```javascript
.isFloat()
```

```javascript
//example: alert true if x is float
var x = 9.3 ;
alert(_jsy(x).isFloat());
```
run function if the internal variable is float

```javascript
.ifisFloat()
```
```javascript
//example: log to console '9.3 is float' if x is float
var x = 9.3 ;
_jsy(x).ifisFloat().log(x+ ' is float');
```


check if **x** equal to the internal variable
```javascript
.equal(x)
```
```javascript
//example: return true if the animals varibale equal to ['puppy', 'cow', 'cat']
var animals = ['puppy', 'cow', 'cat'];
alert(_jsy(animals ).equal(['puppy', 'cow', 'cat']));
```
run function if **x** equal to the internal variable
```javascript
.ifEqual(x)
```
```javascript
//example: console to log "9 is equal to 9" if the randomumber is equal to 9
var randomumber = 9 ;
_jsy(randomumber).ifEqual(9).then(function(){
	console.log(randomumber +' is equal to 9');
});
```

return true if the internal variable has rows
```javascript
.hasRows()
```
```javascript
//example: return true if the animals varibale has rows
var animals = ['puppy', 'cow', 'cat'];
alert(_jsy(animals ).hasRows());
```
return true if the length	of the internal variable between  **min** and **max**
```javascript
.lengthBetween(min, max)
```

```javascript
//example : alert true if the length of the string between 5 and 9
var lastname = "labidi";
alert(_jsy(lastname).lengthBetween(5,9));

```

run function if the length of the internal variable between  **min** and **max**
```javascript
.ifLengthBetween(min, max)
```
```javascript
//example : alert true if the length of the string between 5 and 9
var lastname = "labidi";
_jsy(lastname).ifLengthBetween(5,9).alert("true");

```

return true if the internal variable is email
```javascript
.isEmail()
```
```javascript
//example : alert true if the variable input is an email
var input = "exemple@server.com";
alert(_jsy(input ).isEmail());
```


run function if the internal variable is an email
```javascript
.ifisEmail()
```
```javascript
//example : alert true if the variable input is an email

var input = "exemple@server.com";
_jsy(input).ifisEmail().alert("true");

```

return true if the internal variable is integer

```javascript
.isInt()
```

```javascript
//example: alert true if x is float
var x = 7 ;
alert(_jsy(x).isInt());
```
run function if the internal variable is float

```javascript
.ifisInt()
```
```javascript
//example: log to console '7 is integer' if x is integer
var x = 7;
_jsy(x).ifisInt().log(x+ ' is integer');
```

return true if the internal variable is negative

```javascript
.isNegative()
```

```javascript
//example: alert true if x is negative
var x = -3 ;
alert(_jsy(x).isNegative());
```

run function if the internal variable is negative

```javascript
.ifisNegative()
```
```javascript
//example: alert -3 if x is negative
var x = -3 ;
_jsy(x).ifisNegative().alert();
```

return true if the internal variable is negative

```javascript
.isPositive()
```

```javascript
//example: alert true if x is positive
var x = 3 ;
alert(_jsy(x).isPositive());
```

run function if the internal variable is positive

```javascript
.ifisPositive()
```
```javascript
//example: alert 8 if x is positive
var x = 8 ;
_jsy(x).ifisPositive().alert();
```

alert the internal variable or the argument if the internal condition is true or not defined
```javascript
.alert()
```

```javascript
//example: 
//alert 8
var x = 8 ;
_jsy(x).alert();
//alert equal if x is equal to 8
_jsy(x).ifEqual(8).alert('equal');
//alert 8 if x is equal to 8
_jsy(x).ifEqual(8).alert();
```

log to console the internal variable or the argument if the internal condition is true or not defined
```javascript
.log()
```

```javascript
//example: 
//log to console "jhon"
var name = "jhon" ;
_jsy(name ).log();
//log to console equal if name is equal to "jhon"
_jsy(name).ifEqual("jhon").log('equal');
//log to console "jhon" if name is equal to "jhon"
_jsy(name).ifEqual("jhon").log();
```

run function if the internal condition is true
```javascript
.then(func)
```
```javascript
//example: console to log true if the randomumber is equal to 9
var randomumber = 9 ;
_jsy(randomumber).ifEqual(9).then(function(){
	console.log(randomumber +' is equal to 9');
});
```

run function if the internal condition is true
```javascript
.else(func)
```
```javascript
//example: console to log "9 is not equal to -1" if the randomumber is not equal to nextnumber 
var randomumber = 9 ;
var nextnumber = -1 ; 
_jsy(randomumber).ifEqual(nextnumber).then(function(){
	console.log(randomumber +' is equal to '+nextnumber);
}).else(function(){
	console.log(randomumber +' is not equal to '+nextnumber);
});
```
like finally, run a function when all the treatments ended

```javascript
.end(func)
```
```javascript
//example: console to log "9 is equal to 9" if the randomumber is equal to 9, console "end"
var randomumber = 9 ;
_jsy(randomumber).ifEqual(9).then(function(){
	console.log(randomumber +' is equal to 9');
}).end(function(){
	console.log("end")
});
```
