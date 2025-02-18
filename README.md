# quiz

## Q 1
<pre>
typeof (alert)('jabbascript') // ---> ?
</pre>
<ul>
<li>- error</li>
<li>* undefined</li>
<li>- "symbol"</li>
<li>- "string"</li>
</ul>


## Q 2
<pre>
let arr = new Array(3).fill(Object(null))
arr[1].null = null
arr // ---> ?
</pre>
<ul>
<li>- [{null:null}, undefined, undefined]</li>
<li>- [{null:null}, {}, {}]</li>
<li>* [{null:null}, {null:null}, {null:null}]"</li>
<li>- [{}, {}, {}]</li>
</ul>


## Q 3
<pre>
[,1,2,].length + [,12,,].length // ---> ?
</pre>
<ul>
<li>- error</li>
<li>- 4</li>
<li>* 6</li>
<li>- 8</li>
</ul>


## Q 4
<pre>
new Array(3)[1] // ---> ?
</pre>
<ul>
<li>- error</li>
<li>* undefined</li>
<li>- 0</li>
<li>- 1</li>
</ul>


## Q 5
<pre>
'use strict'
const SomeObj = {
  me () {
    return this
  }
}
const AnotherObj = SomeObj.me
AnotherObj() // ---> ?
</pre>
<ul>
<li>- error</li>
<li>* undefined</li>
<li>- SomeObj</li>
<li>- global</li>
</ul>


## Q 6
<pre>
function UnknownId (id) {
    this.id = (id || 5)
}
UnknownId.prototype.id = 3
let unknownId_1 = new UnknownId()
let unknownId_2 = new UnknownId(4)
++unknownId_1.id
UnknownId.prototype.id = 2
unknownId_1.id // --- ?
unknownId_2.id // --- ?
</pre>
<ul>
<li>- 3 2</li>
<li>- 4 3</li>
<li>- 5 3</li>
<li>* 6 4</li>
</ul>


## Q 7
<pre>
const digitsArray = [1,2,3]
let result = ''
Array.prototype[Symbol.iterator] = () => {}
for (let nextDigit in digitsArray) {
    result += nextDigit
}
result // ---> ?
</pre>
<ul>
<li>- error</li>
<li>- 123</li>
<li>* 012</li>
<li>- 3</li>
</ul>


## Q 8
<pre>
var msg = 'hello '
function greeting () {
	if (!msg) var msg = 'world '
	alert(msg)
}
greeting() // ---> ?
alert(msg) // ---> ?
</pre>
<ul>
<li>- hello world</li>
<li>* world hello</li>
<li>- world world</li>
<li>- hello hello</li>
</ul>


## Q 9
<pre>
setTimeout(console.log, 0, 1)
setTimeout(() => Promise.resolve(2).then(console.log), 100)
Promise.resolve(3).then(console.log)
setTimeout(console.log, 100, 4)
// ---> какова последовательность вызовов ?
</pre>
<ul>
<li>- 1 4 3 2</li>
<li>- 1 3 4 2</li>
<li>* 3 1 2 4</li>
<li>- 3 1 4 2</li>
</ul>


## Q 9
<pre>
const arr = [1, 2, 3]
arr.map(arr.pop, [...arr]) // ---> ?
</pre>
<ul>
<li>- 1 4 3 2</li>
<li>- 1 3 4 2</li>
<li>* 3 1 2 4</li>
<li>- 3 1 4 2</li>
</ul>


## Q 9
<pre>
var [i, arr] = [-10, []]
while (i++) {
	((i) => {
		var i = i
		arr.push(i - i)
	})(i)
}
arr[0] // ---> ?
arr[1] // ---> ?
</pre>
<ul>
<li>- 16 16</li>
<li>* 0 0</li>
<li>- 18 16</li>
<li>- -18 -16</li>
</ul>

