# Test case design

- Test case design (week 3)

- Point out the main differences between white box and block box tests
Specification-based testing technique is also known as ‘black-box’ or input/output driven testing techniques because they view the software as a black-box with inputs and outputs.

The testers have no knowledge of how the system or component is structured inside the box. In black-box testing the tester is concentrating on what the software does, not how it does it.

The definition mentions both functional and non-functional testing. Functional testing is concerned with what the system does its features or functions. Non-functional testing is concerned with examining how well the system does. Non-functional testing like performance, usability, portability, maintainability, etc.

Specification-based techniques are appropriate at all levels of testing (component testing through to acceptance testing) where a specification exists. For example, when performing system or acceptance testing, the requirements specification or functional specification may form the basis of the tests.

• There are four specification-based or black-box technique:
	○ Equivalence partitioning
	○ Boundary value analysis
	○ Decision tables
	○ State transition testing

• WHITE BOX


• Structure-based testing technique is also known as ‘white-box’ or ‘glass-box’ testing technique because here the testers require knowledge of how the software is implemented, how it works.

• In white-box testing the tester is concentrating on how the software does it. For example, a structural technique may be concerned with exercising loops in the software.


• Different test cases may be derived to exercise the loop once, twice, and many times. This may be done regardless of the functionality of the software.


• Structure-based techniques can also be used at all levels of testing. Developers use structure-based techniques in component testing and component integration testing, especially where there is good tool support for code coverage.


• Structure-based techniques are also used in system and acceptance testing, but the structures are different. For example, the coverage of menu options or major business transactions could be the structural element in system or acceptance testing.



- List a few of the elements that a high quality test case in your opinion is comprised of

A well-written Test Case clearly mentions the expected result of the application or system under test. Each test design step should clearly mention what you expect as outcome of that verification step.
So, while writing test cases, mention in detail what page/screen you expect to appear after the test and, any updates you expect as an outcome to be made in back-end systems or database (ex. a new entry should be made to DB table).
You can also attach screenshots or specification documents to the relevant step mentioning the system should work as outlined in the given document to make things simpler.

Mainly, you would find the below information in a well-written test case description:
• Test to be carried out/behavior being verified
• Preconditions and Assumptions (any dependencies)
• Test Data to be used
• Test Environment Details (if applicable)
• Any Testing tools to be used for the test
I have written more about ‘Assumptions and Preconditions’ and ‘Test Data’ below.


- Elaborate on the role of oracles and their usage with regards to test cases 

One of the most important aspects of a test is that it checks that the system does what it is supposed to do. 

We may not know what the right answer is in detail every time, and we can still get some benefit from this approach at times, but it isn’t really testing. In order to know what the system should do, we need to have a source of information about the correct behavior of the system – this is called an ‘oracle’ or a test oracle.



- Explain the overall focus and important considerations in relation to the test analysis process

Test analysis is the process of looking at something that can be used to derive test information.  This basis for the tests is called the test basis.

The test basis is the information we need in order to start the test analysis and   create our own test cases. Basically it’s a documentation on which test cases are based, such as requirements, design specifications, product risk analysis, architecture and interfaces.

We can use the test basis documents to understand what the system should do once built. The test basis includes whatever the tests are based on. Sometimes tests can be based on experienced user’s knowledge of the system which may not be documented.


From testing perspective we look at the test basis in order to see what could be tested. These are the test conditions.  A test condition is simply something that we could test.



- Explain what has to be done during the test design process and what the result of it is

Basically test design is the act of creating and writing test suites for testing a software.

Test analysis and identifying test conditions gives us a generic idea for testing which covers quite a large range of possibilities. 

But when we come to make a test case we need to be very specific. 

In fact now we need the exact and detailed specific input. But just having some values to input to the system is not a test, if you don’t know what the system is supposed to do with the inputs, you will not be able to tell that whether your test has passed or failed.

Once a given input value has been chosen, the tester needs to determine what the expected result of entering that input would be and document it as part of the test case. Expected results include information displayed on a screen in response to an input. If we don’t decide on the expected results before we run a test then there might be a chance that we will notice that there is something wildly wrong.


- Explain which tasks to carry out and decisions to take in the test implementation process
The document that describes the steps to be taken in running a set of tests and specifies the executable order of the tests is called a test procedure
When test Procedure Specification is prepared then it is implemented and is called Test implementation.
Writing the test procedure is another opportunity to prioritize the tests, to ensure that the best testing is done in the time available. A good rule of thumb is ‘Find the scary stuff first’. However the definition of what is ‘scary’ depends on the business, system or project and depends up on the risk of the project.



- Account for some general aspects concerned with test (design / case / procedure) documentation

Er det "bare" en opsummering af overstående?


- Describe how the techniques equivalence partitioning and boundary value analysis are applied in test case design and outline the reasons for using each technique 

Equivalence partitioning (EP) is a specification-based or black-box technique.

It can be applied at any level of testing and is often a good technique to use first.

The idea behind this technique is to divide (i.e. to partition) a set of test conditions into groups or sets that can be considered the same (i.e. the system should handle them equivalently), 
hence ‘equivalence partitioning’.

 Equivalence partitions are also known as equivalence classes – the two terms mean exactly the same thing.


In equivalence-partitioning technique we need to test only one condition from each partition. This is because we are assuming that all the conditions in one partition will be treated in the same way by the software. If one condition in a partition works, we assume all of the conditions in that partition will work, and so there is little point in testing any of these others. Similarly, if one of the conditions in a partition does not work, then we assume that none of the conditions in that partition will work so again there is little point in testing any more in that partition.

Boundary value analysis (BVA) is based on testing at the boundaries between partitions.

Here we have both valid boundaries (in the valid partitions) and invalid boundaries (in the invalid partitions).
As an example, consider a printer that has an input option of the number of copies to be made, from 1 to 99. To apply boundary value analysis, we will take the minimum and maximum (boundary) values from the valid partition (1 and 99 in this case) together with the first or last value respectively in each of the invalid partitions adjacent to the valid partition (0 and 100 in this case). In this example we would have three equivalence partitioning tests (one from each of the three partitions) and four boundary value tests.


- Describe the benefits of decision tables and state transition models in the context of test case design

A decision table is a good way to deal with combinations of things (e.g. inputs).

Decision tables provide a systematic way of stating complex business rules, which is useful for developers as well as for testers.

Decision tables can be used in test design whether or not they are used in specifications, as they help testers explore the effects of combinations of different inputs and other software states that must correctly implement business rules.



• State transition testing is used where some aspect of the system can be described in what is called a ‘finite state machine’. This simply means that the system can be in a (finite) number of different states, and the transitions from one state to another are determined by the rules of the ‘machine’. This is the model on which the system and the tests are based.

Any system where you get a different output for the same input, depending on what has happened before, is a finite state system.


We need to be able to identify the coverage of a set of tests in terms of transitions.

Deriving test cases from the state transition model is a black-box approach.

---

* Demonstrate your solution to the study point exercise "Test Case Design"
	- You should (as a minimum):
	- Explain how you have designed your different test cases
	- Explain which equivalence partitions and boundary values your test cases entail, plus why you have chosen these specifically
	- Account for any open boundaries in your test cases 
	- Demonstrate if you have chosen a two or three value approach in your boundary value analysis
	- Demonstrate how a decision table is created and used in your test case
