---
title: First Phaser Game
description: End product of the Phaser.js introductory tutorial, with some slight
  modifications to fit my personal taste
date_published:
  year: '2018'
  month: '10'
  day: '6'
---
 Soon after picking up JS for the first time I realized the potential it must have for game writing. Strong OOP basis and direct integration into the browser? Perfect combo. I found [Phaser](https://phaser.io) through the [MDN JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) [learning area](https://developer.mozilla.org/en-US/docs/Learn) while I was working through their excellent [Express tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs). Upon completing that project, I quickly moved on to Phaser's [introductory tutorial](https://phaser.io/tutorials/making-your-first-phaser-3-game). My satisfaction at completing this app convinced me t was time I had a somewhere to display my creations, and so this website came together from the scraps of the original MDN Express tutorial project.

 I intend to develop this project into something more of my own in the future. As it stands, it is very little modified from the original design of the tutorial. The most noticable difference is that I modified the code to prevent the player sprite from performing the running animation while in midair, and instead only facing in the direction of motion. I achieved this by adding animations with only the right- and left-facing frames of the spritesheet. I then modified the update function to check `player.body.touching.down` and chose the animation based on that.
