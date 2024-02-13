<span style="color:#00b050">Basic building blocks</span>
	entity - anything about which data are to be collected and stored
	attribute - a characteristics of an entity
	relationship - describes an association among entities
		one to many (1:m)
		many to many (M:M or M:N)
		one to one (1:1)
	Constraint - a restriction placed on the data



<span style="color:#00b050">Relational model</span>
	developed by Codd (IBM) in 1970
	conceptually simple
	relational database management system (RDBMS)
		hide the complexities of the relational model from the user
	rise to dominance due to in part to its powerful and flexible query lang
	SQL allows the user to specify what must be done without specifying how it must be done
	SQL-based relational database application involves 
		user interface
		a set of tables stored in the database
		SQL engine

<span style="color:#00b050">Steps in database design</span>
	requirement analysis
		user needs what must databse do?
	conceptual design
		higher description(often done w/ER model)
	logical design
		translate ER into DBMS daata model
	schema refinement
		consistency, normalization
	physical design-indexes, disk layout


<span style="color:#00b050">Conceptual design</span>
	what are the entities and relationships in the enterprise?
	what information about these entities and relationships should we store in the database?
	what integrity constraints or business rules hold?
	a database schema in the ER model can be represented pictorially (ER diagrams)
	can map an ER diagram into relational schema.

<span style="color:#00b050">ER model basics</span>
	entity: real-world objects, distinguishable from other objects. An entity is described using a set of attributes.
	Entity **set**: a collection of similar entites. E.g all employees
		all entities in an entity set have the same set of attributes. (Until we consider hierarchies)
		each entity set has a key(underlined)
		each attribute has a **domain**
	Relationship: association among two or more entities. E.g Jack works in Pharmacy department.
		relationship can have their own attributes.
	Relationship set: collection of similar relationships
		An n-ary relationship set R relates n entity sets E1,......En; each relationship in R involves entities e1 E E1,.....,en E En.
	same entity set can participate in different relationship sets, or in different "roles" in the same set.


<span style="color:#00b050">Contraints</span>
	an employee can work in many departments; a department can have many employees.
	in contrast, each department has at most one manager, according to the constraint on Manages.


<span style="color:#00b050">Definitions</span>
	Relational database: a set of relations
	relation: made up of 2 parts:
		schema: specifies name of relation. plus name and type of each column
			e.g., Students(sid: string, name: string, login: string, age: integer, gpa: real)
		instance: a table with rows and columns
			#rows = cardinality
			#fields =

<span style="color:#00b050">A lang of relational DB</span>
	SQL standard language
	data definition lang(DDL)
		create, modify, delete relations
		specify constraints
		administer users, security, etc
	Data manipulation lang(DML)
		specify queries to find tuples that satisfy criteria
		add, modify, remove tuples

<span style="color:#00b050">Keys</span>
	keys are a way to associate tuples in a different relations
	keys are one form of integrity constraint (IC)

<span style="color:#00b050">Primary keys</span>
	set of fields is a superkey if:
		no two distinct tuples can have same values in all key fields
	a set of fields is a key for a relation if:
		its a superkey
		no subset of fields is a superkey
	what if > 1 key for a relation?
		one of the keys is chose (by DBA) to be primary key. Other keys are called candidate keys.
	e.g.,
		SID is a key for Students
		what about name?
		the set(sid, gpa) is a superkey


<span style="color:#00b050">Primary keys and candidate keys</span>
	possibly many candidate keys (specified using UNIQUE), one of which is chosen as the primary key.
		keyys must be used carefully


