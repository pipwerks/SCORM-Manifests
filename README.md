# SCORM-Manifests
Boilerplate SCORM Manifests for SCORm 1.2 and 2004

*Intended to be used for single-SCO courses.*

The supporting SCORM schemas have been placed into subfolders to help declutter the root of your course ZIP package, as described here: https://pipwerks.com/2014/02/17/clean-out-the-root-of-your-scorm-2004-package/

To use the templates, update the variables inside the manifests as needed.

 * Change `identifier="CourseIDHere"` to whatever course ID you desire.
 * Change `version="1"` to the appropriate version identifier for your course. Typically a number, but a string is acceptable.
 * Change `<organizations default="course-code-here">` to your course code. This is typically the code that the LMS will display after importing the course.
 * Change `<organization identifier="course-code-here">` to match `<organizations default="course-code-here">`
 * Change both `<title>Course Title here</title>` nodes to use the appropriate title for your course. Why two? If you were creating a multi-SCO course, you'd use different titles for each SCO. Since this template is intended for a single-SCO course, you just use the same title in both locations.

These templates assume your course's initial file is index.html, located in the root of the course's ZIP package. If your course uses anything other than index.html, or if the initial file is in a subfolder (such as `content/`), you will need to update the href attributes in `<resource identifier="resource_1" type="webcontent" adlcp:scormtype="sco" href="index.html">` and `<file href="index.html" />` to point to the appropriate file.