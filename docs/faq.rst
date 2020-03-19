Frequently Asked Questions
==================================

What is the best way to phrase a belief?
--------------------------------------------
Always limit the scope of what you want to say as much as possible. 

* Start the belief with 'the' where possible instead of 'a'. For example, say "The person", instead of "A person". The best way to describe an abstract person would actually be "The person in question". 
* When in doubt, over-specify what you mean instead of under-specify.

What are the most important characteristics to look for in the ideal expert system for managing legal or philosophical knowledge?
--------------------------------------------

Here are a list of considerations that were taken into account during the design process of deCheem.

* **Type-less knowledge entry**

  * A word or phrase can mean different things in different contexts (e.g. club as in golf club or disco club), so any form of 'type' declaration (in the broadest sense of the word) will inevitably limit the ability of that word to take on different meanings (and hence roles) in future situations.
  
* **Sequence-insensitive knowledge acquisition**

  * Expert systems are only considered useful if it can produce accurate advice faster and cover knowledge areas larger than any human can. To achieve this, acquiring and assimilating the knowledge from a large number of sources is essential. To enable large scale knowledge aggregation to take place efficiently, it is crucial that the sequence in which knowledge is entered into the system has no effect on it's usefulness later on. 

* **Deterministic**

  * Probabilistic methods (e.g. text-clustering, correlation-based) do not have a lot of use in philosophical and legal settings, as saying that something is 'maybe' or 'likely' true does not allow one to settle an argument completely. it is therefore important that the framework deduces conclusions, rather than makes a guess of what it is (regardless of the likelihood that it is correct).

* **Syntax-less knowledge entry**

  * For expert systems to be truly useful in the fields of law and philosophy, it should not enforce specific syntax that the user needs to learn in order to document their knowledge. Not only does specific syntax decrease the usability of the system, it also can be seen as a form of 'typing', which has the downsides described above.
  
* **Directionless reasoning**

  * `Forward and backward chaining <https://www.javatpoint.com/forward-chaining-and-backward-chaining-in-ai>`_ are functionalities often looked at in expert systems, but any system that considers 'chaining' as having more than one type will eventually be insufficiently generic for philosophical and legal use cases.

How does deCheem deal with forward and backward chaining?
--------------------------------------------
deCheem intentionally does away with the technical distinction between these two forms of 'chaining'. In the spirit of 'typelessness', deCheem instead has just one way of exploring situations, without taking into account if it's the desired starting or ending situation. The degree to which a particular explore is doing 'forward', 'backward' (or mixed??) chaining is determined by the human language used to describe those situations.

How does deCheem represent beliefs about different subjects without using IF-ELSE statements?
--------------------------------------------
IF-ELSE statements are needed when relating between two different subjects. But this can be bypassed by phrasing everything as a property of a common subject.
'Situations' is the best choice here, as it allows anything under the sun to be phrased in terms of situations, thus achieving conditionality without resorting to IF-ELSE clauses. This also ensures that statements are sequence-insensitive.

Why is a relational database not suitable for this?
--------------------------------------------
To analyse 20 different possible situation types, we would need a table with 2^20 rows. This is unscalable and is not what relational databases should be used for. 

Why are graph databases not suitable for this?
--------------------------------------------
Graph databases sees things as nodes with fixed relationships. deCheem forms relationships between different nodes based on certain conditions, and the inference engine layer is not native to graph databases.

Why are decision-trees not useable for this?
--------------------------------------------
Decision trees operates on branches. If an idea in a deep branch has links to another idea in an earlier branch, there is no efficient way to represent that relationship.

Why is a argument-map not good for this?
--------------------------------------------
Argument-maps are similar to decision trees and therefore share the same pitfalls.

Why is Prolog not useable for this?
--------------------------------------------
`Prolog <https://en.wikipedia.org/wiki/Prolog>`_ is great for quantitative inferences and relationship deduction when properties share only inherit properties from a single parent. 
However, numerical methods are useless against analysis of beliefs, and the need for beliefs to take on different meanings (aka inherit properties) from any number of situations makes Prolog a bad choice to use for belief analysis.
Prolog makes a distinction between 'rules' and 'facts', and that distinction takes away from the 'type-less' nature of a good general expert system.

Why is the Carneades system not useable for this?
--------------------------------------------
When it comes to how knowledge is represented, the `Carneades argumentation system <https://carneades.github.io/about-carneades/>`_ is one of the closest to the deCheem belief language. Subjects and predicates are represented together in 'statements' (belief properties in deCheem's terms), which is one step closer to true 'typelessness'. Carneades also represents only relations between statements in a single direction, while deCheem does that but also allows statements to have true modality (e.g. represent assertions that are true in all cases/directions).
However, when it comes to how conclusions are generated (aka the inference engine), Carneades takes a graph-based approached (e.g. linking nodes to each other through edges) while deCheem goes for a set-based approach. Graphs are meant to show (cor)relation, and it can at best only deal with forward-chaining use-cases, and only for the situations that have been explictly documented either in part or full. deCheem does away with directionality altogether thanks to it's set-based approach, and also allows for deduction of all possible implicit conclusions.

What can deCheem not deal with (natively)?
--------------------------------------------
Working with beliefs with a temporal or numerical nature is possible, but cumbersome without tools to help generate the arbitrary number of beliefs needed to cover temporal or numeric graduations.

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

