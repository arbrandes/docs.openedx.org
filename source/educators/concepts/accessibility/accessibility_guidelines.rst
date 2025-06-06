.. _Accessibility Guidelines:

#######################################################################
Open edX® Accessibility Guidelines
#######################################################################

.. tags:: educator, concept

Almost one fifth of the world's population has some kind of disability. Online
courses can reduce many barriers to education for these learners by providing
access to courses from any location, at any time, and through the use of
assistive technologies.

The Open edX project is dedicated to creating a platform that is not only itself accessible,
but also enables course content creators to create accessible content. If you
encounter platform issues that you believe might affect your ability to
provide accessible course content, please post on the `Open edX forums`_
for advice. However, for clarity, please note that use of Open edX authoring
tools does not ensure that your course content will be accessible.

It is highly recommended that you implement the best practices in this document
and in other resources. If you cannot easily address any of these barriers to
providing accessible course content, it is recommended that you consult with
resources at your organization such as Disability Services, or assistive
technology and accessibility specialists.

************************
Who Are Our Learners?
************************

In the following sections, we provide guidance on creating and delivering
course content that allows learners to use built-in accessibility
functionality (such as text-to-speech and magnification features), assistive
technologies, and alternative formats. These practices consider learners with
diverse needs, such as:

* Blind learners who use a screen reader, which reads page text aloud, or a
  Braille display device, which renders page text in refreshable Braille.

* Low-vision learners who use screen magnification software to enlarge or
  modify the contrast of text and other onscreen content.

* Learners with vision impairments, such as difficulty seeing in low-light
  conditions, who modify their browser or operating system to change
  background colors and text settings to make text easier to read.

* Learners with learning disabilities, such as dyslexia, who use text-to-
  speech technology that reads page content aloud.

* Physically disabled learners who control their computers using switching
  devices, voice recognition software, or eye gaze-activated technology
  instead of mouse devices or keyboards.

* Learners who modify their operating system settings to make the mouse or
  keyboard easier to use.

* Learners with hearing impairments who cannot access audio content and need
  the equivalent information in an alternative format, such as captions.

**********************************
Open edX® Accessibility Standards
**********************************

As the Open edX® platform is strongly based on well-accepted `HTML5 markup standards <https://html.spec.whatwg.org/>`_ and `WAI-ARIA <https://www.w3.org/WAI/standards-guidelines/aria/>`_, we expect that learners who require additional accessibility tools such as screen readers and screen magnifiers will enjoy strong compatibility.

In addition, our guidance is based on principles of `universal
design <https://en.wikipedia.org/wiki/Universal_design>`_ (usable by all, to the greatest extent possible, without the need for
adaptation or specialized design) and `Universal Design for Learning (UDL) <https://en.wikipedia.org/wiki/Universal_Design_for_Learning>`_. Course teams who build courses based on these principles create an inclusive experience that considers the diverse set
of learning styles and needs of all learners, including learners with
disabilities, learners whose native language is not English, and learners with
technical issues such as low bandwidth internet or no access to audio.

To supplement the
accessibility of the materials you can create within the platform, engage with any available
resources at your institution to support learners with disabilities.
These trained professionals typically provide the following services, which may be equally applicable to courses that are taught online:

* Help with making disability accommodation decisions and advise you on what accommodations may be appropriate in light of the goals of the course and the instructional methodologies employed.

* Help with `document accessibility remediation <https://helpx.adobe.com/acrobat/using/create-verify-pdf-accessibility.html>`_

* For live events, they can help with sourcing providers for learners' `real-time captioning <https://www.nad.org/resources/technology/captioning-for-access/communication-access-realtime-translation/>`_, `signed-language interpretation <https://en.wikipedia.org/wiki/Language_interpretation#Sign_language>`_, or `cued speech transliteration <https://en.wikipedia.org/wiki/Cued_speech>`_ needs.

************************************
Additional Accessibility Resources
************************************

The following resources might also assist you in producing accessible course
content.

* `User Agent Accessibility Guidelines (UAAG) <https://www.w3.org/WAI/standards-guidelines/uaag/#user-agent-accessibility-guidelines-uaag>`_ may be useful if you're intending to implement a browser or browser extension that will be compatible with the Open edX® platform.
* `Authoring Tool Accessibility Guidelines (ATAG) <https://www.w3.org/WAI/standards-guidelines/atag/#atag>`_ guides efforts to make Studio more accessible.
* `HTML5 <https://html.spec.whatwg.org/>`_ and `WAI-ARIA (Accessible Rich Internet Applications) <https://www.w3.org/WAI/standards-guidelines/aria/#introduction>`_ are the standards to help ensure that the platform is accessible. You should follow the same standards to ensure that learner content inside `XBlocks <https://github.com/openedx/xblock-sdk>`_ (learning units) is accessible.
* `EPUB 3.0 <http://idpf.org/epub/30>`_ is a format for ensuring that redistributable learning materials are accessible, though `Adobe PDF <https://www.adobe.com/accessibility/pdf/pdf-accessibility-overview.html>`_, `Microsoft Office <https://www.microsoft.com/en-us/accessibility/microsoft-365?activetab=pivot_1%3aprimaryr2>`_, and `Google Docs <https://support.google.com/docs/answer/6199477?hl=en>`_ may also be made accessible.
* The `DAISY Consortium <http://www.daisy.org/>`_ contributes to EPUB accessibility standards and has a tool for checking EPUB document accessibility.
* `MathML <http://www.w3.org/Math/>`_ is a preferred markup format for all math content.
* `MathJax <https://www.mathjax.org>`_ is the system used within the Open edX platform for rendering MathML content.
* `WCAG2ICT <http://www.w3.org/WAI/standards-guidelines/wcag/non-web-ict/>`_ covers non-web Information and Communications Technologies.

While your ability to support students in the MOOC context might be different
from supporting on-campus students, we encourage you to develop a plan to
respond to students who inform you of accessibility barriers to learning.
However, given the large numbers of learners enrolling in many of the courses,
you will quickly see how important it is to proactively address accessibility concerns
when creating a course.

.. seealso::

 :ref:`Designing for Mobile` (concept)

 :ref:`Accessibility Best Practices Checklist` (reference)

**Maintenance chart**

+--------------+-------------------------------+----------------+--------------------------------+
| Review Date  | Working Group Reviewer        |   Release      |Test situation                  |
+--------------+-------------------------------+----------------+--------------------------------+
| 2025-03-02   | Sarina Canelake               | Sumac          | Pass                           |
+--------------+-------------------------------+----------------+--------------------------------+
