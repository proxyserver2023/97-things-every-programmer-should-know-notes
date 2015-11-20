#97 Things Every Programmer Should Know
1. Act With Prudence - seb rose
2. Apply Functional Programming Principle - edward garson
3. Act What the User Do? [you are not the user] - giles colborne
4. Automate your coding standard - filip van laenen
5. Beauty is in Simplictity - Jorn Olmheim
6. Before You Refactor - Rajith Attapattu
7. Beware the Share - Udi Dahan
8. The Boy Scout Rule - Robert C Martin [Uncle Bob]
9. Check Your Code First Before Looking to Blame Others - Alan Kelly

#1. Act With Prudence - Seb Rose

Whatever you undertake act with prudence<br/>
and consider the consequences - "Anon"

## Chosing Between 'Do it right' or 'Do it Quick' 
if do it quick - technical debt.<br/>
technical debt vs inadvertent[deliberate] technical debt<br/>

**N.B** Pay Of Technical Debt ASAP. it would be imprudent to do it otherwise

#2. Apply Functional Programming Principle - Edward Garson
[later]

#3. Ask What would the user do? [you are not the user] - giles colborne
We all tend to assume other people think like us but they don't.
<br/>psychology calls this false-consensus bias. When the people think or act differently from us we are
<br/>quite likely to label them subconsciously as defective in some way.

## False-Consensus effect
<pre>
In psychology, the false-consensus effect or false-consensus bias is a cognitive bias 
whereby a person tends to overestimate the extent to which their beliefs or opinions are typical of those of others. 

There is a tendency for people to assume that their own opinions, beliefs, preferences, values, and habits are normal and 
that others also think the same way that they do.[1] This cognitive bias tends to lead to the perception of a consensus 
that does not exist, a "false consensus". This false consensus is significant because it increases self-esteem. 

The need to be normal and fit in with other people is underlined by a desire to conform and be 
liked by others in a social environment.
</pre>

##The Best way to find out how a user thinks is to watch one. 
- Give him a task
- don't help
- keep asking why he is doing like that ?
- why he is not doing like that? 

The first thing you will notice that users do a core of things similarly and then to complete the task in similar order
<br/>and make the same mistakes in the same place

**you should design around that core behavoior**

you will see users get stuck. when you get stuck you look around. when users get stuck they **narrow their focus**.
It becomes harder for them to see soln elsewhere.
<br/>

it is one reason why help text is a poor choice to Poor UI.<br/>
if you must have instructors or help text make sure you locate it right next to your problem areas

A user's narrow focus of attention is why tooltips are more useful than help menus/

It's really better to provide one wayof doing things than two or three shortcuts

you will also find that there is a gap between 
- what user's say they want
- and what they actually do

That's worrying cause the normal way to gather info is to **ask them**

<br/>
it'st why the best way to capture requirements is to watch users.

### Spending an hour watching a user is more informative than spending a day guessing what they want?

#4. Automate your coding Standard - Filip van lanen
New Project Resolution<br/>
Reason to format code
- nobody can own a piece of code by formatting it in his or her favourite way
- we may prevent developers from using antipatterns in order to avoid some common bugs
- we make sure code formatting is part of the build process so that everybody runs it automatically everytime they compile the code
- use static code analysis tools to scan the code for unwanted anti patterns.
if any are found break or build
- learn to configure those tools so that you can scan for your own project specific antipatterns
- Do not only measure test coverage but automatically checks the results too.

Again break the build if test coverage is too slow.<br/>

Finally the coding standard should be dynamic rather than static,<br/>

As the Project evolves the needs of project changes and what <br/>
may have seemed smart in the beginning may not necessarily be smart a few monts later

#5. Beauty is in Simplicity - Jorn Olmhein

####Summary : make your code as simple as possible

"Beauty of style and harmony and grace and good rhythm depends on Simplicity"

There are number of things we strive for in our code -

- Readability
- Maintainability
- Speed Of Development
- The Elusive quality of beauty

Study other peoples' code <br/>
if you have not spent enough time studying other peoples code<br/>
stop reading this right now and find some open source code to study.<br/>

Beauty is born of and found in simplicity

#6. Before you Refactor - Rajith Attapattu

1. The best approach for restructing code is by taking stock of the existing codebase and the tests written against that code. this will help you understand the strengths and weakness of the code as it currently stands, so you ensure that you retain the strong points while avoiding the mistakes, we all think we can do better than the existing system .. until we end up with something no better or even worse than the previous incarnation because we failed to learn from the existing system's mistakes

2. Avoid the temptation to rewrite everything. it is best to reuse as much code as possible. no matter how ugly the code is, it has already heen tested, reviewed etc. Throwing away the old code - especially if it was in production - means that **you are throwing away months (or years) of tested, batlle-hardened** code that may have had certain workarounds and bugfixes you aren't aware of. if you don't take this into account, the new code you write may end up showing the same mysterious bugs that were fixed in the old code. This will waste a lot of time, effort, and knowledge gained over the years

3. Many incremental changes are better than one massive change. incremental changes allows you to gauge the impact on the system more easily through feedback after you make a change. This can lead to frustration and pressure that can in turn result in bad decissions. A couple of test failures at a time is easier to deal with, leading to a more manageable approach

4. After each development iteration, it is important to ensure that the existing tests pass. Add new tests if the existing tests are not sufficient to cover the changes you made. Do not throw away the tests from the old code with outdue-consideration. On the surface, some if these tests may not appear to be applicable to your new design, but it would be well worth the effort to dig deep down into the reasons why this particular test was added.

5. Personal preferences and ego shouldn’t get in the way. If something isn’t broken, why fix it? That the style or the structure of the code does not meet your personal preference is not a valid reason for restructuring. Thinking you could do a better job than the previous programmer is not a valid reason, either

6. New technology is an insufficient reason to refactor. One of the worst reasons
to refactor is because the current code is way behind all the cool technology we have today, and we believe that a new language or framework can do things a lot more elegantly. Unless a cost-benefit analysis shows that
a new language or framework will result in significant improvements in
functionality, maintainability, or productivity, it is best to leave it as it is. 

7. Remember that humans make mistakes. Restructuring will not always
guarantee that the new code will be better—or even as good as—the previous attempt. I have seen and been a part of several failed restructuring
attempts. It wasn’t pretty, but it was human.

#7. Beware the Share - Udi Dahan

####Summary : Try to reduce the Dependecy.

Something Critical in Software Development <br/>
** Context **

The Libraries of Shared Code I created tied the shoelaces of each foot to the
other. Steps by one business domain could not be made without first synchronizing with the other. Maintenance costs in those independent functions used
to be negligible, but the common library required an order of magnitude more
testing.

While I’d decreased the absolute number of lines of code in the system, I had
increased the number of dependencies. 

The context of these dependencies is
critical—had they been localized, the sharing may have been justified and had
some positive value. 

When these dependencies aren’t held in check, their tendrils entangle the larger concerns of the system, even though the code itself
looks just fine

These mistakes are insidious in that, at their core, they sound like a good idea.

When applied in the right context, these techniques are valuable. 

In the wrong
context, they increase cost rather than value. When coming into an existing
codebase with no knowledge of where the various parts will be used, I’m much
more careful these days about what is shared.
Beware the share. 

####Check your context. Only then, proceed.

#8. The BoyScout Rule - Robert C Martin [Uncle bob]

"Always leave the campground clearer than you found it" - The Boy Scout

If you find a mess on the ground, you clean it up regardless of
who might have made it. 

You intentionally improve the environment for the
next group of campers. 


What if we followed a similar rule in our code: “Always check a module in
cleaner than when you checked it out”? 

Regardless of who the original author
was, what if we always made some effort, no matter how small, to improve the
module? What would be the result?

1. you might simply improve the name of the variable
2. split one long function into two smaller functions
3. might break a **Circular Dependency**, or add an interface to **decouple policy** from detail.

#9. Check Your Code First Before Looking to blame others - Allan Kelly

Developers-All of us!- often have trouble believing our own code is broken. 

it is just som improbable that, for once, it must be the compiler that's broken.

To Find out your hidden problem 
- all the debugging advice applies
- isolate the problem 
- stubout calls 
- surround it with tests
- check calling conventions
- look out for stack corruption
- variable type mismatches and try the code on different machines and different build configurations, such as debug and release
- question your own assumptions and the assumptions of others.

When Someone else is reporting a problem you cannot duplicate, go and see what they are doing. 

They may be doing something you never thought of or doing something in a different order.

My personal Rule is taht if I have a bug I can't pin down, and i'm starting to
think it's the compiler then it's time to look for stack corruption. this is
especially true if adding trace code makes the problem move around

#### MultiThreaded Problems
another source of problems where **hair turns gray** and induce screaming at the machine. All the recommendations to favor simple code are multiplied when a system is multithreaded.

Debugging and unit tests cannot be relied on to find such bugs with any consistency, so simplicity of design is paramount.

#### Sherlock
So, before you rush to blame the compiler,
remember -
**"Once you eliminate the impossible, whatever remains,
no matter how improbable, must be the truth"

