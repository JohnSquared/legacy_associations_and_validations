# Legacy Associations and Validations

## Description

Take an existing legacy codebase with no associations or validations and add them.

## Normal Mode

Given existing code we added associations and validations to it. The two people on our team did each of the following tasks while adding tests along the way to our test suite (test.rb) to make sure each new association/validation was correct.

### John Buscemi:
* Associate `schools` with `terms` (both directions).
* Associate `terms` with `courses` (both directions).  If a term has any courses associated with it, the term should not be deletable.
* Associate `courses` with `course_students` (both directions).  If the course has any students associated with it, the course should not be deletable.
* Associate `assignments` with `courses` (both directions).  When a course is destroyed, its assignments should be automatically destroyed.
* Set up a School to have many `courses` through the school's `terms`.
* Validate that Lessons have `names`.
* Validate that Readings must have an `order_number`, a `lesson_id`, and a `url`.
* Validate that the Readings `url` must start with `http://` or `https://`.  Use a regular expression.
* Validate that Courses have a `course_code` and a `name`.
* Validate that the `course_code` is unique within a given `term_id`.
* Validate that the `course_code` starts with three letters and ends with three numbers.  Use a regular expression.

### John Greiner:
* Associate `lessons` with `readings` (both directions).  When a lesson is destroyed, its readings should be automatically destroyed.
* Associate `lessons` with `courses` (both directions).  When a course is destroyed, its lessons should be automatically destroyed.
* Associate `courses` with `course_instructors` (both directions).  If the course has any students associated with it, the course should not be deletable.
* Set up a Course to have many `readings` through the Course's `lessons`.
* Validate that Schools must have `name`.
* Validate that Terms must have `name`, `starts_on`, `ends_on`, and `school_id`.
* Validate that the User has a `first_name`, a `last_name`, and an `email`.
* Validate that the User's `email` is unique.
* Validate that the User's `email` has the appropriate form for an e-mail address.  Use a regular expression.
* Validate that the User's `photo_url` must start with `http://` or `https://`.  Use a regular expression.
* Validate that Assignments have a `course_id`, `name`, and `percent_of_grade`.
* Validate that the Assignment `name` is unique within a given `course_id`.
