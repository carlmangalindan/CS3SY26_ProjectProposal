# CS3SY26_ProjectProposal

### Project Title or Name of the Application	: Cite Right
### Section			   	      : Lithium
### Group Members			    : Mangalindan, Lacanilao, Bodiongan
### Date (Proposal Date)  : Nov 14, 2026
### Project Description:

SUMMARY:

As students who constantly refer to websites and material for learning, citation is very important as to avoid getting plagiarized. However, citation can, at times, be time consuming and be alloted more time than necessary. To fix this, our group is developing "Cite Right", a program meant for students to minimize the time for citing, and maximize the time for actually doing the project. It does this by gathering data and organizing it to fit the APA 7th style of citation. Moreover, students use AI to cite their sources. However, AI is limited, it cannot always access every piece of material, it also opens up windows of error that can be minimized through our program.

`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-
  
### Elements, Attributes, Methods:

Class: Source

**The Source class acts as the abstract parent class from which more subclasses of more specific media types inherit from.**
Attributes: authors, year_published, and title, which are the information common to all citations regardless of media type. 
Methods: cite_in_text(), which would follow a single format involving authors and year_published, and cite_ref_list(), a method that would be overridden by subclass methods because the format varies.

`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-

Class: ReferenceList

**ReferenceList is the class that functions to store the user's sources and print the citations under each list.**\
Attributes: name, reflist. At first, reflist is empty, but to be appended into it are Source objects that would have been instantiated already.\
Methods: add_source() simply appends a Source object into reflist. print_bibliography() runs through reflist and prints each object's corresponding citation using the cite_ref_list() method of Source.\
Relationship: Each ReferenceList object is an aggregation of one or more Source objects.\

`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-

Subclasses: Book(Source), NewspaperArticle(Source)

**These are both non-digital (or print) media, and corresponding subclasses were directly inherited from Source class.**\
Attributes: Aside from the attributes in the parent class Source, Book(Source) has the additional attribute of publisher, and NewspaperArticle(Source) has the additional attributes of date_published and newspaper. These are the additional required information in APA 7th edition.\
Methods: cite_ref_list() overrides the empty version of this method in the parent class. For each of these subclasses or types of sources, the method cite_ref_list() simply returns the corresponding way to cite it in APA 7th edition.
Relationship: Inherited from Source along with DigitalMedia(Source)\

`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-

Subclass: DigitalMedia(Source)

**DigitalMedia(Source) inherits from Source, and it also acts as the parent class of Webpage(DigitalMedia) and JournalArticle(DigitalMedia).**\
Attributes: url (aside from attributes in its superclasses and subclasses)\
Methods: cite_ref_list() which still doesn't do anything as of now.\

`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-

Subclasses: Webpage(DigitalMedia), JournalArticle(DigitalMedia)

**Since both of these are digital media, they were both inherited from DigitalMedia(Source).**\
Attributes: additional date_published and website_name attributes are included in Webpage(DigitalMedia), while periodical_name is needed for JournalArticle(DigitalMedia).\
Methods: cite_ref_list, which basically has the same role as the same method in Book(Source) and NewspaperArticle(Source).\

`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-`-

Target Demographic:

Cite Right is a program made by students, for students. We've experienced first hand how citation eats time, and through this we realized that this could be fixed.

### UML Diagram
<img width="1544" height="778" alt="image" src="https://github.com/user-attachments/assets/bda02735-f9a8-4ee0-81b6-fa394e0fc6fa" />

### Goals:

Long Term Outcomes:

To have easier write up making and better and more organized time management.

Objectives:

- Objective 1: To be able to make write ups and projects easier to handle.
- Objective 2: For the program to be used frequently.
- Objective 3: To reiterate the program with accordance to the feedback of the users.

[Click here for Rubrics and Sample projects](https://docs.google.com/document/d/1xKd1CqK6DcNWS2_oJPBNtY5n3I3Hqiw8FY3W295Iqfk/edit?usp=sharing)
