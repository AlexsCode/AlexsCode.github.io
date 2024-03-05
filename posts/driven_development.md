# Why are there so many of these techniques cropping up?

Testing Driven Development, Behaviour driven development, Feature driven development, Design driven development ...

The list goes on and on with all the development methodologies coming out the woodwork and growing in popularity.

Here is a a brief summary of each as well as some scenarios when is best to use them.

---

### Testing Driven Development
    Summary

    Creating the tests for the code before writing the code.

    After creating the tests, write the code and as tests start passing, keep expanding the test coverage.
    
    This approach leads to more thorough testing as well as more modular testable code.

    Scenario

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

    This often leads to each statement having its own set of usable code so that when behaviour changes need to happen then "product" managers are able to understand as well as clearly communicate to a development team these changes, each statement being independant should also lead to only smaller technical changes required. This is forcing a modular software design with clear business logic to stakeholders.

