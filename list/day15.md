# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/04 / Week 3

![image](/images/14.png)

Today, we'll start a new team and learn some basic Javascript to gain a better understanding of React.

![image](/images/15.png)

Following that, we build a team task and decide what we will accomplish next; first, we develop a wireframe of the topic we have chosen, and then we start with creating a work timetable.

- What did I learn today?

Understanding functions in games is a good example; being easy to understand and read is also one of the things to consider in programming, as shown below.

```js
function Hero(name, skills, role) {
    this.name = name;
    this.skills = skills;
    this.role = role;

    this.blood = 100;
    this.mana = 1000;
    this.level = 1;
}
Hero.prototype.attack = function(opponent, power) {
    this.mana = this.mana - power;
    opponent.blood = opponent.blood - power;

    console.log(this.name + ' is attacking ' + opponent.name + ', mana = ' + this.mana);
    console.log(opponent.name + '\'s blood is ' + opponent.blood);
};
Hero.prototype.printProfile = function() {
    console.log('Name: ' + this.name);
    console.log('Skills: ' + this.skills.join(', '));
    console.log('Role: ' + this.role);
    console.log('Blood: ' + this.blood);
    console.log('Mana: ' + this.mana);
    console.log('Level: ' + this.level);
};

const hayabusa = new Hero('Hayabusa', ['Skill 1', 'Skill 2', 'Skill 3'], 'Knight');
const miya = new Hero('Miya', ['Skill 1', 'Skill 2'], 'Tank');
const gatotKaca = new Hero('Gatot Kaca', ['Skill 1', 'Skill 2', 'Skill 3', 'Skill 4'], 'Tank');
```

- What did I do well?

It's a good idea to make a function that can be reused and is easy to read.

- What needs to improve?

Make an excellent function.
