Theory behind deCheem
===============================================

The parts of deCheem
------------------------------------
To perform any deCheemic analysis, you will need to make use of three things:

* the deCheem Inference Engine
* the deCheem Belief Language
* a `user interface <https://enterprise.decheem.io/?session=eyJkaXNwbGF5VGhlbkVkaXRvciI6dHJ1ZSwic2VsZWN0ZWRCZWxpZWZCYXNlVXVpZCI6ImFiYjk4NDdmLTY1NDAtNGFjOS04MDA1LWRiOThjZWFjOGVhZiIsImRlQ2hlZW1DYXNlRGlzcGxheU1vZGUiOiIxIiwic2Vzc2lvblRpdGxlIjoiTmV3IGRlQ2hlZW0gc2Vzc2lvbiIsInBpbkZpbGVOYW1lIjpmYWxzZSwicGlubmVkRmlsZU5hbWUiOiIiLCJwdWJsaWNCZWxpZWZCYXNlc1V1aWRBcnJheSI6WyI5ZmRmZDAwZS1hODYyLTQ5MzItODMyZS0wY2IxOGI3M2FiOGEiXSwic2Vzc2lvbkRlc2NyaXB0aW9uIjoiRGVzY3JpcHRpb24gb2YgdGhlIHNlc3Npb24iLCJhcnJheU9mU2l0dWF0aW9ucyI6W3siZXhwbG9yZVRpdGxlIjoiV2hlbiBkb2VzIEhvYmJlcyBjb25zaWRlciBpdCBwb3NzaWJsZSBmb3IgdGhlIHdvcmxkIHRvIG5vdCBiZSBpbiBhIHN0YXRlIG9mIHdhcj8iLCJleHBsb3JlU3VidGl0bGUiOiIiLCJzaXR1YXRpb25PYmplY3QiOnsiVGhlIHBoaWxvc29waHkgb2YgVGhvbWFzIEhvYmJlcyBpcyBiZWluZyBjb25zaWRlcmVkLiI6dHJ1ZSwiVGhlIHdvcmxkIGlzIGluIGEgc3RhdGUgb2Ygd2FyLiI6ZmFsc2V9fSx7ImV4cGxvcmVUaXRsZSI6IldoYXQgZG8gSG9iYmVzIGFuZCBMb2NrZSBzYXkgYWJvdXQgYSB3b3JsZCB0aGF0IGlzIGluIGEgc3RhdGUgb2Ygd2FyLCBidXQgcmVzb3VyY2VzIGFyZSBsaW1pdGxlc3M%2FIiwiZXhwbG9yZVN1YnRpdGxlIjoiIiwic2l0dWF0aW9uT2JqZWN0Ijp7IlRoZSBwaGlsb3NvcGh5IG9mIFRob21hcyBIb2JiZXMgaXMgYmVpbmcgY29uc2lkZXJlZC4iOnRydWUsIlRoZSB3b3JsZCBpcyBpbiBhIHN0YXRlIG9mIHdhci4iOnRydWUsIlRoZSByZXNvdXJjZXMgaW4gdGhlIHdvcmxkIGlzIGxpbWl0bGVzcy4gICAgICAgICI6dHJ1ZSwiVGhlIHBoaWxvc29waHkgb2YgSm9obiBMb2NrZSBpcyBiZWluZyBjb25zaWRlcmVkLiI6dHJ1ZX19XX0%3D>`_.

The deCheem Inference Engine is makes use of set-theory for reasoning. It imagines the world as the universal set of situations, and beliefs as rules that asserts claims about the existence or non-existence of subsets of these situations. 

The deCheem Belief Language is designed to be as close to natural language as possible. It eschews all forms of data type definitions in order to fully expose the expressive power of natural language. This is why deCheemBL statements reads like human language, and is also interpreted computationally exactly like how it reads in human language.

User interfaces uses deCheemBL to interact with instances of the deCheem IE in the backend, allowing one to explore belief systems intuitively without having to deal with any complicated syntax or code.


Sets vs Always, Never and Possibly.
-----------
deCheem operates on the belief that all beliefs can be constructed out of the subject(s) and statement(s) about the subject(s). Statements are about whether a situation applies, not applies or perhaps applies (Possibly, mostly, probably, often...) to a situation. 
deCheem encourages users to use 'Always' and 'Never' as modals in their statements, and pushes users to figure out why they are hesitant to make hard statements about the 'Always'ness or 'Never'ness of a situation.

By interpreting what 'Always' or 'Never' says about the existence of subsets of situations in the world, deCheem is able to help you derive the implications of any argument in this belief system. 

This file `here <https://docs.google.com/spreadsheets/d/16sUikzHOWCzJLGlTpIpeP4ojyGBsPNrKz8bOs8zeLQM/edit?usp=sharing>`_ illustrates how deCheem statements are used to filter out sets of situations out of the set of all possible situations.
Sheet A shows how 6 different beliefs translate to statements about the (non-)existence of certain subsets of situations.
Sheet B shows 3 beliefs overlay to form a final world view, which can be 'explored' to find out what the implications are in each explore.

A live demo of deCheemBL, the deCheem Inference Engine and a suitable user-interface can be found `here <https://enterprise.decheem.io/?session=eyJkaXNwbGF5VGhlbkVkaXRvciI6dHJ1ZSwic2VsZWN0ZWRCZWxpZWZCYXNlVXVpZCI6ImFiYjk4NDdmLTY1NDAtNGFjOS04MDA1LWRiOThjZWFjOGVhZiIsImRlQ2hlZW1DYXNlRGlzcGxheU1vZGUiOiIxIiwic2Vzc2lvblRpdGxlIjoiTmV3IGRlQ2hlZW0gc2Vzc2lvbiIsInBpbkZpbGVOYW1lIjpmYWxzZSwicGlubmVkRmlsZU5hbWUiOiIiLCJwdWJsaWNCZWxpZWZCYXNlc1V1aWRBcnJheSI6WyI5ZmRmZDAwZS1hODYyLTQ5MzItODMyZS0wY2IxOGI3M2FiOGEiXSwic2Vzc2lvbkRlc2NyaXB0aW9uIjoiRGVzY3JpcHRpb24gb2YgdGhlIHNlc3Npb24iLCJhcnJheU9mU2l0dWF0aW9ucyI6W3siZXhwbG9yZVRpdGxlIjoiV2hlbiBkb2VzIEhvYmJlcyBjb25zaWRlciBpdCBwb3NzaWJsZSBmb3IgdGhlIHdvcmxkIHRvIG5vdCBiZSBpbiBhIHN0YXRlIG9mIHdhcj8iLCJleHBsb3JlU3VidGl0bGUiOiIiLCJzaXR1YXRpb25PYmplY3QiOnsiVGhlIHBoaWxvc29waHkgb2YgVGhvbWFzIEhvYmJlcyBpcyBiZWluZyBjb25zaWRlcmVkLiI6dHJ1ZSwiVGhlIHdvcmxkIGlzIGluIGEgc3RhdGUgb2Ygd2FyLiI6ZmFsc2V9fSx7ImV4cGxvcmVUaXRsZSI6IldoYXQgZG8gSG9iYmVzIGFuZCBMb2NrZSBzYXkgYWJvdXQgYSB3b3JsZCB0aGF0IGlzIGluIGEgc3RhdGUgb2Ygd2FyLCBidXQgcmVzb3VyY2VzIGFyZSBsaW1pdGxlc3M%2FIiwiZXhwbG9yZVN1YnRpdGxlIjoiIiwic2l0dWF0aW9uT2JqZWN0Ijp7IlRoZSBwaGlsb3NvcGh5IG9mIFRob21hcyBIb2JiZXMgaXMgYmVpbmcgY29uc2lkZXJlZC4iOnRydWUsIlRoZSB3b3JsZCBpcyBpbiBhIHN0YXRlIG9mIHdhci4iOnRydWUsIlRoZSByZXNvdXJjZXMgaW4gdGhlIHdvcmxkIGlzIGxpbWl0bGVzcy4gICAgICAgICI6dHJ1ZSwiVGhlIHBoaWxvc29waHkgb2YgSm9obiBMb2NrZSBpcyBiZWluZyBjb25zaWRlcmVkLiI6dHJ1ZX19XX0%3D>`_.

deCheemQL samples
----------------------------------------

Here are examples of how deCheem beliefs are stored and queried/explored in order to get the inference results we need.

**Belief Base sample**

The following is an example of how a belief base with 6 beliefs is stored in a data base. 

You are free to store it in any database type you want as long as the object structure below is respected when the belief base is stored and retrieved.

.. code-block:: json

  {
    "then": [
      {
        "case": {
          "type": "LET",
          "modalPhrases": [
            {
              "modal": "Always",
              "properties": {
                "The world is in a state of war.": true
              }
            }
          ],
          "filterPhrases": [
            {
              "The world is in the state of nature.": true,
              "The individual in question is rational.": true,
              "The resources in the world is limitless.": false,
              "The philosophy of Thomas Hobbes is being considered.": true
            }
          ]
        },
        "beliefUniqueId": "426aa178-be38-432f-b9a5-9ab35e09d4ef"
      },
      {
        "case": {
          "type": "LET",
          "modalPhrases": [
            {
              "modal": "Always",
              "properties": {
                "The collective in question is rational.": true
              }
            },
            {
              "modal": "Always",
              "properties": {
                "Force is deployed to bring about peace.": true
              }
            }
          ],
          "filterPhrases": [
            {
              "The world is in a state of war.": false,
              "The philosophy of Thomas Hobbes is being considered.": true
            }
          ]
        },
        "beliefUniqueId": "134c21d4-7005-4bdc-9ddc-e39991223328"
      },
      {
        "case": {
          "type": "LET",
          "modalPhrases": [
            {
              "modal": "Always",
              "properties": {
                "The individual's liberties are constrained by their innate morality.": true
              }
            }
          ],
          "filterPhrases": [
            {
              "The individual has liberties.": true,
              "The world is in the state of nature.": true,
              "The philosophy of John Locke is being considered.": true
            }
          ]
        },
        "beliefUniqueId": "c1667128-8f29-4c29-82dc-55af15127a3b"
      },
      {
        "case": {
          "type": "LET",
          "modalPhrases": [
            {
              "modal": "Always",
              "properties": {
                "The world is in a state of war.": false
              }
            }
          ],
          "filterPhrases": [
            {
              "The resources in the world is limitless.": true,
              "The philosophy of John Locke is being considered.": true
            }
          ]
        },
        "beliefUniqueId": "c6ac2033-905d-4e8b-bcb8-24b6c4c19b0c"
      },
      {
        "case": {
          "type": "LET",
          "modalPhrases": [
            {
              "modal": "Always",
              "properties": {
                "The collective is in agreement on the methods of punishment and enforcement.": false
              }
            }
          ],
          "filterPhrases": [
            {
              "The world is in a state of war.": true,
              "The world is in the state of nature.": true,
              "The philosophy of John Locke is being considered.": true
            }
          ]
        },
        "beliefUniqueId": "791ea8f0-4779-4d64-b8b7-478bdf2b979e"
      },
      {
        "case": {
          "type": "LET",
          "modalPhrases": [
            {
              "modal": "Always",
              "properties": {
                "The collective in question is rational.": true
              }
            }
          ],
          "filterPhrases": [
            {
              "The collective is in agreement on the methods of punishment and enforcement.": true
            }
          ]
        },
        "beliefUniqueId": "120dc259-2033-47b9-a5f3-cb316e4b883f"
      }
    ],
    "beliefBaseName": "Political philosophy demo",
    "beliefbaseowner": "guangmian@gmail.com"
  }

**Explore query**

You submit a request to the deCheem Inference Engine in order to infer what the implications of an initial situation will be. 
The deCheem Inference Engine takes two arguments: the deCheem Belief Base object as show above, and the simple object below representing the situation you want to explore. 

The actual code of the deCheem Inference Engine will be made public at a later stage.

.. code-block:: json 

  {
    "The philosophy of Thomas Hobbes is being considered.": true,
    "The philosophy of John Locke is being considered.": true,
    "The world is in the state of nature.": true,
    "The resources in the world is limitless.": true,
    "The individual's liberties are constrained by their innate morality.": false
  }

**Explore results**

After the Inference Engine has received the Explore object and the Belief Base to base the inference on, it processes the situation and returns a result object like the one below:

.. code-block:: json

  {
    "resultCode": "Success",
    "resultReason": "Successful with no errors found",
    "exploreResults": {
      "possible": true,
      "reasoningSteps": [
        {
          "deducedProperty": {
            "The individual has liberties.": false
          },
          "sourceBeliefId": "c1667128-8f29-4c29-82dc-55af15127a3b"
        },
        {
          "deducedProperty": {
            "The world is in a state of war.": false
          },
          "sourceBeliefId": "c6ac2033-905d-4e8b-bcb8-24b6c4c19b0c"
        },
        {
          "deducedProperty": {
            "The collective in question is rational.": true
          },
          "sourceBeliefId": "134c21d4-7005-4bdc-9ddc-e39991223328"
        },
        {
          "deducedProperty": {
            "Force is deployed to bring about peace.": true
          },
          "sourceBeliefId": "134c21d4-7005-4bdc-9ddc-e39991223328"
        }
      ]
    }
  }


This result object can then be used to power all kinds of visualisations and logic on the frontend of your application.
