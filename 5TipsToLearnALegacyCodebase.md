**5 Tips To Learning A Legacy Codebase**

YOU ARE IN A LEGACY CODEBASE

```
> RUN TESTS
YOU HAVE NO TESTS

> READ SPEC
YOU HAVE NO SPEC

> WRITE FIX
YOU ARE EATEN BY AN ELDER CODE HACK.

-@brianwisti
```

So you’ve got your first programming job out of coding bootcamp. Congratulations! You’ve likely got a solid grasp of Rails, MVC, Object Oriented Programming, and SQL, and have completed your final project in the not-so-distant past. You officially know how to build a web app from the ground up. However, when you get into the office on your first day and take a look at your new company’s codebase (realistically maybe not quite your first day, depending on how daunting environment set-up is at your new workplace), chances are it won’t look as familiar as you’d hope. 

First off, it will likely be far, far larger than anything you’ve had to contend with in the past. It will also likely be more disorganized, even if you’re working in an opinionated framework like Rails. The organization also might be very different than what you’re used to; the codebase may actually consist of a series of separate small apps that all need to communicate with each other, or (if you’re out of Rails) may not be MVC at all.

Fortunately, there’s no reason to panic. Every old, large codebase is full of unique quirks and odd design choices, and it takes even seasoned developers some time to figure out what everything does and why. Ideally, your employers will have a ramp-up plan for you which includes small tickets that will help familiarize you with the app without being overwhelming. Even so, there are few things you can do early on that will help you enormously on your way:

Ask if there are high level diagrams or explanations of your app’s architecture and database structure available. Most companies have a wiki, documentation, or internal stackoverflow-like site that’s used as a repository for institutional memory, and sometimes you’ll find this kind of information there. Or possibly your ramp-up will include a talk on this already. If nothing like this exists, however, ask if a senior dev has time to give you a walk-through. Take copious notes during the explanation, and for extra bonus points, offer to write it up and make it available for future new devs’ reference. 

Read up on the design patterns your company uses. Try implementing them on a new project of your own, so you’ll understand how they work from the ground up. If your app uses more than one language or framework (for example Ember or Angular on the front-end), read up on the ones you’re unfamiliar with too, even if working with them is not a part of your daily responsibilities. It will still help you understand the context that you’re working in, or deal with arcane future bugs.

Look at the test suite. Most likely, your company’s app has some amount of test coverage. If you’re lucky, the tests will also be somewhat discursively written. If you aren’t sure what the purpose of a function or file is, reading through the associated tests should help clarify the intent behind it as well as what it actually does. 

Step through it! How best to do this will vary by stack, editor, and/or IDE, but in most circumstances some tool like pry for Ruby or the Visual Studio debugger will allow you to go through all methods called in a function line by line and to see what variables and values are present at each stage as that function executes. It’s an important tool for debugging code of course, but it’s also a good way to dive into the nitty-gritty of a section of code that you don’t understand.

When in doubt, ask why. If you don’t understand why a design choice was made, or why one method of doing something is better than another, ask! It’s better to ask a lot of questions up front, while you’re still new and junior, than it is to avoid it and have to ask them later. It’s also often a good practice, after receiving a particularly complicated explanation, to immediately rephrase it according to your own understanding and ask if that’s correct. This will help you make sure that your comprehension is actually accurate. It’s also a good way to demonstrate that you’re absorbing the information you’re given and making it your own.
    
If, even after a design choice is explained to you, it still doesn’t seem like the best one, don’t be afraid to say so! Having a productive discussion about various solutions to a problem is valuable both for you and your employers. It will help you develop your own educated opinions about code style, and sometimes an outside observer who hasn’t lived with this codebase for years will be able to see problems that people who’ve gotten too used to it can’t.

Dealing with your first real-world application can be daunting, but don’t get discouraged! You have the tools to handle it, and many of the things that are hard about working with it would be hard for any developer in your shoes. Be an active participant in learning your codebase, break down large problems into smaller chunks, and make sure you understand why things are the way they are, and it will be second nature in no time.
