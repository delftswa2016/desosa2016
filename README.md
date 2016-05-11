# Delft Students on Software Architecture: DESOSA 2016


**[Arie van Deursen], [Maurício Aniche] and [Joop Aué].**<br/>
*Delft University of Technology, The Netherlands, May 11, 2016, Version 1.0*

[arie van deursen]: https://avandeursen.com
[maurício aniche]: https://github.com/mauricioaniche
[joop aué]: https://github.com/joopaue

We are proud to present
_Delft Students on Software Architecture_, a collection of 21 architectural descriptions of open source software systems written by students from Delft University of Technology during a [master-level course][in4315] taking place in the spring of 2016.

[in4315]: http://www.studiegids.tudelft.nl/a101_displayCourse.do?course_id=35212

In this course, teams of 3-4 students could adopt a project of choice on GitHub. The projects selected had to be sufficiently complex and actively maintained (one or more pull requests merged per day). The systems are from a wide range of domains, including web development ([Ember], [D3], [Ruby on Rails][rails]), machine learning ([TensorFlow]), music ([SonicPi]), and gaming ([Terasology]).

[ember]: http://emberjs.com/
[d3]: https://d3js.org/
[rails]: http://rubyonrails.org/
[tensorflow]: https://www.tensorflow.org/
[sonicpi]: http://sonic-pi.net/
[terasology]: http://terasology.org/

During a 10 week period, the students spent one third of their time on this course, and engaged with these systems in order to understand and describe their software architecture.

Inspired by Brown and Wilsons' [Architecture of Open Source Applications][aosa], we decided to organize each description as a chapter, resulting in the present online book.

This book is the second in volume the DESOSA series: The [first DESOSA book][desosa2015] resulted from the 2015 edition of the course, and contained architectural descriptions of ten (different) open source systems.

[desosa2015]: https://delftswa.github.io/

## Recurring Themes

The chapters share several common themes, which are based on smaller assignments the students conducted as part of the course. These themes cover different architectural 'theories' as available on the web or in textbooks. The course used  Rozanski and Woods' [Software Systems Architecture][rw], and therefore several of their architectural [viewpoints] and [perspectives] recur.

[viewpoints]: http://www.viewpoints-and-perspectives.info/home/viewpoints/
[perspectives]: http://www.viewpoints-and-perspectives.info/home/perspectives/

The first theme is outward looking, focusing on the use of the system. Thus, many of the chapters contain an explicit [stakeholder analysis], as well as a description of the [context] in which the systems operate. These were based on available online documentation, as well as on an analysis of open and recently closed issues for these systems.

[context]: http://www.viewpoints-and-perspectives.info/home/viewpoints/context/
[stakeholder analysis]: http://www.mindtools.com/pages/article/newPPM_07.htm

A second theme involves the [development viewpoint][development], covering modules, layers, components, and their inter-dependencies. Furthermore, it addresses integration and testing processes used for the system under analysis, and often includes an assessment of the presence of technical debt.

[development]: http://www.viewpoints-and-perspectives.info/home/viewpoints/

A third recurring theme is _variability management_. Many of today's software systems are highly configurable. In such systems, different features can be enabled or disabled, at compile time (flags) or at run time (toggles). Using techniques from the field of [product line engineering][fospl], several of the chapters provide feature-based variability models of the systems under study.

## First-Hand Experience

Last but not least, the chapters are also based on the student's experience in actually contributing to the systems described. As part of the course over 75 pull requests to the projects under study were made, including refactorings ([Ember 13088], [Rails 24198]), bug fixes ([Terasology 2235]), new features ([Karma 1983]), test cases ([Sonic-Pi 1054]), translations ([OpenTripPlanner 2232]), and documentation ([OpenCV 4375]).
Many projects had issues explicitly marked as "good for new contributors", making it easier for students to find a good starting point.

[Karma 1983]: https://github.com/karma-runner/karma/pull/1983
[Ember 13088]: https://github.com/emberjs/ember.js/issues/13088
[Terasology 2235]: https://github.com/MovingBlocks/Terasology/pull/2235
[Rails 24198]: https://github.com/rails/rails/pull/24198
[Sonic-Pi 1054]: https://github.com/samaaron/sonic-pi/pull/1054
[OpenCV 4375]: https://github.com/Itseez/opencv/issues/4375
[OpenTripPlanner 2232]: https://github.com/opentripplanner/OpenTripPlanner/pull/2232

Through these contributions the students often interacted with lead developers and architects of the systems under study, gaining first-hand experience with the architectural trade-offs made in these systems.

## Feedback

While we worked hard on the chapters to the best of our abilities, there will be plenty of omissions and inaccuracies.
We value your feedback on any of the material in the book. For your feedback, you can:

* Open an issue on our [GitHub repository for this book][dswa.io].
* Offer an improvement to a chapter by posting a pull request on our [GitHub repository][dswa.io].
* Contact @[delftswa][dswa.tw] on Twitter.
* Send an email to Arie.vanDeursen at tudelft.nl.

[dswa.io]: https://github.com/delftswa2016/desosa2016/
[dswa.tw]: https://twitter.com/delftswa


## Acknowledgments

We would like to thank:

* Our guest speakers: Alex Nederlof, Felienne Hermans, Johan den Haan, Tobias Kuipers, Huub Bakker, Hans van Dongen, Daniele Romano, Maikel Lobbezzo.
* [Valentine Mairet] who created the front cover of this book.
* Michael de Jong and Alex Nederlof who were instrumental in the earlier editions of this course.
* All open source developers who helpfully responded to the students' questions and contributions.
* The excellent [gitbook toolset] and [gitbook hosting] service making it easy to publish a collaborative book like this.

[gitbook toolset]: https://github.com/GitbookIO/gitbook-cli
[gitbook hosting]: https://www.gitbook.com/

[Valentine Mairet]: https://github.com/valmai

## Further Reading

1. Arie van Deursen, Alex Nederlof, and Eric Bouwers. Teaching Software Architecture: with GitHub! [avandeursen.com][teaching-swa], December 2013.
2. Nick Rozanski and Eoin Woods. [Software Systems Architecture: Working with Stakeholders Using Viewpoints and Perspectives][rw]. Addison-Wesley, 2012, 2nd edition.
3. Sven Apel, Don Batory, Christian Kästner, Gunter Saake. [Feature-Oriented Software Product Lines: Concepts and Implementation][fospl]. Springer-Verlag, 2013.
4. Eric Bouwers. [Metric-based Evaluation of Implemented Software Architectures][bouwers]. PhD Thesis, Delft University of Technology, 2013.
5. Amy Brown and Greg Wilson (editors). [The Architecture of Open Source Applications][aosa]. Volumes 1-2, 2012.
6. Arie van Deursen and Rogier Slag (editors). Delft Students on Software Architecture: DESOSA 2015. [delftswa.github.io][desosa2015], 2015.

[teaching-swa]: http://avandeursen.com/2013/12/30/teaching-software-architecture-with-github/
[rw]: http://www.viewpoints-and-perspectives.info/
[aosa]: http://aosabook.org/
[fospl]: http://link.springer.com/book/10.1007/978-3-642-37521-7
[bouwers]: http://repository.tudelft.nl/view/ir/uuid:6b65c5f5-398c-4a41-8806-31c638b1891c/


## Copyright and License

The copyright of the chapters is with the authors of the chapters. All chapters are licensed under the [Creative Commons Attribution 4.0 International License][cc-by].
Reuse of the material is permitted, provided adequate attribution (such as a link to the corresponding chapter on the [DESOSA book site][desosa]) is included.

Cover image credits: 
TU Delft library, TheSpeedX at [Wikimedia](https://commons.wikimedia.org/wiki/File:Library_TUDelft.jpg); 
Owl on [Emojipedia Sample Image Collection](http://emojipedia.org/emojipedia/sample-images) at [Emojipedia](http://emojipedia.org/emojipedia/sample-images/owl);
Feathers by [Franco Averta](http://www.flaticon.com/authors/franco-averta) at [Flaticon](http://flaticon.com).


[![Creative Commons](img/cc-by.png)][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[desosa]: https://www.gitbook.com/book/delftswa/desosa2016/details
