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

As we can see, he explains what he has tried (removing the newline), and provides the minimal C program we can compile to reproduce his observed behavior. In return, he receives a well written response explaining to him the buffering system of glibc and how the 8 resulting processes still have the string in their buffer and all flush it at once when each process exits.

### An example of a Not So Smart Question
In this SO [post](https://meta.stackoverflow.com/questions/359447/may-i-ask-for-tips), this user is asking for generic tips for their JavaScript code. Here is the post below:
```
I have a piece of JavaScript code I want to ask advice on. I want to know if I may post a question on the main site, asking for tips on a piece of code I have written. I don't want the answer, just tips. May I do this?

I wrote the code myself, but I am unable to proceed. I would just like some advice on how to proceed - like "use a function" or whatever. Or is there a beginner's site to ask questions?
```

First of all, there is no effort put into the question. The user states that they want advice on the Javascript code but doesn't post it. This makes it impossible for others to know what this user has tried before and where to direct them towards. In addition, if this user just wanted advice for beginners, there are plenty of websites on the internet that can provide such information. This shows that they didn't even attempt to improve on their own or do any research and just went straight to the forum. Rightfully so, this user received -10 points and a set of negative comments from other users, telling them that they should be using the site to ask specific questions and not look for vague advice.

### What I learned
To get good answers, you must put the work to make a good question first. A good answer consists of detailed information about your environment and your problem. It also doesn't include redundant information that will waste contributers' time. You should post your question on a relevant forum as well, or today maybe even ask an LLM and double check its answer. With these steps, you will be sure to get good responses from other users.
