- Design must be Logical (portable), this means that it is a design without regard to a relational database management system. (RDMS)

- Physical Design
	- The Logical design adapted to a particular DBMS 
	- Fluid design that can change during implementation 

- Entity Relation Diagrams (ERD)
	- These are a common way of diagramming entities, their attributes, and their relationships
	- A great way to put your design thinking onto paper
	- Essentially the same as a Branch Topic and topic 
	- An entity is represented as a rectangle divided into three parts
		- Top = Name of the entity
		- Middle box = primary key
		- Bottom = attributes 

- Relationships
	- A relationship is established by repeating one field from one table to another
		- This key is usually a foreign key 
	- The primary key table can be referred to as the parent table, or master table
	- Tables with the foreign keys are sometimes referred to as child tables 
		- Foreign keys are redundancy, which is usually bad, but not in this case.
	- 3 types of relationships
		- One to One 
		- One to many
		- Many to many (Sometimes it is resolved in multiple Many to One relationships)
			- (Many students sign up to many classes ----> Student signs up to many classes + Many classes are assigned to one student)
		- 

- Crow's Feet Notation 
	- A three line, kind of like a pitchfork, represents the "many" side of the relationship 
	- One to many, many to one 

- Naming Conventions
	- Obviously, naming conventions are important, they must be consistent
	- Fuck camelCase, all my homies hate camelCase 

- Conger Book Naming Conventions
	- Entities and Tables are single nouns
		- Tutor
	- Attributes are named with the entity name along with the attribute name
		- TutorLastName
		- May be long, but long is good, MAXIMUM clarity
	- Primary Keys end with the word "key"
		- TutorKey
	- Foreign keys retain the name of the primary key 

- Term Equivalences
	- Table = Relation
	- Column and field = Attribute
	- Row, record = Tuple (Not a too-pull) 

- Repeating Fields (Attributes)
	- Usually bad, but when creating an entity that can contain many of the same attributes, it is tempting to list or number them
	- Don't. Numbering is a huge mistake 
	- It's a sign from god that you split that entity into two separate entities 

