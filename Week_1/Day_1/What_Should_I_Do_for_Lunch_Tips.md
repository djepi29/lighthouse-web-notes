### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in Vagrant.

Work on your code iteratively – that means in small pieces. 

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.

```javascript
const whatToDoForLunch = function(hungry, availableTime) {
  let decision = "";
  if (hungry === false) {
    decision = "I can make good use of the time and start the next assignment!";
  } else {
    if (availableTime < 20) {
      decision = "Grab an apple and keep going!";
    } else if (availableTime <= 30 && availableTime >= 20) {
      decision = "I've earned myself a cooked meal, It's time for a break!";
    } else if (availableTime > 30) {
      decision = "calm down stomach, I fed you yesterday! Let's finish the assignment, then I'll get you food!";
    }
  }
  console.log(decision);
};

console.log("I'm hungry and I have 20 minutes for lunch.");
whatToDoForLunch(true, 20);
console.log("---");

console.log("I'm hungry and I have 50 minutes for lunch.");
whatToDoForLunch(true, 50);
console.log("---");

console.log("I'm not hungry and I have 30 minutes for lunch.");
whatToDoForLunch(false, 30);
console.log("---");

console.log("I'm hungry and I have 15 minutes for lunch.");
whatToDoForLunch(true, 15);
```