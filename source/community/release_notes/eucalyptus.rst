.. _Open edX Eucalyptus Release:

Open edX Eucalyptus Release
###########################

This page lists the highlights of the Eucalyptus release.

.. toctree::
   :hidden:

   bulk_email
   CSMHE/index

.. contents::
 :depth: 1
 :local:

New Features
************

The following new features are included in the Open edX Eucalyptus release.

.. contents::
 :depth: 1
 :local:

Self-Paced Course Configuration
===============================

When course teams create a course, they can now select the way a course is
delivered to learners. You can set a schedule for the course, including due
dates for assignments or exams, or you can specify that the course is
self-paced, which allows learners to work at their own pace.

Subsection Prerequisites
========================

Course teams can now control the visibility of subsections based on the scores
that learners earn in other subsections. This feature prevents learners from
viewing content before they earn a minimum score for previous content.

Course Navigation
=================

Several changes have been made to navigation options in the LMS.

* The **Home** page replaces the **Course Info** page. The **Home** page
  appears first among the page navigation options, and opens automatically when
  a learner selects a course on the learner dashboard. This page now includes
  important course dates in addition to course updates and course handouts.

* **Course** is the new name for the **Courseware** page. This page appears
  after **Home** among the page navigation options.

* Learners can now use the left and right arrow buttons at the ends of the unit
  navigation bar to move to the previous unit or the next unit.

Teams
=====

With the teams feature, a learner can browse a list of topics, and then create
a team and invite other learners to take part in group activities relating to
one of the topics. Team activities provide opportunities for small group
interactions and projects in your course.

Bookmarks
=========

The bookmarks feature allows a learner to add a bookmark to any unit in the LMS
so that the page can be found later on the **My Bookmarks** page.

Drag and Drop Problem XBlock
============================

A new, mobile-ready and accessible drag and drop problem type is now available.
This version replaces the original drag and drop problem type, which is now
deprecated.

Peer Instruction XBlock
=======================

The peer instruction tool emulates the classroom experiences of the Peer
Instruction learning system. A multiple choice question gives online learners
an opportunity to review the answers, and rationales, provided by other course
participants, and arrive at a deeper understanding of concepts.

Completion XBlock
=================

The completion XBlock adds a toggle control that allows learners to mark the
associated section of course content as complete.

CourseTalk for Course Reviews
=============================

The CourseTalk widget allows learners to post course ratings and reviews that
then appear on the course's **About** page. When you add the CourseTalk widget
to an Open edX instance, the widget is enabled for every course on that
instance.

Configurable Data Storage Services
==================================

Instead of specifically referencing the Amazon S3 service for data storage and
retrieval, the Open edX platform now uses the Django file storage API. In
addition to S3, you can now configure an OpenStack Swift Object Store as the
cloud storage provider for certain system features.


Themes for Multiple Sites
=========================

With this release, it is now possible to configure themes for multiple sites in
a single installation of the Open edX platform.


Staff Grading Options for Open Response Assessments
===================================================

This release adds the following options for course teams to grade learner
responses in open response assessments.

* In Studio, course teams can now include a staff assessment step as part of
  the assignment. For a staff assessment, a member of the course team uses the
  rubric to evaluate every response submitted by a learner .

* In the LMS, course teams can now override the grade that an individual
  learner received. To do so, a member of the course team uses the rubric to
  evaluate the learner's response. The learner's grade for the assignment is
  updated to the grade that results from the staff assessment.

Learner ORA Response Report
===========================

A new report is available for ORA assignments that includes each learner's
response, assessment details and scores, the final score for the assignment,
and any feedback provided by the learner about the peer assessment process.

Updates to E-Commerce Checkout
==============================

This release includes updates to the user interface on the **Checkout** page
that is presented by the edX e-commerce service. The functionality of this
page has not changed, and learners can continue to check out using their credit
cards or PayPal.

Badges for Custom Course Events
===============================

Open edX instances can now create and award badges to learners for certain
milestone achievements. Example achievements include enrolling in a certain
number of courses, completing a certain number of courses, or completing a
specific set of courses.

Updates to Course Discussions
=============================

This release includes the following changes to course discussions.

* When learners upload images and links in discussion posts, they can now
  include descriptions of the images or links. These descriptions are the
  accessible text descriptions of the uploaded material, and are required
  unless learners indicate that an image is decorative only.

* In course discussions, learners can no longer vote for or report their own
  posts.

* Previously, the course **About** page included an unnecessary heading labeled
  **overview**. This release removes the **overview** heading.

* The LMS now supports internationalization and localization of static user
  interface text in XBlocks.

* Learners must now enter or select an answer before they can use **Check** or
  **Final Check** to find out if their answers are correct. This change applies
  to checkbox, dropdown, multiple choice, and text, numerical, or math
  expression input problems.

* In the LMS unit navigation bar, only the unit display name now appears or is
  read when learners move the pointer over a unit icon. Previously, the display
  names of the unit and all of its components appeared or were read.

* The student profile report now includes columns for city and country.

* Course teams can now send bulk email messages to one or more of the cohorts
  in their courses.

* Studio now has a setting that course teams can use to keep timed exams hidden
  after the exam due date has passed. In the LMS, course team members who view
  the course as a specific learner see the timed exam content even if the exam
  is hidden.

* System administrators can now add custom fields to the registration page for
  their Open edX instances. Fields can be of different types, including
  dropdown and text entry.

Updates to Bulk Email
=====================

The way the bulk email feature is enabled and disabled has changed, see
:doc:`bulk_email` for more details.

Updates to Analytics Events and Database Tables
***********************************************

.. contents::
 :depth: 1
 :local:

Changes to ``courseware_studentmodulehistory`` Table
====================================================

There were significant changes to how we manage the
``courseware_studentmodulehistory`` table in the LMS and CMS.  Please see
:doc:`CSMHE/index` for more information.

New Non-Certificate Statuses
============================

The ``audit_notpassing`` and ``audit_passing`` statuses have been added to the
``certificates_generatedcertificate`` table.

* ``audit_notpassing`` applies to learners who did not earn a passing grade and
  who have a value of "audit" in ``student_courseenrollment.mode``.

* ``audit_passing`` applies to learners who earned a passing grade and
  who have a value of "audit" in ``student_courseenrollment.mode``.

No certificate is generated for learners who have either of these statuses.
Learners who are enrolled in the audit track see a message on the **Progress**
page that indicates that the audit track does not include a certificate.

New and Updated Video Player Events
===================================

Changes to the video player's controls resulted in the following new and
updated events.

* The button that shows or hides a transcript file on the right of the video
  was relabeled from CC to ``"``. The video player emits the existing
  ``show_transcript``/ ``edx.video.transcript.shown`` and ``hide_transcript``/
  ``edx.video.transcript.hidden`` events when users interact with this control.

* A button labeled CC was added to show or hide closed captions. The video
  player emits new events, ``edx.video.closed_captions.shown`` and
  ``edx.video.closed_captions.hidden``, when users interact with this control.

* A menu for selecting a different language for the transcript and closed
  captions was added. The video player emits the existing
  ``video_hide_cc_menu`` and ``video_show_cc_menu`` when users interact with
  this control. In addition, these events now include ``name`` values of
  ``edx.video.language_menu.hidden`` and ``edx.video.language_menu.shown``,
  respectively, and the ``video_hide_cc_menu``/
  ``edx.video.language_menu.hidden`` events include a new ``event`` member
  field, ``language``.

New Events
==========

The following analytics events reflect course navigation actions in the LMS.

* ``edx.ui.lms.link_clicked``
* ``edx.ui.lms.outline.selected``
* ``edx.ui.lms.sequence.next_selected``
* ``edx.ui.lms.sequence.previous_selected``
* ``edx.ui.lms.sequence.tab_selected``

The following analytics events have been added for the new drag and drop
problem XBlock.

* ``edx.drag_and_drop_v2.feedback.closed``
* ``edx.drag_and_drop_v2.feedback.opened``
* ``edx.drag_and_drop_v2.item.dropped``
* ``edx.drag_and_drop_v2.item.picked_up``
* ``edx.drag_and_drop_v2.loaded``

The following analytics events have been added for the bookmarks feature.

* ``edx.bookmark.accessed``
* ``edx.bookmark.added``
* ``edx.bookmark.listed``
* ``edx.bookmark.removed``

The following analytics events have been added for the notes feature.

* ``edx.course.student_notes.added``
* ``edx.course.student_notes.deleted``
* ``edx.course.student_notes.edited``
* ``edx.course.student_notes.notes_page_viewed``
* ``edx.course.student_notes.searched``
* ``edx.course.student_notes.used_unit_link``
* ``edx.course.student_notes.viewed``

The following events have been added for the staff grading features in open
response assessments.

* ``openassessmentblock.get_submission_for_staff_grading``
* ``openassessmentblock.staff_assess``


Accessibility Updates
*********************

In keeping with edX's commitment to creating accessible content for everyone,
everywhere, the Open edX Eucalyptus release contains numerous accessibility
enhancements and improvements to readability and navigability.

.. contents::
 :depth: 1
 :local:

Video Player
============

The video player now includes closed captions, which are overlaid on the video
while it plays. Users can view closed captions and transcripts separately or at
the same time. Those who choose to view the closed captioning for a video can
drag the captions to a different place on the video. In addition, the video
player now includes accessible labels for every control.

HTML Component Templates
========================

To ensure that all headings on a course page in the LMS are rendered correctly
by screen readers, the Heading 1 and Heading 2 options have been removed from
the HTML component visual editor.
The Heading 3 option remains available, and Heading 4, Heading 5, and
Heading 6 options have been added. All of the examples provided for HTML
component options include headings beginning with Heading 3. This release
also includes styling and scalability changes to the toolbar icons in the HTML
component visual editor.


Other Accessibility Updates
===========================

This release includes a number of improvements to the appearance and
accessibility of controls in the edX LMS.

* When learners who use high contrast mode on their systems select an LMS page
  such as **Course** or **Discussion**, the selected page is now clearly
  distinguishable from the other pages.

* The **Calculator** control has been enhanced so that it appears for learners
  who use high contrast mode on their systems.

* The target of the **Skip to Content** links has been updated so that keyboard
  and screen reader users can more easily navigate to the unique content on
  each page. Screen reader users can now use the ``<main>`` element as a page
  landmark.

* The editing options for circuit schematic builder problems, including the
  tools to cut, copy, paste, and show or hide the grid display, now include
  accessible labels.

* On wiki article pages, the options for an article, including **View**,
  **Edit**, and **Settings**, now appear next to, rather than in, the shaded
  area below the article.

System Upgrades and Updates
***************************


* You can now enable or disable the bulk email feature from the Django
  administration console, rather than editing different configuration files.

  .. important:: As a result of this change, the bulk email feature is disabled
    until you manually re-enable it.

* The OAuth 2.0 provider library has been updated to version 0.5.0. This update
  includes support for the client credentials grant.

* The number of days before OAuth tokens expire for mobile OAuth clients can
  now be configured.

* In this release, Ruby has been removed from the edx-platform repository. As a
  result, the ``prereqs`` paver command no longer installs the prerequisite
  environment for Ruby, and the edxapp user on new instances of Devstack
  no longer has ``rbenv`` in the search path. However, discussion forums use
  Ruby, and the forums user continues to have ``rbenv`` in the search path.

* The jQuery JavaScript library has been updated from version 1.7.2 to version
  2.2.0. To support legacy API calls, this update also adds the JQuery Migrate
  library.

* The JavaScript library Underscore.js has been upgraded to version 1.8.3.

* A number of CoffeeScript files have been converted to JavaScript.

* JavaScript tests are now run using Karma rather than JS-Test-Tool.


Mobile App Updates
******************

The Open edX Eucalyptus release supports versions 2.5.1 (Android) and 2.5.3
(iOS) of the mobile app, and includes the following mobile app features.

* Course discussions are now supported in the mobile app, including content-
  specific discussion topics in course units. Discussions can be viewed in
  landscape mode.

* Course search. Learners can search for courses using keywords, and filter
  courses by subject and availability.

* User profiles. Learners can create and edit limited or full profile
  information in the mobile app. In discussions, selecting the linked username
  of the author of a post takes you to that person's profile page.

* The mobile app now uses refresh tokens. Learners do not have to sign in
  again, even after a token expires.

* Mobile-ready assessments now include the drag and drop and math expression
  input problem types as well as basic assessment types (checkbox, dropdown,
  multiple choice, text input, and numerical input).


Deprecated Features
*******************

Several features are deprecated, or deleted, by the Open edX Eucalyptus
release.

.. contents::
 :depth: 1
 :local:

Deprecated REST APIs
====================

The mobile, course structure, and profile images REST web services are
deprecated.

* Use the ``/api/courses/v1/courses/`` web service instead of the deprecated
  mobile and course structure web services.

* Use the ``/api/user/v1/accounts/`` web service instead of the deprecated
  profile image web service.

Deprecated Tools and Problem Types
==================================

* The randomize component is now deprecated. To provide randomized content in
  your courses, add randomized content blocks to assign problems from a content
  library.

* The original drag and drop problem type is now deprecated. A new mobile-
  ready, accessible drag and drop problem type is available.

Deleted Tools and XModules
==========================

* The graphical slider tool is no longer available.

* The crowdsource hinter XModule is no longer available as a course tool.

* To improve grade calculation performance for the **Progress** page in the
  LMS, support for the ``always_recalculate_grades`` XBlock field has been
  removed.

* The ``ENABLE_JWT_AUTH`` feature flag has been removed.


Patch Releases
**************

2 September 2016: Eucalyptus.2
==============================

* A problem that caused the Django Debug Toolbar to raise a "process() takes
  exactly 3 arguments (2 given)" exception has been fixed.

* Course discussion performance has been improved.

* Learners can now correctly add a comment to a response in inline course
  discussions.

* Links to vertical blocks have been fixed.

* The install_stack.sh file now creates directories differently.


**Maintenance chart**

+--------------+-------------------------------+----------------+---------------------------------------------------+
| Review Date  | Working Group Reviewer        |   Release      |Test situation                                     |
+--------------+-------------------------------+----------------+---------------------------------------------------+
|2025-04-28    | Docs WG                       | Teak           | Deprecated: This is no longer the current release |
+--------------+-------------------------------+----------------+---------------------------------------------------+

