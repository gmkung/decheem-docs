User Guide
===============================================

Getting started
------------------------------------
deCheem is a tool for sketching and testing rule/belief systems, and the layout is meant to help you with this process.
deCheem was designed to allow everyone to start sketching and testing ideas and rules within a few minutes. deCheem is a tool for sketching and testing rule/belief systems, and the layout is meant to help you with this process.
If you need some help to get started, here are some instructions for you!

Creating a deCheem account
^^^^^^^^^^^^
#. To create an account, go to app.decheem.io and click on 'Sign Up'
#. Sign up either with your Google Account or create a fresh user name and password for deCheem.
#. Once done, you will be redirected to the working view, where you can start creating and testing your first rule systems.

Navigating deCheem
^^^^^^^^^^^^
#. If it is your first time logging into deCheem, the first thing to do is to click on the big grey box on the left to create a new rule system.
#. deCheem is a tool for sketching and testing rule/belief systems, and the layout is meant to help you with this process.

    #. The basic building block in deCheem is simply a `basic English sentence <https://simple.wikipedia.org/wiki/Sentence#Basic_English_sentences>`_, which - as a proposition - can be either **true** or **false** (basically a `proposition <https://www.lexico.com/definition/proposition>`_).
    #. Sentences can then be used to build If-Then **Rules**.
    #. A collection of rules forms a **Rule System**, which can then be explored, analysed and tested.

#. Sentences (describing a situation) can be entered directly as part of a rule or simply pinned at the left side under 'Pinned sentences', until you figure out how to fit it into a rule.

    #. Note that sentences should read grammatically correct whether it is standalone (e.g. **The person is guilty**) or as part of a rule (e.g. If the evidence is found then *the person is guilty*)

#. Once you have at least one rule, by default you should see nodes appearing in the graph on the right. This shows the **correlation** between various situations/ideas (aka sentences) and rules.
#. If you want to test and analyse the **causation** between various situations instead, select on 'Causation analysis' at the top-right instead.

    #. In this view, you can explore hypothetic situations described by any combination of sentences (true or false) mentioned in your rule system. 

#. Whenever you want to save your rule system, just click on the save button at the top.


User rights and permissions
^^^^^^^^^^^^
#. deCheem utilises a graph-based user permission system, which basically means that instead of managing access rights through a static folder structure, it allows for any combination of user groups to fit your organisational needs.
#. There are three main kinds of permission entities in deCheem:

    #. **Users** - Like the one you used to log into deCheem, which is represented by your email address.
    #. **Rule Systems** - These are the rule systems that you create through the interface. They can be accessed by Users and/or User Groups.
    #. **User groups** - These are entities that either users or other user groups groups can belong to. User groups also serve as folders in deCheem for grouping Rule Systems together.

#. Permissions for Rule Systems and User Groups are managed the same way. Click on the '+' sign in the Permission Overview interface

    #. **User groups** can be created, viewed and managed by doing a mouse-over on your user avatar at the top right and clicking **Manage User Groups**. 
    #. **Rule System** permissions can be viewed and managed by clicking on the permission management icon in the top right of the Rule System Editor.

#. In the Permission Management Overview, you will see on the left all the entities that have access to the entity you are examining. On the right you will see all the entities that it has access to (only applicable if you are managing User Groups).
#. To add permissions, click on the '+' sign and grant access by any User (Groups) to any User Group or Rule Systems. 
#. To remove permissions, click on the '-' sign next to the entity on the Permission Management Overview to revoke its access.

Features for education
------------------------------
deCheem has several features that are meant to allow philosophy/law educators and students to work together more effectively. 

deCheem Rule Systems (in combination with deCheem causation analysis test cases) could easily be used to replace essays arguing a certain standpoint, or to show where various systems of belief concur and disagree.

If you - as an educator - prefer to offer more guided assignments, deCheem also allows you to create 'rule assembly' assignments that help beginning students quickly understand the process of distilling ideas and rules from existing literature.

For teachers: Creating 'Rule Assembly' assignments 
^^^^^^^^^^^^^^^^^^^^
#. A Rule Assembly assignment is basically a **mix-and-match** exercise where the teacher determines the set of possible sentences to use, and the students have to use them to recreate the rules the teacher had in mind.
#. Imagine you are a teacher of law and you:
    * want your students to read 5 different past cases and distill the rules that led to the judgments in these cases.
    * have created the Rule System yourself and you want your students to try to recreate it, but want to set boundaries of the phrasings that the students can use for ease of marking.
    * want to programmatically mark the work of your students without having to read through every single essay painstakingly. 
#. To prepare such an assignment, you just need to do the following:
    #. Create the Rule System that contain all the rules that you want your student to pick out from the past cases. Save this properly, as it will serve as your **marking scheme**.
    #. In the Rule System selector on the top left, click and duplicate the rule system, and choose to make a 'disassembled' copy of the rule system.
    #. Share this disassembled copy with the User Group where your students are in. Grant only read-only rights so that students have to make a personal copy of it before working on it.
    #. Create a new User Group as a submission folder (see instructions in previous section), and copy down the Submission Code at the bottom of the permission overview of the User Group.
        
        * Grant other teachers and teaching assistants access to this group so they can help you with reviewing the assignments later. Do not add your students to this group.
#. When communicating the assignment to your students, point them to the disassembled copy you shared with them, as well as the Submission Code for them to use once they are done.

For students: Submitting Rule Systems
^^^^^^^^^^^^^^^^^^^^
#. All assignments in deCheem involve the creation of a Rule System, regardless of whether you were giving a disassembled rule system to start with or simply a blank slate to work from.
#. Once you have created and saved the rule system, go to the Permission Overview of the Rule System, and click on 'Submit this rule system'.
#. In the pop-up, enter the Submission Code given to you by your teacher, and adjust the submission name of the Rule System to fit the format given to you by your teacher. 
#. Once done, click Submit. That's it, you have just submitted a timestamped and unlinked copy of your rule system to your teacher.


For teachers: Marking 'Rule Assembly' assignments 
^^^^^^^^^^^^^^^^^^^^
#. Once all your students have used the Submission Code to submit the assignment, you can mark all of them at one go using your marking scheme.
#. Click on the star icon at the top of the page to open up the deCheem scoring interface. 
#. In the first dropdown, select the Rule System that you want to use as the marking scheme.
#. In the second dropdown, select the User Group that is linked to the Submission Code you gave to your students. Once done, all the submitted rule systems will be listed in the table below.
#. Click on 'Go!' to grade all these Rule Systems according to the marking scheme.
#. Each deCheem Rule is broken down and translated into a certain number of assertions in the background. deCheem then uses these assertions to score the students' Rule Systems on two measures:

    * **Completeness** - percentage of the marking scheme's assertions that are also made by the student's rule system.
    * **Correctness** - percentage of the total set of assertions implied by the student's rule system that are also made by the marking scheme.
#. These two measures are then averaged out to give a score reflecting the overall grade of the submitted Rule System.