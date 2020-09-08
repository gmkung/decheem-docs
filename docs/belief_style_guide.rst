deCheem rule writing guide
==================================
Here you will find a number of best practices on how to phrase your rule in order to build the most scalable rule system possible. 

How do I construct a deCheem rule?
--------------------------------------------
Entering new deCheem rules is simple: you just need to phrase your rules in terms of IF-THEN statements.
In these statements, you first describe 'situations', then use the words 'is', 'is possibly' or 'is not' to add what the situation should or should not be.

Here are a few examples:

**Diabetes and sugar**

* **Regular speech**:
   * People who have diabetes should eat less sugar
* **deCheem rule**:
   * If we are in a situation where **the person has diabetes** then it **is** a situation where **the person should eat less sugar**.

**Coconut trees and climate**

* **Regular speech**:
   * If the climate is cold, people should not be trying to plant coconut trees
* **deCheem rule**:
   * If we are in a situations in which **the climate is cold** then it **is not** a situation where **the person should be trying to plant coconut trees**.


Write rules with clear and limited scopes
------------------------------------------------
deCheem analyses are most useful when specific cases can be used to derive very advice about other specific situations. 
In the deCheem world, general rules are derived from the exceptions. This means that the more specific and concise you write your rule, the more useful they become. 
Why is this so? The more specific the scope of a rule (provided it's correct), the higher the chance that it will not over-generalise and end up making an incorrect generalisation about a certain kind of situation. 

A few guidelines:

**Make rules narrow but deep**

Use words like "the" and "in question" to narrow the scope of your rule, and refer to subjects singularly instead of in plural, as using the latter increases the chance of over-generalisations.

**Sentence 1**: If we are in a situation where **people are unhappy** then it **is** a situation where **work is not good**.*

  'People' and 'Work' are used in a way that's too generic here. 'Work' here could mean an artwork, labour of a person or the work in the physics sense. 
    
**Sentence 2**: If we are in a situation where **the person is unhappy** then it **is** a situation where **the work of the person is not good**.

  By introducing 'the' and transforming plural to specific singular (e.g. 'people' to 'person'), the rule lends itself to being used in more situations without risk of generalisation. However one question remains: which person am I talking about?

**Sentence 3**: If we are in a situation where **the person in question is unhappy** then it **is** a situation where **the work of the person in question is not good**.

  Using the words "in question" to denote the person we are talking about this very moment, we distinguish it from the 'abstract person', allow us to introduce phrases like "the person in question is Bill Gates" in other rules that will help sharpen the identity of the person we are talking about. 



Using 'And' and 'And or' right
----------------------------------------------------------
The following two rules sound similar, but actually can mean very different things:

**'AND' within a situation **

  If we are in a situation where **the cat is blue, furry** then it **is** a situation where **the cat is friendly**.
  
...versus...

**'AND' between situations**

  If we are in a situation where **the cat is blue** and/or **the cat is furry** is **Always** a situation where **the cat is friendly**.

The first one implies that only when a cat is *both* blue *and* furry is it also friendly (meaning a cat that is only blue and not furry is not friendly).

The second one implies that when a cat is *either* blue *or* furry, it is also friendly.


Likewise, the same applies when 'and' is applied to the second part of the rule:

**'AND' within a situation**
  Situations in which **the cat is red** is **Never** a situation where **the cat is friendly, cute**.
  
...versus...

**'AND' between situations**

  Situations in which **the cat is red** is **Never** a situation where **the cat is friendly** and **Never** a situation where **the cat is cute**.

The first one implies that when a cat is red, it is not friendly *only when* it is also not cute, and not cute *only when* it is not friendly. 

If the cat is red and cute, it could still be either friendly or not friendly.

The second one implies that when a cat is red, it will definitely be *neither* cute *nor* friendly.
