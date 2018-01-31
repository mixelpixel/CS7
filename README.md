<div align="center">
  <h1>CS7 DAY by DAY</h1>
  <img src="https://raw.githubusercontent.com/mixelpixel/LambdaSchoolTA/master/art/cs7lambda.png" alt="CS7 Lambda" height="200px" width="200px">
  <br><br><br>
  <p><b>!EASTER EGGS: Click on the ▶︎ black ▶︎ triangles ▶︎ to reveal EASTER EGGS!</b></p>
</div>

# Overview
## [CS7 on Piazza](https://piazza.com/class/jc6vhnh8mdl5pw)
### [LS Syllabus Training Kit](http://ls-training-kit.netlify.com/cs-master)
##### [LS CSA Syllabus on GitHub](https://github.com/LambdaSchool/LambdaCSA-Syllabus)

<details>
  <summary>Google Calendar Week Example</summary><p>

  - The CS7 Calendar is available on Google Calendars per invite.

  ![CS& Google Calendar](art/google-calendar.png)

  </p>
</details>

<details>
  <summary>Lambda School Sprint Structure</summary><p>

  - [Lambda School Sprint Structure](https://docs.google.com/spreadsheets/d/1m83sq7Td5jpJ0XQUTwN7dJKhBHvIUppyHGIQ58pVQl4/edit?usp=sharing)

  ![Lambda School Sprint Structure](art/weeklySchedule.png)

  </p>
</details>

***

<details><summary>Month 1: January, 2018</summary><p>

<details><summary>Prior to my starting mid-Week 3</summary><p>

##### THIS LIST IS JUST AN EDUCATED GUESS RIGHT NOW

## Pre-Coursework
- https://github.com/LambdaSchool/Precourse (PR review???)
- https://github.com/LambdaSchool/Pre-Course-Git-Fu - Is this still issued to students?
***
## Week 1: Jan. 8 - 12
## JavaScript I - IV
- https://github.com/LambdaSchool/JavaScript-I-Mini
- https://github.com/LambdaSchool/JavaScript-I
- https://github.com/LambdaSchool/JavaScript-II-Mini
- https://github.com/LambdaSchool/JavaScript-II
- https://github.com/LambdaSchool/Sprint-Challenge--JavaScript
***
## Week 2: Jan. 16 - 19 (1/15: MLK Jr.)
## Data Structures
- https://github.com/LambdaSchool/Data-Structures-I
- https://github.com/LambdaSchool/LS-Data-Structures-I-Solution (PR review???)
- https://github.com/LambdaSchool/Data-Structures-II
- https://github.com/LambdaSchool/LS-Data-Structures-II-Solution (PR review???)
- https://github.com/LambdaSchool/Sprint-Challenge--Data-Structures
***
#### Code Challenges 1 through 10
1. [reverseString](https://piazza.com/class/jc6vhnh8mdl5pw?cid=10)
2. longestString
3. [reverseCase](https://piazza.com/class/jc6vhnh8mdl5pw?cid=14)
4. [reverseNumber](https://piazza.com/class/jc6vhnh8mdl5pw?cid=20)
5. [moneyFormat](https://piazza.com/class/jc6vhnh8mdl5pw?cid=24)
6. [toCamepCase](https://piazza.com/class/jc6vhnh8mdl5pw?cid=28)
7. evenOccurences
8. [romanNumerals](https://piazza.com/class/jc6vhnh8mdl5pw?cid=33)
9. [stringCompression](https://piazza.com/class/jc6vhnh8mdl5pw?cid=34)
10. collatzSequence

</p></details>

***

## Week 03: Jan. 22 - 26
## HTML/CSS and DOM Manipulation
- https://github.com/LambdaSchool/HTML-CSS-mini
- https://github.com/LambdaSchool/LS-Web-Intro-I (???)
- https://github.com/LambdaSchool/DOM-JavaScript-mini
- https://github.com/LambdaSchool/DOM-JavaScript-mini-Solution (PR review???)
- https://github.com/LambdaSchool/Sprint-Challenge-DOM-Javascript
### Day 10: Mon, Jan. 22
#### [Code Challenge 8: Roman Numerals](https://youtu.be/Q5T0Spd69uA)
***
### Day 11: Tue, Jan. 23
#### [Code Challenge 9: String Compression](https://youtu.be/5B-3pOd7b2E)
***
### Day 12: Wed, Jan. 24
#### [Code Challenge 10: Collatz Sequence](NO_VIDEO_RECORDED)
#### [Introduction to DOM and manipulation with Vanilla JS - Lecture](https://youtu.be/X8Q1yD1wjig) w/Ivan Mora
#### [Introduction to DOM and manipulation with Vanilla JS - Q&A](https://youtu.be/iuzkSVRJEss) w/Ivan Mora
***
### Day 13: Thu, Jan. 25
#### [Code Challenge 11: Consecutive Strings](https://youtu.be/Ft_nfW8GKiQ) w/Patrick Kennedy

<details><summary>Consecutive Strings Solution</summary><p>

<img src="https://raw.githubusercontent.com/mixelpixel/LambdaSchoolTA/master/art/consolelog.png" height="200px" width="200px">

- https://piazza.com/class/jc6vhnh8mdl5pw?cid=40

```js
/*
  You are given an array of strings called arr and an integer k.
  Your task is to return the longest string consisting of k consecutive
  strings from the array.

  n being the length of the string array, if n = 0 or k > n or k <= 0 return "".
 */

function longestConsecutive(arr, k) {
  // n being the length of the string array, if n = 0 or k > n or k <= 0 return "".
  // n = arr.length
  if (arr.length === 0 || arr.length < k || k <= 0) return '';

  // return the longest string consisting of k consecutive strings from the array.
  return arr
    .map((value, index) => (
      arr.slice(index, index + k).join('')
      ))
    .reduce((longest, current) => (current.length > longest.length) ? current : longest);
}

// TEST SUITE - swEEt!
// console.log(longestConsecutive([], 1), "empty string")      // <--- '' - arr.length === 0
// console.log(longestConsecutive(["one"], 2), "empty string") // <--- '' - arr.length < k
// console.log(longestConsecutive(['something'], -1), "empty string")     // <--- '' - k <= 0

// const array = ['1', '22', '333', '55555', '4444', 'xx', '666666', 'ggg', 'q', 'kk'];
// console.log(array.length);      // <--- 10
// console.log(array.slice(3, 6)); // <--- [ '55555', '4444', 'xx' ]
// console.log(array.join(''));    // <--- 122333555554444xx666666gggqkk
// console.log(array.map((value, index) => (array.slice(index, index + 2).join('')))); // <--- ugly
// console.log(array.reduce((longest, current) => current.length > longest.length ? current : longest)); // <--- six sixes


// console.log(longestConsecutive(["zone", "abigail", "theta", "form", "libe", "zas"], 2)) // <--- "abigailtheta"
// console.log(longestConsecutive(["zone", "abigail", "theta", "antidisestablishmentarianism", "form", "libe", "zas"], 3)) // <--- abi theta anti
// console.log(longestConsecutive(["zone", "abigail", "theta", "antidisestablishmentarianism", "capybara", "form", "libe", "zas"], 3)) // <--- theta anti capy

/*
 RESOURCES: google search "MDN {method name}", W3 schools, Free Code Camp
 ARRAY METHODS
 SLICE: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice
 JOIN: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join
 MAP: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
 REDUCE: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce
 ALSO GOOD: https://medium.freecodecamp.org/reduce-f47a7da511a9
 */
```

#### Truth Table: Inclusive Or
- If ANY one of the variables evaluates to `true`, then the entire proposition evaluates to `true`.
- There are three terms: `phi`, `psi` & `fry`.
- Each term has two possible states: `true` or `false`.
- The total number of _possible_ combination of three terms which each have two possible states is...?
- Number of ***states*** (either true or false) raised to the power of the number of ***terms*** (phi, psi & fry), i.e. 2<sup>3</sup>, or (2 \* 2 \* 2), a.k.a. *eight*:

| # | phi | psi | fry | "phi inclusive_or psi inclusive_or fry" |
|:---|:---:|:---:|:---:|:---:|
| 1) | T | T | T | True |
| 2) | T | T | F | True |
| 3) | T | F | T | True |
| 4) | T | F | F | True |
| 5) | F | T | T | True |
| 6) | F | T | F | True |
| 7) | F | F | T | True |
| 8) | F | F | F | False |

#### Exclusive Or (with only two terms)
- Just a quick explanation of the difference between exclusive and inclusive or logic.
- An _exclusive_ "or" operator evaluates to true when ONLY one of the terms (operands) is true.
- i.e. "I will have either a cheese burger, or pizza, but _not both_"

| Φ | Ψ | "Φ exclusive_or Ψ" |
|:---:|:---:|:---:|
| T | T | False |
| T | F | True |
| F | T | True |
| F | F | False |

</p></details>

#### [Introduction to DOM and manipulation with Vanilla JS - Q&A 2](https://youtu.be/qpI5z1DAiuY) w/Ivan Mora
#### [Introduction to DOM and manipulation with Vanilla JS - Q&A 3](https://youtu.be/7qi6vrzgyNE) w/Ivan Mora
***
### Day 14: Fri, Jan. 26
#### [Sprint Challenge](https://github.com/LambdaSchool/Sprint-Challenge-DOM-Javascript) Sprint-Challenge-DOM-Javascript
#### [Introduction to DOM and manipulation with Vanilla JS - Solution 1](VIDEO_RECORDED_NOT_POSTED) w/Ivan Mora
#### [Introduction to DOM and manipulation with Vanilla JS - Solution 2(Refactor)](https://youtu.be/LgFy3zAXK_o) w/Ivan Mora
### Sat, Jan. 27
#### [CS7 - Introduction to DOM and manipulation with Vanilla JS - Optional Review](https://youtu.be/xZfB890FWMw)


***


## Week 04: Jan. 29 - Feb. 2
## Responsive Design and CSS Pre-Processors
- https://github.com/lambdaschool/preprocessing-one

##### Prep w/ Josh Knell
- [Friday prior prep walkthrough for TAs](https://youtu.be/KikBMTsdQpc)
- https://codepen.io/bigknell/pen/zpgMbE

##### Posted in Slack Sunday prior: https://lambdaschoolstudents.slack.com/archives/C8ZM4HHD3/p1517169440000109

<details><summary>Setting up for LESS</summary><p>


> *Q: Why LESS and not SASS or another preprocessor?*

> A: Learning one will be almost identical to the other but SASS compiles on Ruby and to install Ruby for PC and MAC would have been an unwanted side effect for teaching.  You will find that the time spent in LESS will prepare you for any pre processor.

> *Q: I have node installed, but when I try to install LESS or run any commands I get an error: *

```bash
npm ERR! Error: EACCES: permission denied, access '/usr/local/lib/node_modules'
```

> A: This is because of where your files for the node modules on your computer are stored.  The quick fix is to simply run "sudo" in front of your commands to override the permission error.

> Example:

```bash
$ sudo npm install -g less
```

> This command, known as "super user do" will grant the correct permissions after you enter a password.

> For a more permanent fix, you can follow this guide on the npm website:

> https://docs.npmjs.com/getting-started/fixing-npm-permissions

> *Q: The pre course video talks about using jet brains IDE to further optimize my LESS build but I don't have that IDE.  What gives?*

> A:  Don't worry about the IDE.  That was just a helpful tip and trick.  We will be going over every detail in our guided demo.  Just get LESS installed and attempt to write a few lines of LESS so you're familiar with it.  Don't stress!

</p></details>

##### Day 1 - Preprocessors Intro
- Required: https://htmlmag.com/article/an-introduction-to-css-preprocessors-sass-less-stylus
- Documentation: http://lesscss.org/3.x/
- Install video (my version will be coming soon): https://www.youtube.com/watch?v=YQYJUeokqOY
##### Day 2 - Preprocessors Advanced
- *Read this first:* https://www.sitepoint.com/a-comprehensive-introduction-to-less-mixins/
- *After you have a decent handle on them, go try them out on your own!*
- Here are some examples to get your started:
- https://css-tricks.com/snippets/css/useful-css3-less-mixins/
- I looked for a *super short and succinct* video on LESS and this is a great review in practice:
- https://www.youtube.com/watch?v=EU1sUpPGIb4
##### Day 3 - Responsive Web Design Intro
##### Day 4 - Responsive Web Design Advanced
***
### Day 15: Mon, Jan. 29
#### [Code Challenge 12: Sum of Digits](https://youtu.be/udMpY37k7ng) w/Patrick Kennedy

<details><summary>Sum Of Digits Solutions</summary><p>

```js
/*
 * Sum Of Digits
 * Write a function called sumOfDigits that given a positive integer, returns the sum of its digits.
 * Assume all numbers will be positive.
 *
 * Input: 23  >>>function>>> Output: 5
 * Input: 496 >>>function>>> Output: 19
*/

// SOLUTION 1 - everyone loves for loops!
function sumOfDigits (num) {
  const integerStrings = ('' + num).split(''); // does the same thing as the next line
  // const integerStrings = String(num).split(''); // I find this reads better
  console.log(typeof(integerStrings)) // <--- 'object' (JA arrays are objects - Everything Is Objects!!!)

  const len = integerStrings.length;
  console.log(integerStrings);        // <--- should return an array of strings

  // declaring variables to be used in the for loop
  let i = 0,
    sum = 0;

  // For-Loop Love!
  for (i; i < len; i++) {
    sum += Number(integerStrings[i]); // <--- turns the strings into type: integers
    console.log(sum);                 // <--- sum of adding up all ints in the array of ints
  }

  return sum;
}

// SOLUTION 2 - using map() and reduce()
function sumOfDigits (num) {
  const stringIntegers = String(num).split('');
  console.log(`strInts.len: ${stringIntegers.length} & the strInts ${stringIntegers} are: ${typeof(stringIntegers[0])}`);

  const integers = stringIntegers.map(num => Number(num));
  console.log(`integers: ${integers} are: ${typeof(integers[0])}`);

  const sum = integers.reduce((sum, n) => sum + n, 0);
  return sum;
}

// CS1 MODEL SOLUTION - w/dot chaining
function sumOfDigits(num) {
  const digits = (String(num)).split('')
    .map(num => parseInt(num))
    .reduce((sum, n) => sum + n);
  return digits;
}

// MODEL SOLUTION - just return it!
function sumOfDigits(num) {
  return (String(num)).split('')
    .map(num => parseInt(num))
    .reduce((sum, n) => sum + n);
}

/* eslint no-console: 0 */
// TEST SUITE
const x = 12345;
console.log(sumOfDigits(x));           // ~~~> 15
console.log(sumOfDigits(23));          // ~~~> 5
console.log(sumOfDigits(496));         // ~~~> 19
console.log(typeof(sumOfDigits(496))); // ~~~> number
console.log(typeof(Number(x)));        // <--- number
console.log(typeof(String(x)));        // <--- string
console.log(typeof(parseInt(x)));      // <--- number
console.log(String(x).split(''));      // <--- [ '1', '2', '3', '4', '5' ]
```

</p></details>

#### [CSS Preprocessor Intro](https://youtu.be/YlYTye2UOzg) w/Josh Knell
#### [CSS Preprocessor Intro Q&A](https://youtu.be/5uffIhKvPUo) w/Josh Knell
***
### Day 16: Tue, Jan. 30
#### [Code Challenge 13: Common Elements](VIDEO_RECORDED_NOT_POSTED) w/Satish Vattikuti
#### [CSS Preprocessor 2](https://youtu.be/GwIEh4R8AUY) w/Josh Knell
#### [CSS Preprocessor 2 Q&A](https://youtu.be/shXMYNQtg48) w/Josh Knell
***
### Day 17: Wed, Jan. 31
#### [Code Challenge 14: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/Satish Vattikuti
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/Josh Knell
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/Josh Knell
***
### Day 18: Thu, Feb. 1
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/Satish Vattikuti
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/Josh Knell
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/Josh Knell
***
### Day 19: Fri, Feb. 2
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/Josh Knell
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/Josh Knell

</p></details>


***


<details><summary>Month 2: February, 2018</summary><p>

## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER

</p></details>


***


<details><summary>Month 3: March, 2018</summary><p>

## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER

</p></details>

***

<details><summary>Month 4: April, 2018</summary><p>

## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER


***


## Week ##: Mon. ## - ##
## WEEKLY_SUBJECT
- GitHub Repositories
### Day ##: Mon, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Tue, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Wed, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Thu, Mon. ##
#### [Code Challenge ##: CODE_CHALLENGE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [LECTURE](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
***
### Day ##: Fri, Mon. ##
#### [Sprint Challenge Repository on GitHub](https://github.com/LambdaSchool/NEW_SPRINT_CHALLENGE) NEW_SPRINT_CHALLENGE
#### [Brown Bag](LINK) w/SPEAKER: TOPIC
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER
#### [Sprint Challenge Review](VIDEO_RECORDED_NOT_POSTED) w/SPEAKER

</p></details>
