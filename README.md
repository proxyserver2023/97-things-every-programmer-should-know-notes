#97 Things Every Programmer Should Know
1. Act With Prudence - seb rose
2. Apply Functional Programming Principle - edward garson
3. Act What the User Do? [you are not the user] - giles colborne
4. Automate your coding standard - filip van laenen

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

# Automate your coding Standard - Filip van lanen
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

#Beauty is in Simplicity - Jorn Olmhein

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

