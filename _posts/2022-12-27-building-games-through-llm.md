---
layout: post
title: "Building games and apps entirely through natural language using OpenAI’s code-davinci model"
author: Andrew Mayne
date: 2022-03-17
categories: [ml/ai/nlp]
tags: large-language-model
---

[https://andrewmayneblog.wordpress.com/2022/03/17/building-games-and-apps-entirely-through-natural-language-using-openais-davinci-code-model/](https://andrewmayneblog.wordpress.com/2022/03/17/building-games-and-apps-entirely-through-natural-language-using-openais-davinci-code-model/)

> ## Lessons learned
>
> I found the new code model great at creating mini-applications and understanding how to take instructions and turn them into functions. The more things I tried, the more I learned about how to give this model instructions.
>
> **Logic first**
>
> Generally speaking, I’ve found that creating my logic elements first then my UI elements was the best approach. It’s easier to get a UI element to refer to a function that’s already in the code.
>
> **Number your instructions**
>
> If you give each instruction a number it makes it easier to see when the model is adding new instructions and to debug the code.
>
> **Create functions to make things**
>
> If you ask the model to “generate a 100 item array” it might try to return a large array which can get the model stuck repeating itself or consume a large number of tokens. However, if you tell the model to create a function to generate the array, it’ll do it in a more efficient manner with a simple for loop. When coding with the model it’s important to keep track of things you want the model to do and things you want the model to create code to do.
>
> **Retry your prompt**
>
> Sometimes there’s a bit of variability in how the model will interpret your instructions. If you set the temperature to around .5 and try it a few times you might get a better hit. When it produces a result I want, I like to see how it interpreted my instructions so I can be more explicit in the future.

> ## 1. Minimal Legend of Zelda
>
> ## 2. Five-letter word game
>
> ## 3. Matrix rain
>
> ## 4. Tic-Tac-Toe
>
> ## 5. Vampire Hunter
>
> ## 6. VR maze builder
>
> ## 7. Image manipulation tool
>
> ## 8. Painting app
