# Episode 1
I would expect the console to output `My name is Keith` as the function printName uses the global name variable to string this sentance together.

# Episode 2
I would expect the console to output `3` as the function returns the local varible scope which is 3

# Episode 3
I would expect the console to output the following
```bash
0: Ducks
1: Dogs
2: Lions
```
as it should loop over all elements in the local myAnimals array and print it out along with the current loop index.

# Episode 4
I would expect it to output the following
```bash
Suspects include: Jay, Val, Harvey, Rick
Suspect three is: Keith
```
As the allSuspects() function should list out all of the suspects including the local variable suspectThree and then the output of suspectThree at the end should use the global variable.

# Episode 5
I would expect the output to be `Poirot` as the detectiveInfo funciton sets the global detective name to Poirot and then passes it to a printName function which just returns the detective name and finally gets logged to the console

# Episode 6
I would expect the output to be `the murderer is rick` as the outerFunction creates a local variable called murderer and sets it to marc and then the innerFunction uses the previous local variable setting it to valerie but the final output uses the global murderer variable which should still be the original rick
 
# Episode 7
```javascript
var murderer = 'rick';
var suspects = function() {
    murderer = 'john';
    var maleSuspects = function() {
        murderer = 'iain';
        var murderer = 'sam';
        murderer = 'jordan';
    }
    var femaleSuspects = function() {
        murderer = 'sally';
        var murderer = 'hannah';
        murderer = 'emma';
    }
    femaleSuspects();
    maleSuspects();
}
suspects();
console.log('The murderer is ' + murderer);
```
[comment]: # (The murderer is actualy john but I kinda thought it would be iain)
