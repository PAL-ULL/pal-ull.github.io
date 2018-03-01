# Abstraction

https://www.pinterest.es/pin/683702787150046617/

The aim of this activity is to get you to think about what Wing is saying in the following, rather long but important, sentence: 
‘… this feedback loop that one has when you’re abstracting from some physical-world phenomenon, 
creating a mathematical model of this physical-world phenomenon, 
and then analysing the abstraction, 
doing sorts of manipulations of those abstractions, 
and in fact automating the abstraction, 
that then tells us more about the physical-world phenomenon that we’re actually modelling.’

https://youtu.be/C2Pq4N-iE4I


Wing talks about abstractions as a means of ignoring detail that is not of interest. 
Consider the following description of an algorithm for searching a paper and ink dictionary.

Given:

i.  a dictionary
ii. a headword W which appears in the dictionary

to find the definition of W: 

Begin the search with an entry that appears (roughly) in the middle of the dictionary. 

Then there are three possibilities:

1. The current entry’s headword is W. In this case, the definition of W is the definition of the current entry.
2. W appears alphabetically before the current entry’s headword. In this case, the entry with headword W must appear in the first half of the dictionary. Look for the word W, following the same approach, in the first half of the dictionary.
3. W appears alphabetically after the current entry’s headword. In this case, the entry with headword W must appear in the second half of the dictionary. Look for the word W, following the same approach, in the second half of the dictionary.

This is an informal description of an algorithm, but the steps are sufficiently precise that a human should have no problem following them.
This algorithm depends crucially on the fact that the words in a dictionary are alphabetically ordered. 
It also, however, ignores some of the details of paper and ink dictionaries.

Wing’s discussion of abstraction draws on a wide variety of concepts. 
You have come across phrases such as ‘ignoring’ and ‘hiding information’, ‘levels’ and ‘layers’, ‘models’ and ‘implementation’.
It has been left somewhat in the air how these all hang together. 
So next, we will make the relations between them explicit. 

To do so, we will distinguish between two kinds of abstraction:
* abstraction as modelling
* abstraction as encapsulation.

Although Wing deals in great detail with the idea of abstraction as modelling, 
she only hints at the concept of abstraction as encapsulation.
Both are, however, at play in computing.
Distinguishing between them will give you a better understanding of the remainder of Wing’s story. 

# Models
A model which represents the details of interest of this reality. 
For this reason, models are sometimes also referred to as representations.

The previous algorithm for looking up words work with a model of a dictionary as an alphabetically sorted list of headwords,
each paired with its definition. 
The model corresponds to how the data that the algorithm works with are structured. 
This model captures the essentials (i.e. that the dictionary consists of an alphabetically sorted list of words and their definitions) 
and ignores certain details (for example, that a physical dictionary is divided into pages of a certain size and has a cover 
to protect it). 
In other words, the irrelevant details are not reflected by the structure of the data that the algorithm works with.

https://en.wikipedia.org/wiki/The_Treachery_of_Images

Representations, including paintings and drawings, are models. 
This is brilliantly illustrated by René Magritte’s famous painting of a pipe with the words ‘Ceci n’est pas une pipe’ 
(‘This is not a pipe’) underneath. 

Explain how this painting brings home the point that modelling involves two levels: 
the abstraction and the reality which the abstraction models.

The part of reality for which one creates a model or representation doesn’t need to be a static object such as a pipe or dictionary. 
It can also be a process or system which changes over time. 
In that case, the model will not only have to capture any enduring properties of interest, 
but also any changes in time that are of interest. 

https://en.wikipedia.org/wiki/Orrery

For example, in astronomy there is a rich tradition of building such models of the solar system. 
The purpose of such a model, known as an orrery, is to represent the position of the planets relative to each other over time. 

The invention of the orrery is usually attributed to George Graham (1673–1751).
Graham worked on this with the support of the 4th Earl of Orrery, which explains the name. 
The tiny crank on the side of the central cylinder in Figure 8 allows the model to be animated. 
Turning the crank causes the (representations of the) planets to follow a path around 
the (representation of the) Sun at the centre of the model. 
Usually such an animated model is referred to as a simulation. 

# Encapsulation

The model of the solar system also illustrates the second type of abstraction: abstraction as encapsulation. 
The brass cylinder in the middle of the device encloses a clockwork of cogwheels.
This mechanism causes the small spheres representing the planets to rotate around the centre at a velocity that is proportional to the speed of the actual planets. 
The mechanism is hidden from view for the casual user, who is only interested in the movement of the planets.

The layer through which the user interacts with the model is called the interface. 
It hides the detailed workings of the model from the user. 
The interface sits between the user and the layer at which the model is implemented. 
The latter is responsible for making the model do what it is supposed to do. 
This is where the automation of the model takes place.


# Glossary

* abstraction
   provides a handle on complexity by either ignoring detail by means of a model, or hiding detail through the use of encapsulation.

* algorithm
  A precisely stated, step-by-step list of instructions.
  
* data structure
  A way of organising data for use by an algorithm.
  
* encapsulation
  Hiding details of an implementation from users. This is achieved through an interface that sits between the user (or client) and the implementation.
  
* interface
  An interface sits between a user (or client) and an implementation. It hides the details of the implementation from the users or clients of the implementation. (See encapsulation.)
 
* model
  A representation or abstraction of a part of reality which ignores certain details.
   
* simulation
  A working model of a process or a system which changes over time.
