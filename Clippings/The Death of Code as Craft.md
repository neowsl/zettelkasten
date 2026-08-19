---
title: The Death of Code as Craft
source: https://every.to/p/the-death-of-code-as-craft
author:
  - "[[Jon Christensen]]"
published: 2024-05-05
created: 2026-03-07
description: What is the business value in keeping developers happy?
tags:
  - clippings
---

*Are developers artists, or are they cogs? If they are artists, individual care and craft—the hallmarks of great work—are prized, and handcrafting code would be highly profitable. If coding is just a cog in the industrial machine, then the job of the software engineer is diminished. For many years,* ***Jon Christensen*** *—a software engineer himself—argued the former, but with the rise of AI, he worries that the latter is becoming true. It signals a profound shift in the economics of the tech industry and our relationship to the labor of technology company building. I found his perspective honest and refreshing. —* [*Evan Armstrong*](https://every.to/@ItsUrBoyEvan)

[Subscribe](https://every.to/subscribe)

---

I have a confession to make.

For the better part of two decades, I've been a card-carrying member of the code-as-craft cult, which espouses the belief that deeply considered, finely honed code can create better products. I used to [evangelize the ideology](https://mobycast.fm/) to anyone who would listen. I’ve waxed poetic about the sanctity of clean code. The nobility of well-architected systems. The pride of a perfect pull request.

As the founder of Kelsus, a software development services company that has built products for more than 40 startups and large companies, including Chewy, Intel, Equifax, and Splunk, I've browbeaten teammates to adopt rigorous coding standards and argued myself hoarse in conference rooms fighting for more time to hone our digital craftsmanship. I've even rage-quit projects where management failed to recognize the *value* of well-honed code.

Code as craft was my religion, my identity. And among developers, I was not alone.

But a blinding light on the horizon of technology has made me question everything I once believed. The meteoric rise of Large Language Models (LLMs) has cast a shadow over the concept of code as craft, threatening to eclipse it entirely.

In this piece, we'll embark on a journey beyond the horizon and into the land of AI-driven development. We'll explore the far-reaching implications of LLMs on the way we write, design, and think about code.

And I'll make the case for why—as painful as it is to admit—code as craft might just be a relic of a bygone era.

## Crafting a talent magnet

To truly grasp the rise of code as craft, we’ll need to understand its role in the fierce battle for programming talent.

In the early days of software, coding was considered a niche, almost clerical skill. When the first electronic computers were developed in the 1940s, the people responsible for "programming" these machines [were often women](https://www.nytimes.com/2019/02/13/magazine/women-coding-computer-programming.html), many of whom had previously worked as clerks or secretaries. Due to ingrained biases, people still believed women were better suited for repetitive tasks, despite the complex skills required for programming. These women, known as "computers" or "coders," were tasked with translating mathematical equations into machine language, a tedious and error-prone process.

Even as coding became more sophisticated in the 1950s and ’60s, with the advent of higher-level programming languages like FORTRAN and COBOL, most organizations still treated it as a secondary, support role. Programmers were there to serve the "real" stars—the hardware engineers and business analysts who were responsible for designing the physical systems and making high-level business decisions.

In 1975, in an article titled ["The Humble Programmer,"](https://www.cs.utexas.edu/~EWD/transcriptions/EWD03xx/EWD340.html) computer scientist Edsger Dijkstra lamented this perception of early programming as a second-class intellectual activity:

But most important of all, the programmer himself had a very modest view of his own work: his work derived all its significance from the existence of that wonderful machine. Because that was a unique machine, he knew only too well that his programs had only local significance, and also because it was patently obvious that this machine would have a limited lifetime, he knew that very little of his work would have a lasting value.

But things were changing. Software was finding a foothold in every industry, and programmers like Donald Knuth and Dijkstra started to push back against this "second-class" ethos. They believed that it was as much a craft as anything else, and that a disciplined, aesthetic-minded approach would lead to programs that were more efficient, reliable, and easier to maintain. Knuth famously declared that programming was an art form, stating in a [1974 article](https://paulgraham.com/knuth.html): “The chief goal of my work as educator and author is to help people learn how to write beautiful programs.”

His words were deeply influential. As the personal computer revolution unfolded into the internet boom, demand for software developers exploded. Suddenly, programmers were the rock stars of the business world, and companies were locked in an all-out war to attract and retain the best coding talent. For employers, craft became a subtle form of marketing to signal to developer talent that their company cared about code and was a good place to work.

However, the language people used to describe craft was foreign to standard boardroom dwellers. Developers mostly talked about mantras and idioms they had invented, like “continuous integration” (which is about reducing the amount of repeated effort required to release a new version of an application) and “DRY code” (short for “don’t repeat yourself,” referring to code that has very little repetition despite an application’s functionality being repeated in different places). None of this meant anything to the vast majority of CEOs.

Sometimes, the easiest way to convince the CEOs of the value of craft was just to say: The engineers say it’s good, and we need the engineers. Keep that in mind. Code as craft doesn’t always have to do with the bottom line. Sometimes, it has more to do with winning developer talent.

## The great AI divide

LLMs have sparked a fierce battle, pitting the old guard of code as craft against a new wave of AI enthusiasts.

On one side of the divide are the stalwarts of craftsmanship, like Dave,\* a veteran software architect with 20 years of work experience. When he first experimented with ChatGPT, he was alarmed by what he describes as middling code quality and unvetted code finding its way into his codebase.

“I want an engineer who has carefully considered every line and how it fits into the larger system," he explained to an online group of senior tech leaders. For Dave and others like him, LLMs are a potential threat to the stability and reliability of their software because they sacrifice the careful planning of well-crafted code. This ideology runs deep. Before LLMs, they had been training staff to avoid [Stack Overflow,](https://stackoverflow.com/) which, as an aggregator of crowd-sourced answers for programming questions, was the former best friend of junior developers worldwide. Now, LLMs are seen as just another way of developing bad habits.

On the other side are young, ambitious programmers like Abby.\* Abby sees LLMs as a liberating force. Where Dave sees risk, Abby sees opportunity. It may be that Abby is less encumbered by the past—as a newer developer, she is more open to the solutions provided by LLMs. She doesn’t mind that the code isn’t beautiful because she believes perfection is the enemy of excellence, and AI-produced code helps her learn. "It was like having a highly knowledgeable coding partner," she explains about her first time using an LLM. "It could handle a lot of the repetitive tasks, and even suggest improvements and optimizations I hadn't considered."

Abby and her compatriots believe that the automation of low-level tasks will free up developers to be more creative and focus on the big picture rather than getting bogged down in the details—or worrying about code beauty. She also points out the potential for LLMs to aid in code comprehension and maintenance—the very thing that Dave’s side worries about: "With an LLM, I can understand someone else's complex code without having to spend hours reading through it and adding breakpoints to see what it's doing…" In Abby’s world, there’s no need to care about the beauty of code. The LLMs will sort out our mess.

Who will win this war for the soul of code?

[![](https://every.to/_next/image?url=https%3A%2F%2Fd24ovhgu8s7341.cloudfront.net%2Fuploads%2Feditor%2Fposts%2F3091%2Foptimized_UXhSfkNMtcp74DrWzBX6wj9Q_F8vkbjGsz1QEz6Ich_Vy53fwUQpkCymderfE8--aCFN42v2HxBqxaHhJT5T4BKvMypSbZgS71eqaE9di6D4LmAkESvKfYwH0L-SjtTIC8hH5GQNgjW0rjVqUFTskq8.jpeg&w=1920&q=75)](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3091/optimized_UXhSfkNMtcp74DrWzBX6wj9Q_F8vkbjGsz1QEz6Ich_Vy53fwUQpkCymderfE8--aCFN42v2HxBqxaHhJT5T4BKvMypSbZgS71eqaE9di6D4LmAkESvKfYwH0L-SjtTIC8hH5GQNgjW0rjVqUFTskq8.jpeg?link=true)

*Source: DALL-E. Prompt: Pandora's box covered in runes opening into a landscape with the aurora borealis.*

## The future is bright...and weird

If the evangelists are right that AI will be able to “\[outmatch\] humans on a [range of tasks](https://www.technologyreview.com/2023/11/16/1083498/google-deepmind-what-is-artificial-general-intelligence-agi/),“ we could be on the cusp of a golden age, where the drudgery of coding is largely eliminated and developers are free to focus on higher-level problems—and, I have [argued](https://renaissance.kelsus.com/p/what-no-one-is-saying-about-what), build ever more complex systems.

If they are wrong, the world will stay largely as it is, with an ongoing [shortage](https://www.griddynamics.com/blog/software-developer-shortage-us#the-state-of-software-developer-shortage-in-the-us) of software developers unable to meet the insatiable demand for software, as venture capitalists Paul Kedrosky and Eric Norlen [have argued](https://skventures.substack.com/p/societys-technical-debt-and-softwares).

It’s more interesting to consider what will happen in a changing world. What software development practices will change under Abby’s regime?

[Subscribe](https://every.to/account)

#### Configuration over convention

First, we'll need to flip the script on the "convention over configuration" dogma that's become popular in recent years, thanks in large part to frameworks like Ruby on Rails and newer ones like the [Serverless Framework](https://www.serverless.com/).

Humans don’t like reading long lists of technical details, known as configuration files. Programmers like David Heinemeier Hansson, who wrote [The Rail Doctrine](https://rubyonrails.org/doctrine), realized that these lists were often 80–90 percent the same across programs. They decided to come up with conventions that essentially told the computer: “Do it the usual way.” For example, in Ruby on Rails, simply labeling a variable “resource” will add all the necessary pipes to be able to insert, retrieve, and update it in a database, and to do so from a web page. That’s a powerful word.

But while they are useful for human developers because we can pack a lot of “intention” into a name—such as including the word "save" in a function name to wire its result to a database without additional configuration—they’re a nightmare for LLMs. If an LLM is trying to understand a codebase, it needs to reason about the behavior and purpose of every component. If those components' behaviors are implied by their names, rather than explicit configurations, the LLM has to carry around a huge amount of context about naming conventions. And if those names change, the LLM's understanding could be completely broken.

In an LLM-driven world, explicit is better than implicit. We should strive to make our code as self-describing as possible so that an LLM can understand what the code will do by “reading” it rather than having to “mentally simulate” running it (if those are the right words for what LLMs do!). It should be more akin to an illustrated instruction manual than a rule book.

#### Language selection (training)

We'll also need to be strategic about the languages and ecosystems we choose to work in. LLMs are only as good as the data they're trained on, so it makes sense to develop with languages that have a wealth of publicly available code examples.

Based on [GitHub's language stats](https://github.blog/2023-11-08-the-state-of-open-source-and-ai/), widely used languages like JavaScript and Python are likely to have a significant advantage over more niche languages like Go or Kotlin. The more examples an LLM has to learn from, the better it will be at understanding and generating code in that language.

#### Language selection (static versus dynamic)

That said, not all popular languages are created equal in terms of LLM-friendliness. Heavily dynamic languages like Ruby, Python, and Javascript—in which a lot of the behavior isn’t determined until the program runs—are likely to present challenges.

In contrast, programming languages that have strict rules about the types of data they can work with and catch potential errors before the code is run—such as TypeScript (a variant of JavaScript with added type checks), Kotlin, Rust, and Go—will be much easier for LLMs to understand and work with. The more clearly defined and predictable the code's behavior is, the easier it will be for an LLM to generate code that matches the developer's intent.

#### Contextualizing the entire developer experience

Perhaps the most exciting possibilities lie in the ways we can actively design our tools to be more LLM-friendly.

Let’s start with a cooking analogy to explain. Imagine a chef with an idea for a new dish. When they describe it, you can almost taste the food. That's what developers do when they set out to create a new piece of software. They have this idea—this intent—of what they want to build and how it should work.

Now, to make that vision a reality, developers need to write code. Code is like the ingredients and instructions in a recipe. But just like a dish can go wrong with the wrong ingredients or if you cook it for too long, code can have bugs and errors that prevent it from working as intended.

Software tests help ensure accuracy. They're like the taste tests you do while cooking. You take a little bit of your code and check to make sure it works the way you expect it to. If something tastes off, you know you need to make some adjustments. It's the same with code—if a test fails, developers roll up their sleeves and debug.

Finally, once the code is written and tested, developers run it to see the final result. It's like serving up that finished dish to your eager guests. The runtime output is the moment of truth where developers see whether they’ve created something that works as intended.

Developers currently copy-paste code from their code window to the GPT window to tell GPT about their intent, code, tests, and runtime output. They ask questions based on parts of those four things. It’s inefficient and error-prone, especially because GPT doesn’t keep track of everything at once, it only knows as much from your development efforts and running code as you have pasted into your conversation.

Imagine an integrated development environment (IDE) that keeps four layers of context: developer intent, code, tests, and runtime output. If it could, it would be much more useful. Already, companies like [Cursor](http://cursor.sh/), Cognition (which created AI software engineering assistant [Devin](https://www.cognition-labs.com/introducing-devin)[)](https://www.cognition-labs.com/blog), and [GitHub Copilot Workspace](https://every.to/chain-of-thought/i-spent-24-hours-with-github-copilot-workspaces) are trying to solve this problem.

[![](https://every.to/_next/image?url=https%3A%2F%2Fd24ovhgu8s7341.cloudfront.net%2Fuploads%2Feditor%2Fposts%2F3091%2Foptimized_EK-AauZKNWJYlUooNhQsLSJERySfn7N5P4dvkcTOGaD3WcIrFP5bk6pUHbbu2jN5pDOAefmkQUC-_1DE18Gpx-IxGSjp2iX20slEA-fzESd2nSeFEyJt2bS9_SzNS7JzIOCOToAl8GqXvkENfdq4g2g.jpeg&w=1920&q=75)](https://d24ovhgu8s7341.cloudfront.net/uploads/editor/posts/3091/optimized_EK-AauZKNWJYlUooNhQsLSJERySfn7N5P4dvkcTOGaD3WcIrFP5bk6pUHbbu2jN5pDOAefmkQUC-_1DE18Gpx-IxGSjp2iX20slEA-fzESd2nSeFEyJt2bS9_SzNS7JzIOCOToAl8GqXvkENfdq4g2g.jpeg?link=true)

*Source: DALL-E. Prompt: A leather apron-wearing, beard-wielding, craft-loving software engineer in a Craftsman house.*

#### Return to monoliths

More radically, the rise of LLMs could lead to a resurgence of monolithic architectures. In monolithic architectures, code is packaged together and compiled into a single executable program—kind of like an iPhone where you can’t swap the battery, screen, or antenna without rebuilding the whole thing. These types of architectures for big systems have lost favor to microservices, which are small applications that typically have singular purposes—like updating a user’s profile in a database. Microservices allow large teams to work on isolated features independently without stepping on each other's toes.

But microservices come with a significant cost: complexity. Managing the interactions, dependencies, and side effects among scores of microservices is a Herculean task, one that often requires dedicated teams and sophisticated tooling. And it will become more difficult for an LLM to reason about the behavior of the system as a whole as the number of services grows.

Enter LLMs. The larger its context window, the more code an LLM can understand and reason about at once. In a world where LLMs are a primary tool for code generation and modification, the benefits of microservices start to look less compelling.

Why split your system into 100 microservices when an LLM can understand and modify a monolith just as easily? With LLMs automating much of the code writing, the need for separate teams working on separate services diminishes.

Instead, we might see a return to what we could call "mesoservices"—not quite the hulking monoliths of old, but larger and more integrated than the microservices of today. These mesoservices would be large enough to encapsulate significant business functionality, but small enough for an LLM to fully grasp and manipulate.

It's a vision of a future where the structure of our systems is determined not by the limitations of human developers, but by the capabilities of our AI tools. A future where the age-old trade-offs between complexity and modularity, between coupling and cohesion, are fundamentally rewritten by the power of LLMs.

Of course, this is all speculation. The reality is that we're in uncharted territory, and the path forward is anything but clear. But one thing seems certain: The rise of LLMs will force us to reconsider many of our long-held assumptions about programming and how it should be done.

The developers and organizations that are able to adapt, to embrace the power of AI while also understanding its limitations, will be the ones that thrive in this *Hunger Games* of software. It won't be easy, and there will undoubtedly be missteps and setbacks along the way. But the potential rewards—a world in which software development is more accessible, more efficient, and more focused on high-level problem solving—are too great to ignore.

## Reconnecting craft and business value

We’ve spent long enough with CEOs unable to understand the terminology of software engineers and why the things they care about matter. LLMs are likely to be both a revolution and an evolution for the world of software development. They will fundamentally change many of our day-to-day practices and assumptions.

If an LLM can understand and maintain a function with 50 nested “if” statements as easily as it can understand a clean, well-factored one, and they both functionally do the same thing, does one have greater business value than the other? If an LLM can generate a new feature from a simple description faster than we can write the code ourselves, does it still make sense to obsess over clean, minimal code?

LLMs will force us to rethink what we value in code and in developers. The craft of software development, as we've traditionally understood it, may become less about the minutiae of code structure and more about the high-level design of systems and architectures.

On the other hand, many of the fundamental truths about software development are likely to remain unchanged. The skills that truly great developers bring to the table— [creativity, problem-solving, systems thinking](https://every.to/chain-of-thought/you-re-a-developer-now) —will be more valuable than ever in a world where the [low-level details of coding](https://every.to/napkin-math/automate-the-simple-with-stupid) are largely automated.

In this world, the value of these top developers won't just be high—it will be stratospheric. Companies will compete fiercely for their attention and services. The gap between the best developers and the rest will widen, and the impact of these star performers will be felt across the industry.

Organizations that value and nurture this kind of craftsmanship, just like before, will have a significant advantage in the war for talent. And in an industry where the quality of your human capital is often the difference between success and failure, that's an advantage that can't be overstated.

Code as craft is dead. Long live code as craft.

---

*\*Names have been changed.*

***Jon Christensen*** *is the founder of Kelsus, a startup-focused development company that has helped launch more than 40 startups. Previously, he cut his teeth at Denver-based startups like Boldtech, StorePerform, and IP Commerce. He graduated from Amherst College with a degree in computer science.*

*To read more essays like this, subscribe to* [*Every*](https://every.to/subscribe)*, and follow us on X at* [*@every*](http://twitter.com/every) *and on* [*LinkedIn*](https://www.linkedin.com/company/everyinc/)*.*

[Subscribe](https://every.to/subscribe)