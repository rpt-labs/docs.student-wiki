## One Line Takeaways

One-line takeaways are carefully-honed sentences that attempt to compress complex ideas into the simplest statement possible.

If you hear a new 1-line-takeaway that is not on this page, please email your campus's communications@ so we can add it here!

### Recursion

“A task can be solved recursively if, after a little bit of the processing is completed, the remainder of the problem has a structure that remains equivalent to the original problem.”

The recursive ‘contains’ function, stated in a question:
"Do I store the value directly, or would any of my children answer this exact question affirmatively?"

### Data structures

"Fold knowledge into data so program logic can be stupid and robust."

### Serialization

“Serializing is when you take a value and build a serial representation of it as a string--for example, a representation you could communicate over a telephone."


### TDD

“You won’t know that your test code can possibly fail unless you first run it on a known-bad implementation.”


### Closure

A closure is a function that retains ongoing access to the variables of the scope it was created in (even after outer function calls have returned).


### The debugger’s question

"Whenever you notice that reality has diverged from your expectation, place a breakpoint right before the symptomatic line of code and ask yourself this question: What piece of code justifies my expectation that this would run the way I expected."


### Time Complexity of writing a program

"If your program allows each feature to interact with all other features, then the cost to you in man hours of having written the program would be polynomial, with respect to the number of features written."


### This

"The keyword this generally refers to the object to the left of the dot AT CALL TIME of the function referencing 'this'".

“The keyword ‘'this' can’t possibly mean anything until the function it appears within is running.”


### Prototype Chains

"When a property lookup fails on an object, that lookup is invisibly delegated up to its prototype object."


### Classes

"A class is any construct that can produce a fleet of similar instances--objects that conform to the same interface."


### Ambiguity in the word "prototype"

Because this distinction is so complex, the following section contains a mixture of long form explanation and 1 line takeaways.

The word "prototype" is used ambiguously to mean 2 very different things, and you must be careful to discern which one is intended EVERY TIME you hear the word.

1. When talking about an object, mentioning its "prototype" means "the object to which that object will delegate its failed lookups".
    * For some JS environments like Node.js, object is stored in the `.__proto__` property
    * It has NO RELATIONSHIP with the `.prototype` property available on function objects, and `.prototype` will not be an available key on the vast majority of objects
    * If a martial arts student can be thought of as an analogy for an object, then you might say: "The new cadet is learning to be just like his prototype, who is a seasoned warrior deserving of great respect."
1. When talking about a class, mentioning its "prototype" means "the companion object stored in the constructor's `.prototype` property, to which that constructor will make all of its instances delegate their failed lookups".
    * For any function being used as a constructor, this object is stored in the `.prototype` property
    * It has NO RELATIONSHIP with the `.__proto__` property of that function, however the `.prototype` property of a constructor function will be the same object as the `.__proto__` property of its instances.
    * If a martial arts dojo can be thought of as an analogy for a class, then you might say: "The dojo has a new prototype, which it is encouraging all its cadets to emulate. She is a seasoned warrior deserving of great respect." Note that in this example, you wouldn't expect the dojo itself to "emulate its prototype" in any way, since dojos don't fight with people. They create fighters that will "emulate" something.

To reinforce this distinction, consider the fact that every function is an object, and as such it will delegate any failed lookups somewhere (`.__proto__`). Furthermore, some functions are used as constructors for classes, so they have a companion object (`.prototype`) that they will make their instances delegate to. Thus every constructor function "has a prototype" in two different senses at the same time. In one sense, the function will delegate failed lookups somewhere. In another sense, it has a `.prototype` property that it will make its instances delegate to. There is NO OVERLAP in these two uses of the word, and to try and consolidate or mix them will confuse you tremendously.


### Use of hash tables

"Any time you are faced with a programming problem that has a higher complexity/cost than you like, and you want to knock it down to a lower tier of complexity/cost, you should consider using some form of indexing using hashes."


### MVC architecture

“Avoid storing model state in the view. Never rely on the visualized output as the source of truth.”


### Security

"You want to escape user input right before it is sent to another system, using the appropriate context for that system."


### Cross-Origin

Start by assuming that an "origin" and a "domain" are the same thing (although they are slightly different). The browser has introduced restrictions on how the code downloaded from one origin (the domain in your url bar) may communicate with code from other domains.


### Routing

Routing is the process of mapping a URL pattern that your visitor might request to the routine that should be run to satisfy the request.


### Databases

"In a one-to-many relationship, the foreign key reference needs to be stored in the table with many entries."
