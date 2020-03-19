Frequently Asked Questions
==================================


What is the best way to phrase a belief?
--------------------------------------------
Always limit the scope of what you want to say as much as possible. 

* Start the belief with 'the' where possible instead of 'a'. For example, say "The person", instead of "A person". The best way to describe an abstract person would actually be "The person in question". 
* When in doubt, over-specify what you mean instead of under-specify.

How does deCheem represent beliefs about different subjects without using IF-ELSE statements?
--------------------------------------------
IF-ELSE statements are needed when relating between two different subjects. But this can be bypassed by phrasing everything as a property of a common subject.
'Situations' is the best choice here, as it allows anything under the sun to be phrased in terms of situations, thus achieving conditionality without resorting to IF-ELSE clauses. This also ensures that statements are sequence-insensitive.

Why is a relational database not suitable for this?
--------------------------------------------
To analyse 20 different possible situation types, we would need a table with 2^20 rows. This is unscalable and is not what relational databases should be used for. 

Why are graph databases not suitable for this?
--------------------------------------------
Graph databases sees things as nodes with fixed relationships. deCheem forms relationships between different nodes based on certain conditions, and the inference layer is not native to graph databases.

Why is a decision-tree not useable for this?
--------------------------------------------
Decision trees operates on branches. If an idea in a deep branch has links to another idea in an earlier branch, there is no efficient way to represent that relationship.

Why is a argument-map not good for this?
--------------------------------------------
Argument-maps are similar to decision trees and therefore share the same pitfalls.

Why is Prolog not useable for this?
--------------------------------------------
Prolog is great for quantitative inferences and relationship deduction when properties share only inherit properties from a single parent.
However, numerical methods are useless against analysis of beliefs, and the ability for beliefs to inherit properties from any number of situations makes Prolog a bad choice to use for belief analysis.

Why is the Carneades system not useable for this?
--------------------------------------------
??


What can deCheem not deal with? (conditionals based on a situation)
--------------------------------------------
The current 'flat' implementation of deCheem allows for almost all conditionals to be stated, except those that pivot on a single condition.
See this example, which cannot be constructed without resorting to IF-ELSE statements.
```
IF (pigs-are-cute) be never (sky-is-blue)
  then:
  LET (!pigs-are-cute) be (!sky-is-blue)
```

How do you compartmentalise belief-systems?
--------------------------------------------
If you want to categorise belief-systems based on their provenance, simply add that as an additional description of the situation.

Is deCheem a NLP project?
--------------------------------------------
Nope. deCheem neither is nor aims to do Natural Language Processing in any way.

Why can't deCheem automatically solve all confusion in conversations?
--------------------------------------------
deCheem shifts the complexity of reasoning out of code and math and into the realm of language.
While this grants it enables the user to utilise any corner of his/her vocabulary, it cannot help the user extend his/her vocabulary.

Why doesn't deCheem use weighting? 
--------------------------------------------
Using weightage/votes to determine the correctness of a belief is fundamentally against the idea of deCheem, which is to use logical deduction to arrive at facts about our world. 
If you find yourself struggling with the correctness of a certain belief, think about a specific subset of situations with this belief that you for sure is correct, and document that instead.

But 'not good' is not necessarily 'bad', so how can things be binary.
--------------------------------------------
Indeed, 'not good' is not the same as 'bad', just like 'not hot' is not necessarily 'cold'. deCheem leaves it to the user to determine what the opposite of each situation is, be it a new situation or simply the negation of the former.

How do you deal with 'scales of things' or 'rankings' or 'priorities'.
--------------------------------------------
'Scales' have similar pitfalls to weightage - something has to be more important than everything else, and when it's not, then something else is. This means that any arbitrary ranking-list can be expressed as a series of beliefs about the utmost importance of a certain thing under certain circumstances.

How efficient is deCheem?
--------------------------------------------
deCheem is the most efficient way of generating arguments. 3 beliefs relating 4 situations generates 16 different situations and even more arguments. 

Should we use complex beliefs or try to break them down?
--------------------------------------------
deCheem Inference Engine doesn't care if you are long-winded or not, but humans do. Try to deconstruct your beliefs into simpler ones if possible for readability of your arguments.


What is the difference between regular and cluster 'and'.
--------------------------------------------
...
