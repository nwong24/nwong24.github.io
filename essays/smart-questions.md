---
layout: essay
type: essay
title: "What makes a good question?"
# All dates must be YYYY-MM-DD format!
date: 2026-03-31
published: true
labels:
  - StackOverflow
  - Forums
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/smartq.png">

### You get what you ask for
The difference between getting a good and a bad answer depends on how you ask. If you give a vague question such as "How do I do X?", not only will people often feel annoyed by the lack of effort on your end but will also not have enough context to properly assist you. In contrast, if you provide plenty of details and have a well structured question that indicates that you put a lot of thought behind it, it will show others that you respect their time and effort and make them more willing to answer your question with an equally detailed response.

### Asking good questions to LLMs??
This is similar to the skills required to be a successful prompt engineer. LLMs perform best when given enough context and specific instructions on what to do. Pasting in a vague question like "Implement this" leaves much room for the LLM to wander and hallucinate. Next time, keep in mind all of the requirements of a task and include as many as you can into the LLM. Putting no work into your prompts will lead to garbage output.

### What should I put in my question?
What type of details should I put in my questions though? First, you should explain your problem, what you are trying to achieve, and enough details to allow someone to reproduce your setup or problem on their own machine. For example, if you are getting a segmentation fault in a tool you are using, it might be helpful to include the minimized input you are providing, the version number, the backtrace, and the flags you were using. You should also describe what you have tried to fix the problem, which can help save the time of your helpers when debugging and also signals that you have spent effort. On the other end, don't post baseless speculation which can waste others' time; just focus on what you can observe happening. Once you have found the solution, be sure to post it for future people to use if they have the same issue.

### An example of a Smart Question
This is a StackOverflow [post](https://unix.stackexchange.com/questions/447898/why-does-a-program-with-fork-sometimes-print-its-output-multiple-times) asking about how newlines in printed strings affect the behavior after `fork()`. Here is the full post:
```
In Program 1 Hello world gets printed just once, but when I remove \n and run it (Program 2), the output gets printed 8 times. Can someone please explain me the significance of \n here and how it affects the fork()?

Program 1

#include <sys/types.h>
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("hello world...\n");
    fork();
    fork();
    fork();
}

Output 1:

hello world... 

Program 2

#include <sys/types.h>
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("hello world...");
    fork();
    fork();
    fork();
}

Output 2:

hello world... hello world...hello world...hello world...hello world...hello world...hello world...hello world...
```
