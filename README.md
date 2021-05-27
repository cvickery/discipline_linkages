# Linking Disciplines

The goal of this project is to determine the set of disciplines that are related to an academic
program. These relationships are important for selecting course articulation rules that a person
will review for accuracy and applicability to the target program.

This project explores possible ways to relate academic programs (majors, concentrations, and minors)
with course disciplines using information available in CUNY‘s PeopleSoft Student Information System,
known as CUNYfirst. That information includes college-specific discipline names, CUNY-wide
discipline names, CIP codes, and HEGIS codes, which are explained next.

## Terminology

  - CUNY has nineteen colleges that offer undergraduate degrees. They are called *institutions* in
  CUNYfirst.

  - Colleges are generally organized with various divisions or schools. They are called *academic
    groups* in CUNYfirst.

  - Each school or division houses one or more academic departments. Departments are called
    *academic organizations* in CUNYfirst.

  - Departments offer courses in one or more disciplines. Disciplines are called *subjects* in
  CUNYfirst.

  - ”Similar disciplines” (a tricky term for this project) are often named differently across CUNY.
  Each discipline in each department at each college is assigned a CUNY-wide discipline name, which
  is called the *external subject area* in CUNYfirst. I don’t know how these names were assigned,
  but, looking at them, they seem to have face validity.

## Taxonomies

There are two taxonomies for classifying academic disciplines in use at CUNY. The US Department of
Education’s [CIP](https://nces.ed.gov/ipeds/cipcode/) and the NYS Department of Education’s
[HEGIS](http://www.nysed.gov/college-university-evaluation/new-york-state-taxonomy-academic-programs-hegis-codes).
Both use six-digit numeric codes in which successive pairs of digits indicate finer and finer levels
of detail within the taxonomy. CIP codes are a structured in a somewhat more convenient way for our
purposes, with separate names for each pair of digits. For example:

 CIP Code | Name
 ---------| ---------------------------------------------------------------
 01       | AGRICULTURAL/ANIMAL/PLANT/VETERINARY SCIENCE AND RELATED FIELDS.
 01.01    | Agricultural Business and Management.
 01.0101  | Agricultural Business and Management, General.
 01.0102  | Agribusiness/Agricultural Business Operations.


In CUNYfirst, each program (major, minor, concentration) is assigned both a CIP Code and a HEGIS
Code. Likewise, college-specific disciplines are assigned both CIP and HEGIS codes. However, the
CUNY-wide discipline names do not have CIP or HEGIS codes explicitly associated with them.

## The Problem

The [Transfer Explorer ](https://explorer.cuny.edu) website (“T-Rex”)includes the ability to see how
courses transfer across CUNY. Faculty, advisors, and administrators who are interested in seeing how
courses in particular disciplines transfer can select a set of sending and receiving colleges, and
then tell what disciplines they are interested in. The system then filters the 1.4 million course
articulation rules in CUNYfirst to display a list showing how all courses matching the user’s
selection transfer.

Because disciplines are named differently at different colleges, selecting “disciplines of interest”
is based on matching cuny-wide discipline names. The user sees the CUNY-wide name and, for each
college, the matching college-specific discipline names. This procedure works very well in practice,
but there are some issues.

  - It’s not always obvious what CUNY-wide disciplines to select. For example, a Studio Art program,
  might offer photography courses, but users might not think to filter using both the CUNY-wide
  *Art Studio* and *Photography* disciplines to find all matches.

  - There are ambiguities in assigning CUNY-wide discipline names to college-specific discipline
    names. For example, LaGuardia’s Math Deprtment has three disciplines that it calls “Mathematics,
    Engineering, and Computer Science,” all of which use the same CUNY-wide discipline name of
    *MATH*. But the three disciplines have different acronyms: MAC, MAE, and MAT, and the titles of
    courses offered under those acronyms indicate that MAC courses are computer science, MAE are
    engineering math, and MAT are pure math courses. Someone looking at how computer science courses
    transfer from LaGuardia to other colleges would have to know enough to select the CUNY-wide Math
    discipline name, but then they would be faced with all the engineering and pure math courses as
    well as the computer science courses they are interested in. Oh, and the user would need to know
    enough use the CUNY-wide Computer Science discipline name the courses in LaGuardia’s “Business
    and Technology” discipline.

Note that users (primarily students) who are interested in courses in a particular discipline at a
particular college have an alternate way to locate courses of interest in T-Rex. The issue at hand
primarily affects faculty, advisors, and administrators selecting transfer rules to review rather
than information about particular courses.

## The Premise

There might be a way to find transfer rules that need to be reviewd by improving on CUNY-wide
discipline names as the only information used for selecting courses. Specifically, CIP and/or HEGIS
codes might provide a way to relate disciplines based on the similarity of taxonomic positions.

At first look, the approach doesn’t work in a simple way. For example, the CIP codes for the
computer-related courses at LaGuardia are in totally different parts of the taxonomy for the
Business and Math departments' offerings. It’s possible, however, that we may be able to do a
meta-analysis of CIP and/or HEGIS codes to find groupings that would be useful.

