# Using Industry Best Practices in Computer Science Education
A proposed talk by Chris Cannon

## Intended Audience
The intended audience for this talk is CS or other technical educators seeking
strategies that will give their students an edge in the workforce.

## Abstract
Technical educators are tasked with equipping the engineers, developers, and
leaders who will solve the problems faced by generations to come. With this
responsibility in mind, it is absolutely essential that we make the most of the
short time we have with our students. Often, in modern technical education,
students will be receive a solid introduction to the concepts of the topics
covered, without ever solving a problem fully, as they will be tasked with in
the workplace. This skill gap leaves students of good, dedicated teachers, just
short of fully equipped to step into their roles in the workforce.

Therefore, I intend to propose a teaching paradigm that places emphasis on
learning vital foundations of computer science through the best practices
used in the industry. Evaluating problems, specifying a solution, and
implementing that solution in a version controlled, continuously integrated
environment will allow students to understand the power of these tools as they
learn the power of computer science. I will propose workflows manageable for
every experience level, and solutions that any secondary or undergraduate
technical educator can adopt.

Primarily, I will use git, GitHub, Travis-CI, and StarUML as example methods
for bringing these solutions to classrooms. For example:
- Stipulate that a mechanical engineering professor wants to issue a group
project where students are tasked with developing a specification for a part.
This group project will be revised as the semester progresses, and additional
"issues" of the specification will be completed as the students learn.
Demonstrate the difference in collaborating multiple releases of a text-based
file on GitHub, versus making multiple copies on Google Drive, DropBox, or
local solutions.
- Illustrate a CS classroom where professors grade programs by hand, or, by
an automated testing framework that does not provide feedback to students.
Contrast this illustration with a Travis-CI server that provides immediate
build and testing framework in a pull request. Note that the emphasis is now on
student success, and using the tools available in the industry to facilitate
this success, than on student failures only pointed out after the due date.
- Contrast hand-drawn student UML diagrams with specifications from major
companies. Note that teaching students to produce _almost industry-quality_
work enables them to _almost succeed_ in the workforce. Contrast student-
developed StarUML diagrams with industry specifications and note the
similarities in quality.

## Excerpts from "Using Industry Best Practices in Computer Science Education"
"When I say we should be using industry best practices in our classrooms, I
don't mean to say that you should run your class like a business. Our job as
educators is to build up and empower our students, not demand that they produce
for us. Rather, I'm postulating that we _owe_ it to our students to teach them
the tools that make the _most_ sense to get any given job done. GitHub isn't the
largest community of open source projects in the world by mistake, it has grown
so rapidly because it _empowers_ its users to work _better_ together and be as
efficient as possible."

"Industry best practice also means emphasis on standardization, not as an
obstacle to innovation but as a tool for encapsulation and modularity. When
our students spend less time reinventing basic code infrastructure, because we
have taught them how to reuse key building blocks from a well organized code
base, we have more time to teach the advanced concepts that will give our
students an edge in the technical interview."

"Take, for example, COMP 167, Computer Program Design at North Carolina A&T
State University. COMP 167 has a series of what's called 'major programming
assignments'. These assignments address blocks of program design topics at once,
and are intended to test students' ability to integrate skills to produce a
single solution. They work _great_, but recently we made them work even better.
Previously, these programs were submitted to a Teaching Assistant via a .zip
file containing a NetBeans project, not exactly industry best-practice. Grades
were assigned based on 'levels', with each added layer of functionality earning
a student a higher level. However, a student's grade was limited by the first
incomplete level. So, if levels 3-4 were perfect, but level 2 was accidentally
incomplete, a student would only get about a 40 out of 100. We decided there was
a better way to approach this problem. Now, as students work through their
assignment, they make a new branch in a GitHub Classroom assignment for each
level. Additionally, after completing each level, students submit a pull
request. This gives the Teaching Assistants the ability to give constructive
feedback _as the students complete their work_, just like they could receive in
the workplace. Additionally, an approved pull request confirms that a student
receives full marks for a given branch, so much of the surprise is taken out of
grading. This industry-mimicking approach gives students more opportunities to
succeed, and more opportunities to learn as they complete an assignment because
the Teaching Assistants can watch which parts the students struggle with and
give immediate feedback."
