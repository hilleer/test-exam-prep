# Integration testing

- Explain what the focus and purpose of integration testing is

**Formålet med integrationstest er at verificere funktionaliteten mellem moduler, som er integreret.**
Integration Test case differs from other test cases in the sense it focuses mainly on the interfaces & flow of data/information between the modules. Here priority is to be given for the integrating links rather than the unit functions which are already tested.

Sample Integration Test Cases for the following scenario:Application has 3 modules say 'Login Page', 'Mail box' and 'Delete mails' and each of them are integrated logically.

Here do not concentrate much on the Login Page testing as it's already been done in Unit Testing. But check how it's linked to the Mail Box Page.

Similarly Mail Box: Check its integration to the Delete Mails Module.




- Account for the relation between integration scope and defects isolation

Testing performed to expose defects in the interfaces and in the interactions between integrated components or
systems. 
The individual modules are first tested in isolation. Once the modules are unit tested, they are integrated one by one, till all the modules are integrated, to check the combinational behavior, and validate whether the requirements are implemented correctly or not.??



- Explain when integration is done and under which conditions


**Phase in software testing in which individual software modules are combined and tested as a group that occurs after
unit testing and before system testing.**
Integration testing takes as its input modules that have been unit tested, groups them in larger aggregates, applies
tests defined in an integration test plan to those aggregates, and delivers as its output the integrated system ready for
system testing
In its simplest form, two units that have already been tested
are combined into a component and the interface between them is tested. A component, in this sense, refers to an
integrated aggregate of more than one unit.


- List different types of integration tests and elaborate on the differences between them


Big Bang integration testing
**In Big Bang integration testing all components or modules are integrated simultaneously, after which everything is tested as a whole.**
**Advantage**: Big Bang testing has the advantage that everything is finished before integration testing starts.
**Disadvantage**: The major disadvantage is that in general it is time consuming and difficult to trace the cause of failures because of this late integration.

Top-down integration testing
**Testing takes place from top to bottom, following the control flow or architectural structure (e.g. starting from the GUI or main menu). Components or systems are substituted by stubs.**
**Advantages of Top-Down approach:**
	• The tested product is very consistent because the integration testing is basically performed in an environment that almost similar to that of reality
	• Stubs can be written with lesser time because when compared to the drivers then Stubs are simpler to author.
**Disadvantages of Top-Down approach:**
	• Basic functionality is tested at the end of cycle


Bottom-up integration testing

**Testing takes place from the bottom of the control flow upwards. Components or systems are substituted by drivers.**
**Advantage of Bottom-Up approach:**
	• In this approach development and testing can be done together so that the product or application will be efficient and as per the customer specifications.
**Disadvantages of Bottom-Up approach:**
	• We can catch the Key interface defects at the end of cycle
	• It is required to create the test drivers for modules at all levels except the top control


Incremental testing
**Another extreme is that all programmers are integrated one by one, and a test is carried out after each step.**
- The incremental approach has the advantage that the defects are found early in a smaller assembly when it is relatively easy to detect the cause
- A disadvantage is that it can be time-consuming since stubs and drivers have to be developed and used in the test.
- Within incremental integration testing  a range of possibilities exist, partly depending on the system architecture.

- Functional incremental

**Integration and testing takes place on the basis of the functions and functionalities, as documented in the functional specification.**
--- 

**_Demonstrate your solution to the study point exercise "Integration Testing"_**


- You should (as a minimum):

	- Explain the most important implications involved in performing integration tests that involve databases
	 A good test is self-sufficient and creates all the data it needs.
	You can make a setup method that all database tests call to put the DB in a known state
	Måske ikke bruge PROD DB men IN-MEMORY
	
	
	- Explain the purpose and some of the key features of DBUnit
	**DBUnit is JUnit extension for database testing**
 - Import and export data as XML datasets
 - Initialize database into known state before testing
 - Set up database state with DBUnit framework
 - Use xml datasets to alter database and define expected 
	
	
	- Demonstrate how Mockito and DBunit can be used in integration tests
