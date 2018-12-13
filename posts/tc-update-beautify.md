---
title: Refacing the Time Calculator React app
description: Implementing the react-datetime package
date_published:
  year: '2018'
  month: '10'
  day: '9'
---

 The first iteration of this project was in many respects a success. I took a project from concept to usable with about a day of coding. I was satisfied with the internals. The face on the otherhand, which I had hastily pulled together during the prototyping process, was ugly and cumbersome. It was extremely buggy in Safari, which did not support the `<input type="datetime-local">` tags I was using, and on my iPhone the app's utility was almost completely ruined by the slot machine-style native date/time picker.

 Fortunately, I had had the foresight to keep the presentational components well abstracted from the controller, a technique React makes extremely straightforward. All I had to do was decide on a new implementation and then just plug and play. This was where my research began. I at first entertained the possiblity of rebuilding the component from scratch, but after a few minutes of googling I realized that many, many other people had solved this problem already. After testing a couple of options such, I settled on the [react-datetime-picker package](https://www.npmjs.com/package/react-datetime-picker) because the [npm](http://npmjs.com) project seemed robust and strengthening, because of its relative ease of implementation and its configurability. It's implemented just as a controlled HTML `<input>` is ([reactjs.org tutorial here](https://reactjs.org/docs/forms.html#controlled-components)), where the component is passed its `value` as well as an `onChange` handler as props.
