.. _About Learner Cohorts:

About Learner Cohorts
#############################

.. tags:: educator, concept

This section provides an introduction to using cohorts to divide the learners in your course into smaller groups.

.. contents::
  :local:
  :depth: 1

For more information about setting up and managing cohorts, see the following topics.

* :ref:`Enable Cohorts`

* :ref:`Setting Up Discussions in Courses with Cohorts<Set up Discussions in Cohorted Courses>`

* :ref:`Guide to Managing Divided Discussions`

For information about discussions in general, see :ref:`About Course Discussions`.

For information about offering different content to different cohorts of learners, see :ref:`Offering Different Content Based on Cohort`.


Overview
*********

To create smaller communities in your course, or to design different course experiences for different groups of learners, you can :ref:`set up cohorts<Enable Cohorts>` in your course.

To use cohorts in your course, you define a set of cohorts that are either random or that reflect some characteristic of the communities of learners in your course. Then, you decide on a strategy for :ref:`assigning learners to these cohorts<Options for Assigning Learners to Cohorts>`.

With learners divided into smaller groups based on cohort, you can give learners a course experience that is specific to the cohort that they belong to. You can divide discussion topics by cohort so that learners only interact with other members of the same cohort. You can create course content in such a way that learners in different cohorts are offered different variations of assignments or exams.


.. note::

   * Every learner must be assigned to a cohort. This ensures that every learner has the ability to read and contribute to course discussion topics.

   * Each learner can be in one and only one cohort.

   To provide learners with a consistent experience throughout the course run, do not change cohort configuration or a learner's cohort assignment after your course begins.

.. _Options for Assigning Learners to Cohorts:


Options for Assigning Learners to Cohorts
*****************************************

Learners are assigned to cohorts either :ref:`automatically<About Auto Cohorts>` or :ref:`manually<Assign Learners to Cohorts Manually>`, dependingon the types of cohorts that you create.

Manual cohorts do not have learners assigned to them unless you manually add learners. Automatic cohorts have learners randomly assigned to them if learners do not belong to any cohort by the time they access the course
content (including the course **Discussion** page or content-specific discussion topics, if discussion topics are divided). If you have not created any automated cohorts by the time learners access course content, a default
automated cohort is created and used for automatic assignment, so that no learner in the course is without a cohort.

Determine the basic strategy that you will use to create cohorts. Typically, your purpose in including the cohort feature determines which assignment option you use for your course.

An :ref:`automated assignment strategy<Implementing the Automated Assignment Strategy>` means that you create cohorts to which learners are assigned automatically and randomly. Automated assignment works well if, for example, you are creating cohorts simply to create small groups of learners. Automated assignment means that learners are assigned randomly to cohorts as they access course content and divided discussion topics. The cohorts that result from automated random assignment are likely to be more equal in size.

A :ref:`manual assignment strategy<Implementing the Manual Assignment Strategy>` means that learners are assigned only to the cohorts you have created when you or your course team manually adds them. A manual assignment strategy makes sense if you want to create cohorts based on some characteristic of your learners. For example, if you want alumni from your
institution to have a particular course experience, you can create an alumni cohort and manually assign learners who you know are alumni to that cohort.

You can use a :ref:`hybrid assignment method<Hybrid Assignment>` by creating a combination of automated and manual cohorts.

.. note:: You can add learners manually to any cohort, whether it was created as an automated cohort or a manual cohort.

.. note:: Although you can change the assignment method of a cohort at any time after you create it, you should have a cohort assignment strategy in mind as you design your course, and only make changes to cohorts while the course is running if absolutely necessary. Be aware of the implications of changing cohort configuration while your course is running. For more information, see :ref:`Altering Cohort Configuration`. In general, to provide learners with a consistent experience throughout the course run, do not change cohort configuration or a learner's cohort assignment after your course begins.

For use cases and examples of the strategies for assigning learners to cohorts, see the following topics.

* :ref:`All Automated Assignment`

* :ref:`All Manual Assignment`

* :ref:`Hybrid Assignment`

* :ref:`Default Cohort Group`

.. _All Automated Assignment:


Automated Assignment: Making MOOC Discussions Manageable
========================================================

In very large courses, the number of posts that are made to course discussion topics can make for a daunting amount of daily reading. In such courses, dividing the enrollees into separate cohorts makes the volume of posts, responses, and comments by the members of each cohort more manageable, and is more likely to foster community feeling.

If you use the automated assignment strategy, you create several "auto" (automated) cohorts. Learners are automatically and randomly assigned to one of the auto cohorts when they first view any course content on the **Course** or
**Discussion** page. In this way, each learner who engages with the course content or its discussion community is assigned to a cohort. No learner who participates in these ways remains unassigned.

The following guidelines are based on the experiences of MOOC teams that have used cohorts in this way. They are suggested to help you determine how many automated cohorts to define for your course.

* Each cohort should be large enough to inspire lively participation and diverse points of view, but small enough to allow a sense of community to develop. Cohorts formed by random assignment tend to be successful if they include between 200 and 500 members.

* For every 10,000 learners who enroll, approximately 200 to 400 learners remain active in the discussions throughout the course run.

* Divide the estimated total enrollment of the course run by 10,000.

* Use the result as the number of automated cohorts to create.

For example, two days before it starts, a course has an enrollment of 80,000 learners. To create small communities within the discussions, the course team enables cohorts and then creates eight automated cohorts. As learners visit the **Discussion** page or view the course content, they are randomly assigned to one of the eight cohorts. In divided discussion topics, learners read and respond only to contributions made by other members of the same cohort.

For more information, see :ref:`Implementing the Automated Assignment Strategy`.

.. _All Manual Assignment:

Manual Assignment: Grouping by Common Characteristics
=====================================================

In  small to medium-sized enrollments courses, known existing commonalities can be used to identify cohorts. An example is a course that enrolls learners from different companies or with different educational backgrounds, or members of alumni or parent groups. When learners are assigned to cohorts on the basis of a characteristic that they share, they can privately
discuss applications for what they are learning and explore resources and ideas that are of particular interest.

To implement this assignment strategy, you identify the "real-world" cohorts that your learners already belong to. You enable cohorts and then create manual cohorts to represent each of the real-world cohorts. You then manually assign each enrolled learner to a cohort. Every learner in your course, including those who enroll after the course starts, must be assigned to a cohort.

.. note:: To ensure that every learner is assigned to a cohort, you can set up a single automated cohort, as described for the :ref:`hybrid assignment strategy<Hybrid Assignment>`. If you do not create an automated cohort, the system automatically creates a :ref:`default cohort<Default Cohort Group>` and assigns learners to it if necessary.

For more information, see :ref:`Implementing the Manual Assignment Strategy`.

.. _Hybrid Assignment:

Hybrid Assignment: Accommodating Small Groups Within a Course
=============================================================

For some courses, the manual assignment strategy is not feasible to execute, and the automated assignment strategy does not accommodate existing cohorts in the student body. The enrollment might be too large to complete manual assignments effectively, or only some of the learners might have strong defining characteristics among an otherwise diverse student body. For these courses, you can use a hybrid of the two strategies to implement cohorts.

An example is a course that enrolls members of an alumni association. The alumni want an opportunity to have private interactions, so manual assignment of those learners to a cohort makes sense. For other learners in the class, manual assignment is not needed: you can create one or more automated cohorts for the remaining learners in the course.

Before you implement the hybrid strategy, you identify the characteristics that define existing cohorts in the student body. You also decide whether you want the remaining learners in the course to be divided into their own, similarly-sized cohorts, or if you want them all to be in just one other cohort.

After you enable cohorts, you create a manual cohort for each learner group that you identified. You manually assign learners who belong to each group to the corresponding cohort. You also set up automated cohorts for the other learners in the course, or rely on the default automated cohort. Any learners who are not assigned to a manual cohort are automatically assigned to one of the automated cohorts or to the default cohort when they first view any course content, including the course **Discussion** page or content-specific discussion topics. For best results when you use this strategy, you should complete all manual cohort assignments before the course starts and before learners begin viewing course content and discussion topics.

For more information, see :ref:`Implementing the Automated Assignment Strategy` and :ref:`Implementing the Manual Assignment Strategy`.

.. _Default Cohort Group:

Ensuring That All Learners Are Assigned: The Default Cohort
===========================================================

If you enable cohorts in your course, all learners must be assigned to a cohort. To ensure that there are no learners in the course without a cohort, the system automatically creates a default cohort and assigns learners to it if necessary.

The default cohort is created only if you have not created at least one automated assignment cohort in your course by the time that the first learner accesses your course content. Learners who have not been manually assigned to a cohort when they access the course content are automatically assigned to the default cohort.

Learners who are in the default cohort see a cohort name of "Default Group" in discussion posts. If you want learners to see a different name for the default cohort, you can change its name. For details about renaming cohorts, see :ref:`Renaming a Cohort`.

.. image:: /_images/educator_concepts/post_visible_default.png
  :width: 600 px
  :align: center
  :alt: A discussion topic post with "This post is visible to Default Group" above the title.

You can check the :ref:`learner profile information report<View Learner Data>` for your course to see if any learners are assigned to the default cohort, and change their cohort assignments. Note, however, that in divided discussion topics learners can only see posts by members of their currently assigned cohort: when a learner is reassigned, posts that he previously saw will seem to have "disappeared". To avoid negatively affecting the learner experience, any cohort assignment changes should be done as early in the course run as possible, so that learners' views of discussion posts and contributions remain consistent over time.

.. seealso::
 

 :ref:`Manage Course Cohorts` (how-to)

 :ref:`Best Practices for Cohort Assignment Strategies` (reference)


**Maintenance chart**

+--------------+-------------------------------+----------------+--------------------------------+
| Review Date  | Working Group Reviewer        |   Release      |Test situation                  |
+--------------+-------------------------------+----------------+--------------------------------+
|              |                               |                |                                |
+--------------+-------------------------------+----------------+--------------------------------+
