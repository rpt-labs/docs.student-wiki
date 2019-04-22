# Code Review Best Practices

### A proper mindset

Code reviews are a great way to improve the quality of the code your team writes, but only if everyone shares a positive, growth-oriented mindset. Without such a mindset, code reviews can become a major source of conflict for your team.

As an author, it's easy to get defensive about our code, especially when we take pride in our work. Stay open minded during a code review and try not to take any suggestion personally, your reviewer is only trying to help. As a reviewer, be gentle with your suggestions, explain them fully, and always make it about the code, never the author.

Share this mindset and embrace code reviews as a positive learning experience for everyone.

### Why code reviews are important

* **Learn about the technical challenges your team is working through.** Being able to talk cogently about the challenges your team faced will be invaluable during your job search.

* **Learn the entire codebase.** This knowledge will make you much more effective over the course of the project because you will be able to contribute to any feature without a steep onboarding curve. It will also help you talk more broadly about your project with potential employers.

* **Learn new ways to solve problems.** When reviewing someone's code, you might discover an alternate solution that you hadn't considered.

* **Learn how to write maintainable code.** Learning to write code for other engineers is an often overlooked skill that will be foundational to your success when working with a team of software engineers while on the job.

### When to perform a code review

Ideally, every line of code that makes it to production should be reviewed by another member of the team. When using GitHub, a Pull Request is a great time to perform a code review. To minimize unproductive context switching, you should structure code reviews asynchronously.

After you finish a task and submit a Pull Request, instead of interrupting a team member to have them review it immediately, grab another task, cut a new branch, and get back to work. It's up to your team to decide who will be responsible for each review, but the important part is that they can do it on their own time when they are interruptable. A well thought out file structure will ensure your group's ability to continue working and avoid merge conflicts.

To encourage the above described workflow, it's very helpful to include code reviews in your task tracking system and have the review status available to the team. If you're using waffle.io, you can add a "Needs Review" column and [automatically track pull requests](https://github.com/waffleio/waffle.io/wiki/Recommended-Workflow-Using-Pull-Requests-&-Automatic-Work-Tracking).

It's important to note that not every task can be reviewed asyncronously. Your team should decide on a strategy for any blocking task that must get pushed to the whole team, like emergency bugfixes. Likely that could mean an exception to the asyncronous rule, making a short interruption acceptable.

### How to perform a code review

#### As a reviewer

* **There's no one right way to do everything, and that's OK.** When you come across some code that isn't written exactly how you would have done it, ask yourself if it matters. If it works and follows your group's decided upon best practices and style guide, chances are it's ok for now. Don't fall into the trap of [bikeshedding](https://en.wikipedia.org/wiki/Parkinson%27s_law_of_triviality) when you could be more productive by actually writing code rather than just reviewing it.

* **Read through each line of code changed.** If you see something you want to comment on, you should do so with an in-line comment. This is an easy way to provide context and will make your comments shorter and easier for the rest of your team to read. If you offer a different point of view, always explain your suggestions and offer solutions. Remember to make each comment about the code, not the coder. See [what to look for during a review](#what-to-look-for-during-a-review) for ideas of things to comment on.

* **Compliment and reinforce good practices.** Code reviews are not just to point out what's wrong. If you see some exceptional work, let the author know! It will make them feel warm and fuzzy.

* **Scale your review intensity based on code sensitivity.** If you are reviewing a trivial change, you shouldn't spend that much time on it. If you're reviewing a critical feature, spend a good chunk of time on it. Consider getting a second or third opinion for particularly critical code.

* **Delegate work to your tools whenever possible.** Many style rules can be implemented in a linter, and tests can be run with continuous integration.

* **Confirm that the code works by checking it out locally.** The author might have made some config/environment change that they forgot about. GitHub gives you easy steps on how to do this at the bottom of a PR. This is especially important if you have not yet created a robust testing suite for your code or you don't have continuous integration set up to run them.


#### As an author

* **A code review is not the time to catch bugs for the first time.** Write your code against any existing standards document you have (style guide, [best practices](#what-to-look-for-during-a-review)) and test your own code extensively before you submit it for review. You should not submit anything in a broken state.

* **Review your own code first.** Make sure to `git add` and `git diff --staged` to examine the changes. This is a great time to ensure that:
  - There are no lingering `console.log` or `debugger` statements?
  - There are no TODOs or FIXMEs that need to be addressed
  - All your comments make sense
  - No unnecessary files are being committed:
    - `.DS_Store`
    - Third-party libs that are managed via package manager (e.g., `node_modules`, `bower_components`)
    - compiled files (e.g., .pyc from .py, or .js compiled from coffescript)
    - temporary files generated by text editors
    - database dumps or files
    - log files
    - API keys — provide these via the process's environment variables

* **Include a short, useful message for each commit** that provides context for the enclosed code. If you keep commits small, going back to make changes from the review comments is much easier.

* **Keep the amount of code to review short.** A massive submission will likely be glossed over or not read at all.

### What to look for during a review

In addition to your team's agreed upon style guide, consider some of the following:

* **Single Responsibility Principle** - The idea that functions/classes/modules should have one-and-only-one responsibility. This is much harder than one might expect. If you have to use “and” to finish describing what a function is capable of doing, it might be at the wrong level of abstraction.

* **Code duplication** - Consider the “three strikes” rule. If code is copied once, it’s usually okay as trying to deduplicate any earlier might be a premature optimiztion. If it’s copied again, it should be refactored so that the common functionality is split out.

* **Squint-test offenses** - If you squint your eyes, does the shape of this code look identical to other shapes? Are there patterns that might indicate other problems in the code’s structure? Deeply nested code is something you can easily catch with the squint test.

* **Readability** - Is the code easy to understand? Do you have to pause frequently during the review to decipher it?

* **Cleverness** - Avoid being overly clever with your code. If you cram too much functionality into one line, you're doing every other engineer (even your future self) a disservice by making it very hard. Favor expressiveness over terseness.

* **Commented code** - Sometimes you want to commit commented (i.e., dead) code because you think you or a teammate will need it again soon. Instead of leaving a mess, use `git tag` to create an easy reference to the commit that contains the code that you want to comment out, and then delete it instead.

* **Variable names** - `foo` or `bar` are probably not useful names for data structures. `e` is similarly not useful when compared to `error`. Be as verbose as you need. Expressive variable names make it easier to understand code when we have to revisit it later. You're just going to minify it in production anyway.

* **Function names** - Naming things is hard. If a function is named `getMessageQueueName` and it is actually doing something completely different like sanitizing HTML from the input, then that’s an inaccurate function name and probably a misleading function. Do all the functions you're reviewing have names that accurately describe what they're doing?

* **Function length** - If a function is too long, it might be a good sign that it is trying to do too much and break the Single Responsibility Principle.

* **File length** - If the file is more than a couple hundred lines, it might also be a good time to start thinking about splitting it out.


* **Efficiency** - If there’s an algorithm in the code, is it using an efficient implementation? For example, iterating over a list of keys in an object is an inefficient way to locate a desired value.

* **Potential bugs** - Are there off-by-one errors? Will the loops terminate in the way we expect? Will they terminate at all?

* **Error handling** - Are errors handled gracefully and explicitly where necessary? Have custom errors been added? If so, are they useful?

* **Number of function arguments** - Do functions have many arguments? If so, consider grouping them in a different way (i.e. as an object)



