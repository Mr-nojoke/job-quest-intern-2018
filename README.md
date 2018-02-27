### TakeMeTour Internship Program 2018

Hi all applicants! Welcome to TakeMeTour Internship Program 2018. Being and intern at TakeMeTour is challenging so we have challenges for you! These challenges are designed to assess your learning skill, which is the fundamental and most important skill of great software developer. So I do not expect you to have full or any knowledge about the topic beforehand but it's your job to try to learn and answer those challenges.

## Algorithm in Javascript
Code must be writted in Javascript language. The code will be tested with Node8, so you can use all Javascript features that equivalent to Node8.

1. Write a function that shift the elements of array to left or right by n elements in infinity loop. the function recevice 3 parameters, 1st is an array, 2nd the is direction ('left' or 'right'), 3rd is the number of elements will be shifted. For example,
```
> shift(['john', 'jane', 'sarah', 'alex'], 'left', 2)
['sarah', 'alex', 'john', 'jane']

> shift([1, 2, 3, 4 ,5], 'right', 3)
[3, 4, 5, 1, 2]
```
Answer:
```javascript
function shift(arr,direction,number){
    for(i=0;i<number;i++){
        if(direction==='left'){arr.push(arr.shift());}
        if(direction==='right'){arr.unshift(arr.pop());}
    }
    return console.log(arr);
}
```
2. Download [hero.json](https://github.com/takemetour/job-quest-intern-2018/blob/master/hero.json) and write a code to caculate these values from **hero.json**
- 2.1 Average **networth** of all heroes
- 2.2 Average **level** for hero that has 'intelligent' as **primary_attribute**
- 2.3 Find the hero who got the most **assist**
- 2.4 Find the hero who got the worst **kill/death ratio** (ratio = kill/death)

Answer:
```javascript
const hero  = require('./hero.json')
const averageNetworth = (arr) => {
    let totalnetworth = arr.reduce((total,hero)=>total+hero.networth,0);
    let aveNet = totalnetworth / arr.length;
    return aveNet
}
const averageIntLevel = function(arr){
    let intHero = arr.filter(hero=>hero.primary_attribute==='intelligent');
    let averageIntHeroLevel = intHero.reduce((total, hero)=>total+hero.level,0)/intHero.length;
    return averageIntHeroLevel
}
const mostAssist = (arr) => {
    let most = arr.reduce((a,b)=>a.assist>b.assist?a:b);
    return most.name + ' Assist ' + most.assist
}
const worstKDR = (arr) => {
    let worst = hero.reduce((a,b)=>a.kill/a.death<b.kill/b.death?a:b);
    return worst.name + ' K/D ' +worst.kill/worst.death;
}
console.log('Average Networth of all hero = '+averageNetworth(hero));
console.log('Average Lever of Intellegent hero = '+averageIntLevel(hero));
console.log('Most Hero Assist = '+mostAssist(hero));
console.log('Worst Hero K/D = '+worstKDR(hero));
```

## Simple Web Application: A joke from Chuck Norris.

This part of quest will be a challenging one. You are going to make a simple web application which allow users to get some joke from **Chuck Norris** himself.

> Chuck Norris once ordered a Big Mac at Burger King, and got one.

### Features
- Users can get a joke from [Chuck Norris API](http://www.icndb.com/api/)
- Users has options to change number of result jokes, user's first name and last name
- UI Design as you wish.

### Technical description
- Using data from [REST API](http://www.icndb.com/api/)
- Any tools & framework is allowed.
- If you are using tools & framework which is same as our tech stack (React, Redux, styled-components, recompose etc.) will be a plus.
- Any extra feature will be a plus.

here is the [app](https://blog-793b9.firebaseapp.com/)

## Questions
Q1: What is GraphQL and how it is different from REST API?

A1: GraphQL is a query language that have type witch is greatly improve the readability of query and respond is just what you ask REST API is an architectural style for distributed hypermedia systems 


Q2: Please explain how javascript benefits from cross-platform development

A2: various amount of tools dose not guarantee the quality of the project write one javascript application and run it on several platforms can reduce a lot of code and bug

Q3: What do you expect to get from during an internship at TakeMeTour?

A3: i want to learn much much more and it's hard to do alone so during an internship i expect an experience and advice from TakeMeTour. 

## Submitting

Please fork this repo and submit your repository at jet@takemetour.com along with your contact information.

Note: These challenges must be done by yourself. There is no benefit for both sides if the answer do not reflect your true skill.
