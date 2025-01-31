---
layout: essay
type: essay
title: "I Don't Know, Can You? - Good and Bad Questions"
# All dates must be YYYY-MM-DD format!
date: 2024-1-30
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/question.png">

## What Makes a Question a Good Question?

According to Eric Raymond's essay "How to Ask Questions The Smart Way," there are many factors that make a question a good question. Before asking a question, you should try searching for answers yourself. You can do this by searching websites, books, and manuals or even by working through the material yourself. This will make it easier for you and others to pinpoint what you need help with. It's also essential to use proper grammar so that the people answering your question understand what you are asking. The most important part of asking a question, though, is pinpointing what your problem is. Leaving it vague only makes it more complicated and less appealing to people who might want to answer your question. For online questions, having clear and understandable headers also help.

## How About a Bad One?

Picture this. You're in your third-grade math class and just starting to learn about multiplication and division. You get confused about one question on the homework, and there are many questions that you want to ask. You remember the teacher mentioning that there's no such thing as a bad question, so you raise your hand. As you raise it, however, your classmate asks the teacher for help on the same question. As your teacher attempts to help them, you notice your classmate struggling to understand the teacher's explanation. They never attempted to solve the problem in the first place and were just asking for an answer so they wouldn't have to try to solve it themselves. While these types of questions are generally okay in elementary school, in the real world, bad questions do exist, and this is an example of one of them. In this example, your classmate never attempted to try the problem and, as a result, had difficulty understanding the teacher's explanation. It also made it harder for the teacher to pinpoint what part of multiplication they had trouble with. Asking bad questions makes it harder for everyone. 

## So, What Does a Good Question Look Like?

<img width="300px" class="rounded float-start pe-4" src="../img/litbulb.png">










Here is a snippet of a good question.

```
Q: Why is processing a sorted array faster than processing an unsorted array?

In this C++ code, sorting the data (before the timed region) makes the primary loop ~6x faster:

#include <algorithm>
#include <ctime>
#include <iostream>

int main()
{
    // Generate data
    const unsigned arraySize = 32768;
    int data[arraySize];

    for (unsigned c = 0; c < arraySize; ++c)
        data[c] = std::rand() % 256;

    // !!! With this, the next loop runs faster.
    std::sort(data, data + arraySize);

    // Test
    clock_t start = clock();
    long long sum = 0;
    for (unsigned i = 0; i < 100000; ++i)
    {
        for (unsigned c = 0; c < arraySize; ++c)
        {   // Primary loop.
            if (data[c] >= 128)
                sum += data[c];
        }
    }

    double elapsedTime = static_cast<double>(clock()-start) / CLOCKS_PER_SEC;

    std::cout << elapsedTime << '\n';
    std::cout << "sum = " << sum << '\n';
}
Without std::sort(data, data + arraySize);, the code runs in 11.54 seconds.
With the sorted data, the code runs in 1.93 seconds.
(Sorting itself takes more time than this one pass over the array, so it's not actually worth doing if we needed to calculate this for an unknown array.)

Initially, I thought this might be just a language or compiler anomaly, so I tried Java with a similar but less extreme result.

My first thought was that sorting brings the data into the cache, but that's silly because the array was just generated.
```
<p><a href="https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array">Link to Full Question</a></p>
The heading of this question is clear, making it easier for people to answer the question this user asked. The user also demonstrates that they have experimented and tried to understand what was wrong with their logic through coding with C++ and Java. On top of this, the user explains why he is confused by sharing his thoughts on the experiments with viewers. This makes it even easier for people to pinpoint what is wrong with this user's logic. Overall, this is a good question, and the number of replies it got speaks for itself.

## How About a Bad Question?

<img width="300px" class="rounded float-start pe-4" src="../img/brokebulb.avif">

```
I want to change date 3 7 2015 to 3Aug 2015

I have Date Value Like :

int day=3,month =7 ,year =2015

```
<p><a href="https://stackoverflow.com/questions/31780444/i-want-to-change-date-format">Link to Question</a></p>
 
This is a clear example of a bad question. While the heading does provide the user's problem, it is too vague, and it's hard for viewers to see what they are struggling with without viewing the entire problem. The grammar in this question is also very poor. While the answer to this question was a simple fix, and it got replies that answered the question, this is not a good question. This question did not need to be asked and could have been solved by looking it up on Google.

## In Conclusion...

Being able to ask good questions is essential. Asking good questions helps both parties get what they want. The person asking receives a clear answer to their problems, and the person answering understands what they are having trouble with. Before you ask a question, though, make sure that it cannot be solved by just looking it up online. Ask valuable questions, and you'll get valuable answers as a response.
