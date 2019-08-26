Theory behind deCheem
===============================================

The parts of deCheem
------------------------------------
To perform any deCheemic analysis, you will need to make use of three things:

* the deCheem Inference Engine
* the deCheem Belief Language
* a user interface.

The deCheem Inference Engine is based on set-theory. It imagines the world as the universal set of situations, and beliefs as rules that asserts claims about the existence or non-existence of subsets of these situations. 

The deCheem Belief Language is based on naturally language, and it is purposely under-defined in syntax so as to shift meaning-representation from computer languages to natural language. This is why deCheemBL reads like human language, and is also interpreted computationally exactly like how it reads in human language.

User interfaces uses deCheemBL to interact with instances of the deCheem IE in the backend, allowing one to explore belief systems intuitively without having to deal with any complicated syntax or code.


Sets vs Always, Never and Possibly.
-----------
deCheem operates on the belief that all beliefs can be constructed out of the subject(s) and statement(s) about the subject(s). Statements are about whether a situation applies, not applies or something in between (Possibly, mostly, probably, often...). 
If everything is indefinite, no conclusions can be drawn. Therefore deCheem places a strong emphasis on 'Always' and 'Never' as modals, and implores the user to figure out why they are hesitant to make hard statements about the 'Always'ness or 'Never'ness of a situation.

By interpreting what 'Always' or 'Never' says about the existence of subsets of situations in the world, deCheem is able to help you derive the implications of any argument in this belief system. 

This file [here](https://docs.google.com/spreadsheets/d/16sUikzHOWCzJLGlTpIpeP4ojyGBsPNrKz8bOs8zeLQM/edit?usp=sharing) illustrates how deCheem statements are used to filter out sets of situations out of the set of all possible situations.
Sheet A shows how 6 different beliefs translate to statements about the (non-)existence of certain subsets of situations.
Sheet B shows 3 beliefs overlay to form a final world view, which can be 'explored' to find out what the implications are in each explore.
