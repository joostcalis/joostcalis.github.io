---
title: Hello RSpec!
date: 2016-03-13
tags: ruby, bootcamp, codaisseur, ruby on rails, JavaScript, jQuery, React.js, API
layout: article
---

Wait what? It is week 5 already? I honestly can't believe how fast the weeks were flying by. By now as a group we had grown pretty close, and beside the fun I got from learning how to code it was just good to see everybody's faces again in the morning and catch up about how things were going. Instead of starting a new project, we continued on the work we had been doing in the weekend. All of us were individually building a review site. Front End in React and for the Back End we build another RESTful API. Still having baseball run through my veins, I chose to build a review site for all MLB ballparks.

### **Lots of ballparks**
Though I really enjoyed the teamwork it was also nice to be able to really build something completely by yourself. I made sure to have some time free in the weekend to not feel rushed while being busy. I didn't want to have a site with just a couple of ballparks, I really wanted to cover all 30. That did mean though that while creating my seeds I thought more then once: "I should really write a method for this".

### **RSpec stories**
Before even looking at the Front end I wanted to be sure to have the back end up and running. We had been introduced to test driven development and RSpec the week before, but up until now I hadn't really focused on it besides writing some random tests to see if they would pass. Part of the assignment now though was to really focus on TDD while creating the back end. For the first time I made sure to implement tests before writing the next piece of code. Whether a simple action like adding some routing, or creating connections, I wrote tests first and had guard running. It seriously didn't take long for me to see the benefits. I was writing a create method I think and apparently made a small typo somewhere that i didn't catch. When my tests kept failing it didn't take long to find the typo. Now I know this wasn't some huge event worthy of dedicating a whole paragraph to. But since 2 or 3 nights before that I had spent at least an hour rereading my code, too tired to find a similar mistake, I felt it was worth sharing.

### **RIP nutty professor**
The things with testing is, that it forces you to take small steps and keep constant confidence that whatever you're coding is working, and not breaking any other parts of your code in the same time. It only works though if you stay disciplined enough to keep writing tests before you create new functionality. All this combined basically meant that the nutty professor had to go. I was a bit reluctant to let him go at first. I kind of enjoyed the chaos of code now, ask questions later. But soon I also noticed that even with TDD he is still there, he just works a lot more efficient with some discipline.

### **React is cool**
Anyway, back to ballparks. Once the Back end was up and running, I started on the React Front end. Even if I think we just touched the tip of the iceberg with what we learned about React it was still good to see that setting it up this time went pretty fast and efficient. All the required functionality was done in no time, which gave me some time to try and get more functionality and actually style the damn thing properly this time. One of the things I got confronted with is that it's not really convenient to have 30 ballparks shown in one long list. I decided I wanted to split them up per league that their teams played in. I added a league attribute in the Back End and my first thought was to just filter my incoming array in the Front End. I found out that doing if statements in Reacts render method isn't really efficient though, and soon decided I better just already create lists per league in the Back End.

### **Let's go jobhunting!**
So yeah, 5 weeks have flown by. And while it felt a bit like an ending of something it's so cool to realize it is actually just the beginning. The jobhunting starts now. And as much as that seems like a daunting task, I mean we learned so much these weeks but I don't think its even 1 percent of what there is to learn out there, it doesn't compare to the excitement I feel about getting started and continuing to learn more about this amazing world.
