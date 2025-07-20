# Reflection – Daily Schedule Simulator

## What was your approach to designing the schedule?

These were essential activites I do everyday. They are personal because I need them in order to have a 'good' day.

## What was one challenge or unexpected behavior you encountered?

Originally I had a setInterval and setTimeout function nested within one another, setTimeout was a callback func inside setInterval. This proved incompatible because of the asynchronous code. I then had to separate these two and invoke them individually. That way their delays would not affect one another.

I also changed the background color of an html based on the minutes of the day. I had to debug my conditional statements that set the element color, because I believe the CSS top to bottom hierachy rule was applying to my javascript code as well.

if (minCounter > maxMin / 2) output.style.backgroundColor = 'yellow';
if (minCounter >= maxMin) {
// turn off timer after 6 hours
output.style.backgroundColor = 'pink';
output.textContent = 'The day is done - get some rest cutie :)';

Here I originally had line 16-17 above 13 but the color would not reset. When I change the order of these assignments it behaved as expected. To avoid this in the future I would write my code in a js file not in a script file - hopefully that would fix this.

## What does this assignment teach you about async code?

The thread of operation does not run straight from top to bottom in order. The delays or timers cause the code to sit in queue while waiting for the correct time to run while the TOE continues down to run sync code.

## What creative element did you add?

I changed the styling of the output element based on my min counter. This is meant to signal times benchmarks of the day.

## How does this project simulate or differ from real-world schedules?

It works somewhat similarily to real-world time. It starts when the program is run so not until I begin my day. Additionally it has a set time alloted for each of the tasks, the problem with this is that the code is rigid and does not accomodate unexpected hiccups or delays.
