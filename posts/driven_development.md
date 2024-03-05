# Why are there so many of these techniques cropping up?

Testing Driven Development, Behaviour driven development, Feature driven development, Domain driven development ...

The list goes on and on with all the development methodologies coming out the woodwork and growing in popularity.

Here is a a brief summary of each as well as some scenarios when is best to use them.

---

### Testing Driven Development
    Summary

    Creating the tests for the code before writing the code.

    After creating the tests, write the code and as tests start passing, keep expanding the test coverage.
    
    This approach leads to more thorough testing as well as more modular testable code.

    Scenario :
    Thoroughly documented design which requires implementing.
    Alternatively when the design does not have a high degree of unknown complexities.

### Behaviour Driven Development
    Summary 

    This is where set behaviours are translated directly into code.

    Always starting with a set of behaviours a feature is required to achieve, these can be anything but are often a set of business / product requirements. Often translated into very simple logic that any layman can understand.
    The most common language to achieve this is Gherkin, with cucumber, melon and many other frameworks utilising this language.

    A common pattern for these behaviours is the following:
    
    Scenario: Customer is setting up a device.
    Given: Customer presses a button.
    When: The light is blue.
    Then: The light turns green.
    
    These can be refined and created by anyone in user acceptance testing, but as long as the required behaviours are simply defined then BDD can be used.

    Each of these statements would then be mapped to a code output in this situation, often utilising "Feature" files and interpreters.

    The key is to achieve the entire set of business logic before moving onto the next section of development.

    This often leads to each statement having its own set of usable code so that when behaviour changes need to happen then "product" managers are able to understand as well as clearly communicate to a development team these changes, each statement being independant should also lead to only smaller technical changes required.
    
    Scenario:
    This is forcing a modular software design with clear business logic to stakeholders.

### Domain Driven Development

    Summary:
    Focuses of specifying specific "Domains" which can be associated with specific business logic. These domains are often controlled by domain "experts" these are not programming experts but business experts whom understand that task/proceedure the program is attempting to automate or perform.

    Similar to BDD in terms of the aims, but with a larger extreme where groups of features are referred to as "domains" and require to be achieved, in practise this is achieved similarly to BDD with "Models" being used to create an abstraction layer between "domains" and the underlaying programming functions.

    Scenario:
    Very Business centric logic, where having non-programmer experts is key, yet without having to utilise Gherkin or similar syntax.
    I imagine this be well utilised in a software contracting design company.

### Feature Driven Development
    Scenario: 
    A large project with a large variety of different complex features

    Not as well documented or accepted as TDD/BDD in essence FDD is taking a product or project and creating an expected feature list.
    Then turning each feature into a mini project. Which requires the usual planning, implementing and deployment for each feature.


    In my experience this is often not very suitable when doing agile, as it requires alot of the features to only be loosely connected or with a large amount of additional planning. Otherwise it makes more sense to plan the entire project in one go and achieve implementation in the same steps as best fits whichever software methodology the team prefers.
    TDD and BDD can both be fitted and implemented into a single "ticket" or unit of work, whereas FDD is more for larger chunks of work.

### Personal preference

Each tool has its best environment. 
My preference is primarily to use Test driven development whenever i have the chance.
I will often write different types of tests, which are out of the scope of this document.
But generally i will choose to start my TDD with unit tests.

