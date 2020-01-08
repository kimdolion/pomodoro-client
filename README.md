# FreeCodeCamp's Front End Libraries Project: Pomodoro
[Pomodoro](https://en.wikipedia.org/wiki/Pomodoro_Technique) is a time management mindset where folks use a timer to help break up an activity into smaller tasks.

![Pomodoro Langing Page](public/BobaLanding.png)

[Front-end Client](https://kimdolion.github.io/pomodoro-client/#/)

[Front-end Repo](https://github.com/kimdolion/pomodoro-client)

[Back-end Client](https://limitless-everglades-63033.herokuapp.com/)

[Back-end Repo](https://github.com/kimdolion/boba-tracker-backend)

## Technologies Used
React, React Boostrap, Axios, MongoDB, Express, HTML, CSS, JS

## Setup and Installation
##### Setup and intialize to local/remote and Git Pages
Install dependencies and work with locally with Grunt
-Use `npm` to install dependencies
  -Installed additional dependency React-color to test color pickers
-Use `npm run deploy` to deploy to Git Pages

**User** has many **Timers**

  <table style="display:inline">
  <th colspan="2" style="text-align:center">Timers</th>
  <th colspan="2" style="text-align:center">User</th>
  <tr>
  <td>_id</td>
  <td>MongoDB generated</td>
  <td>_id</td>
  <td>MongoDB generated</td>
  </tr>
  <tr>
  <td>flavor</td>
  <td>string</td>
  <td>email</td>
  <td>string</td>
  </tr>
  <tr>
  <td>datePurchased</td>
  <td>date</td>
  <td>hashedPassword</td>
  <td>string</td>
  </tr>
  <tr>
  <td>location</td>
  <td>string</td>
  <td>token</td>
  <td>string</td>
  </tr>
  <tr>
  <td>cost</td>
  <td>number</td>
  <td>timestamps</td>
  <td>datetime</td>
  </tr>
  <tr>
  <td>color</td>
  <td>string</td>
  <td></td>
  <td></td>
  </tr>
  <tr>
  <td>owner</td>
  <td>ref to user</td>
  <td></td>
  <td></td>
  </tr>
  </table>


  #### Timer actions currently supported:
  -Create timers
  -(Read) See
    -All timers
    -All timers by owner
    -Show timer by id
  -Edit your timers
  -Delete your timers

##### End Point Testing

<ul style="list-style-type:none;">
  <li>get -> #index, #show</li>
  <li>post -> #create</li>
  <li>patch -> #update</li>
  <li>delete -> #destroy</li>
</ul>

## Resource Routes
`user routes`:
  -`/sign-up` - POST for sign up credentials
  -`/sign-in` - POST for sign in credentials
  -`/users` - GET for list of users
  -`/change-password` - PATCH for updating credentials
  -`/sign-out` - DELETE for sign out

`timers routes`:
  -`/timers` - GET for index of timers
  -`/timers/:id` - GET for individual timers
  -`/timers` - POST for timers creation (applies ownership)
  -`/timers/:id` - PATCH for editting timers (requires ownership)
  -`/timers/:id` - DELETE for deleting timers (requires ownership)

## Development Process

## Problem Solving
###
TBD

## Unsolved Problems
TBD

## FreeCodeCamp User Stories
<details>
<summary>User Stories</summary>
<li>User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").</li>

<li>User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").</li>

<li>User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".</li>

<li>User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".</li>

<li>User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.</li>

<li>User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.</li>

<li>User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").</li>

<li>User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).</li>

<li>User Story #9: I can see a clickable element with a corresponding id="start_stop".</li>

<li>User Story #10: I can see a clickable element with a corresponding id="reset".</li>

<li>User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.</li>

<li>User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.</li>

<li>User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.</li>

<li>User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.</li>

<li>User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.</li>

<li>User Story #16: I should not be able to set a session or break length to <= 0.</li>

<li>User Story #17: I should not be able to set a session or break length to > 60.</li>

<li>User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.</li>

<li>User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).</li>

<li>User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.</li>

<li>User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.</li>

<li>User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.</li>

<li>User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.</li>

<li>User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.</li>

<li>User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.</li>

<li>User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".</li>

<li>User Story #27: The audio element with id="beep" must be 1 second or longer.</li>

<li>User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.</li>
</details>

## Stretch Goals

## Additional Resources
