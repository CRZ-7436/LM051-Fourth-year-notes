Weak extensibility mechanism(?)
	weak as in it doesnt protecting the standard

poorly defined semantics
	you want compilers that can generate code from diagrams

Model driven dev(MDD)
	must have a semantics

Identifying Use Cases
	Identify the actors.
	for each actor, determine:
		What they need from the system, use cases that have value for them - primary actor
		any other interactions with the system, use cases in which they play a role but do not derive direct benefit - secondary actor
	In addition to an understanding of task and users, must have:
		knowledge of risk associated with each use case
		a rough estimate of time required to implement each use case

Iconics (he said he will never mention it again)

use case realisation
to realise a use case, make reality

collaboration diagram
communication diagram
class responsibilities collaborations CRC card

linguistic incoherance
	this is another one of the problems of UML

communication diagram
	shows message passing see week 2 slide 40

star means iteration, see week 2 slide 40

use case class diagram, see week 2 slide 44

package just  defines name space - used to store classes
tabs (triangle) in top of square to show package

activity diagrams are really used for modeling work flows or business processes

recap
	use case relisation a systematic approach method to creating an analysis time diagram
	1 produces good quality, dont want a method that makes shit
	if both are using use case realisation, a pro and a noob will creating something similar.


architecture- what are the components their internal/external properties(interface) and relationships(dependencies)

use case description needs multiple steps

aggregation
^ unshaded diamond

with aggregation an object can take part in other associations including aggregation but not composition

association roles
	sometimes more readable to show each role that both objects play in an association

		advisor-------student
		avises--------advisee

why not use inheritances?
it is a maintenance nightmare, see week 3 lecture examples

qualified association
	see week 3 lecture notes square and board, the bottom one slide 10

forward slash "/" means derived 
	see slide 12 of week 3

constraints
	a constraint is any condition that has to be satisfied by any correct implementation of the design.
	express constraints as class invariants, written formally as object constraint language (OCL) which UML has adopted


liskob substitution princple (LSP)
	applicable to inheritance hierarchies
	it states that in object interaction, it should be possible to treat a derived class as if it were a base class



