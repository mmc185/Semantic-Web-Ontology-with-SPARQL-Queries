# Semantic Web: Ontology with SPARQL Queries

<img src="utilities/unipi-logo.png" height="256" align="right"/>

Project for the <i>Semantic Web</i> course (657AA), <i>University of Pisa</i>, consisting in the creation of an <b>OWL 2 DL ontology</b> using the <b>RDF Turtle notation</b>, and performing some queries using the <b>SPARQL</b> language.

## Ontology Definition

The fundamental concepts in the domain related to an Italian research organisation are: _employees_, _institutes_, _laboratories_ and _research groups_. Some of the facts that characterise this domain can
be stated as follows:
1. An employee is a person who has exactly one contract with the research organisation.
2. An employee can be a researcher, a technologist, a graduate fellow, a postdoctoral fellow or a
member of the administrative staff.
3. A researcher can be a young researcher, a senior researcher or a director.
4. Each employee has a unique ID (an positive integer).
5. A research organisation has three types of subparts: institute, laboratory and research group. The
research organisation consists of more than one institute, each institute consists of more than one
laboratory, and each laboratory consists of at least one research group.
6. Each institute, each laboratory and each research group have exactly one name (a string).
7. Each institute is identified by an ID number (a positive integer) and the date of its creation.
8. Each institute has exactly one institute director.
9. Each researcher, technologist, graduate fellow or postdoctoral fellow is member of exactly one
laboratory and exactly one research group.
10. Each institute has one or more buildings. Each building has exactly one location. Each building
contains more than one office.
11. Each employee has exactly one office. Each office hosts one or more employees.
12. Research organisation, employee, institute, laboratory, research group, building, location and office
are pairwise disjoint concepts.

## Tasks
1. Declare the required classes, providing for each class a textual label and a concise textual description of the intension of the class, using the appropriate annotation properties from the RDF Schema vocabulary
2. Provide the sub-class axioms defining the class taxonomy
3. Declare the required object properties, providing for each property: <br>
  &nbsp;  3.1 a textual label, using the appropriate annotation property from the RDFS vocabulary <br>
&nbsp; 3.2. a textual description of the intension of the property, using the appropriate annotation property from the RDFS vocabulary <br>
 &nbsp;   3.3. one axiom defining the domain of the property <br>
 &nbsp;   3.4. one axiom defining the range of the property <br>
 &nbsp;   3.5. one axiom defining the inverse of the property <br>
 &nbsp;   3.6. any additional axioms expressing disjointness of the property with other object properties, and the property characteristics. <br>
4. Provide the sub-property axioms defining the object property taxonomy
5. Declare the required data properties, providing: <br>
&nbsp; 5.1. a textual label, using the appropriate annotation property from the RDFS vocabulary <br>
&nbsp; 5.2. a textual description of the intension of the property, using the appropriate annotation property from the RDFS vocabulary  <br>
&nbsp; 5.3. one axiom defining the domain of the property <br>
&nbsp; 5.4. one axiom defining the range of the property <br>
&nbsp; 5.5. any additional axioms expressing disjointness of the property with other data properties, and whether the property is functional. <br>
6. Define the axioms necessary for expressing any statement in 1 to 12 that has not already been expressed. 
7. Populate the ontology with at least one individual for each class, and at least one assertion for each property.

Additionally:

8. Identify two different assertions that would make the ontology inconsistent.
9. Define the complex role inclusion axiom capturing the fact that if an employee has an office that is contained in a building that is assigned to an institute that is part of a research organisation, then the
employee has a contract with that research organisation.
10. Verify and explain whether or not the created ontology (including the complex role inclusion axiom defined in 9) satisfies the global restrictions on the axioms of an OWL 2 DL ontology.
11. Write the following queries in SPARQL: <br>
&nbsp; 11.1. Find all the offices that host at least one graduate fellow and order the results by employee ID. <br>
&nbsp; 11.2. Find all the senior researchers with ID lower than 5000 who are members of the laboratory named “AIMH”. <br>
&nbsp; 11.3. Find all the laboratories that have a total number of research group greater than 2. <br>
