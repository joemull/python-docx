# Contributor’s guide

## Project vision

## Learning the codebase

1. Choose a point of entry. This could be a document feature, like tables,
   or a Word feature, like tracked changes. Just so long as it is
   something you are motivated by.

2. Find and read any analysis documentation about it. These documents were
   produced to elucidate the often labyrinthine Office Open XML standard
   and the opaque Visual Basic for Applications (VBA) API.

3. Find and read any acceptance tests related to it. These are the test
   files ending in `.feature` in `/features/`. They are written in Gherkin
   and belong to the [behavioral driven development
   philosophy](https://open.nytimes.com/no-code-no-problem-writing-tests-in-plain-english-537827eaaa6e).
   Notice how the acceptance tests draw out generalised use cases, using
   [declarative
   language](https://en.wikipedia.org/wiki/Declarative_programming),
   treating python-docx like a black box.

4. Find and read any unit tests related to it. These are in `/tests/` and
   are written in `pytest` style. This is where you can begin to piece
   together how python-docx takes each step required to achieve the goals
   declared in the acceptance tests.

5. Find and read the code related to it. Trace the object relationships to
   see how the proxy objects fit together with the element classes. Get
   used to common dynamic property name prefixes and suffixes such as
   `lst` in `gridCol_lst`.

## Writing

1. Identify the gap between the bugfix or feature you have in mind and the
   current python-docx codebase. This could extend all the way from
   acceptance test to code, or it could just be code, or something in
   between.

2. Get to work at the highest level document that does not yet exist. This
   would be an analysis document for a new feature, or an acceptance test
   for a new behavior that is not yet offered or not working as called for
   by a common use case. Submit analysis documents for peer review before
   starting on testing or coding.

3. Once a maintenance document exists that the maintainers accept, you are
   ready to write acceptance tests. Then write unit tests and code until
   all the tests are passing.

4. Submit code for peer review.
