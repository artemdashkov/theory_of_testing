## Prioritize features to test based on the following factors:
- Recent—New features, new areas of code, new functionality that has been recently repaired, refactored, or otherwise modified
- Core—Your product’s unique selling propositions (USPs). The essential functions that must continue to work in order for the product to be useful
- Risk—Areas of the application that pose more risk, such as areas important to customers but not used regularly by the development team or parts that use third-party code you don’t quite trust
- Problematic—Functionality that frequently breaks or often gets defect reports against it
- Expertise—Features or algorithms understood by a limited subset of people report

### cards --help
- Usage: cards [OPTIONS] COMMAND [ARGS]...
Cards is a small command line task tracking application.
Options:
--help Show this message and exit.
**Commands**:
- `add` Add a card to db.
- `config` List the path to the Cards db.
- `count` Return number of cards in db.
- `delete` Remove card in db with given id.
- `finish` Set a card state to 'done'.
- `list` List cards in db.
- `start` Set a card state to 'in prog'.
- `update` Modify a card in db with given id with new info.
- `version` Return version of cards application

### Creating Test Cases
- Start with a non-trivial, “happy path” test case
- Then look at test cases that represent
    - interesting sets of input,
    - interesting starting states,
    - interesting end states, or
    - all possible error states.

### When writing automated tests, these are common mistakes:
- Only writing happy path test cases
- Spending too much time thinking about how things can go wrong
- Ignoring how behaviors change based on system or component state