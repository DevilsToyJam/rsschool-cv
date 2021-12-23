# Dranov Alexander
## Contacts 
* Location: Russia, Chelyabinsk
* Phone: +7 900 025-36-23
* E-mail: moze9lol@gmail.com

## About Me
I'm 28 years old. Currently working on freelance as Quality Assurance in Translating Agencies. Learning what is Front-end development. 
Strong soft skills: Communication, Focus, Teamwork, Time management, Public speaking.
## Skills 
* HTML
* CSS (Bootstrap, Tailwind, SASS, BEM)
* JavaScript (Fundamentals, ES6+, DOM, JSON, Asynchronous JavaScript)
* Git/GitHub
* Figma, Photoshop

## Experience
...
## Education
Institue: Russian-British Institute of Management. Bachelor in Business Informatics.
## Code Example
### [645. Set mismatch](https://leetcode.com/problems/set-mismatch/)
You have a set of integers `s`, which originally contains all the numbers from `1` to `n`. Unfortunately, due to some error, one of the numbers in s got duplicated to another number in the set, which results in **repetition of one** number and **loss of another** number.
You are given an integer array `nums` representing the data status of this set after the error.
Find the number that occurs twice and the number that is missing and return *them in the form of an array*.
```javascript
const findErrorNums = function (nums) {
    let sumFormula = nums.length * (nums.length + 1) / 2
    let obj = {};
    let answer = [];
    for (let i = 0; i < nums.length; i++) {
        sumFormula -= nums[i];
        obj[nums[i]] = obj[nums[i]] + 1 || 1;
        if (obj[nums[i]] == 2) {
            answer.push(nums[i]);
        }
    }
    answer.push(answer[0] + sumFormula);
    return answer;
};
```