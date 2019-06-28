# Overview of the FAIR Implementation Choices and Challenges Model (Draft)

## Diagram

![diagram](icc-overview-diagram.png)

## Namespace

    https://w3id.org/fair/icc/terms/

## Classes

- `Choice`: The kind of choice communities have to make (can be expressed as a question; choices are represented as rows in the Matrix)
- `Challenge`: The kind of challenge that some communities face if the lack of existing resources doesn't allow them to make a choice yet
- `Consideration`: Something that is either a `Choice` or a `Challenge`
- `Community`: A non-empty set of people and/or organizations that form a self-declared community with the aim to implement the FAIR principles for their fields of interest (communities are represented as columns in the Matrix)
- `ChoiceDeclaration`: The expression of a community of their choice made (corresponds to an answer to a question, i.e. a cell in the Matrix)
- `ChallengeDeclaration`: The expression of a community of challenge they accepted
- `Declaration`: Something that is either a `ChoiceDeclaration` or a `ChallengeDeclaration`
- `Resource`: An artifact or service that can contribute to the implementation of the FAIR principles (corresponds to the possible values of the cells in the Matrix)

## Properties (= Relations)

- `refers-to-principle`: connects a `Consideration` (left) to a FAIR (sub-)principle (right) it refers to (a choice can refer to zero or more FAIR principles)
- `related-challenge`: connects a `Choice` (left) to a `Challenge` (right) that some communities might face before they can make the given kind of choice
- `refers-to-consideration`: connects a `Declaration` (left) to the `Consideration` (right) it is derived from (indicates row of the Matrix for choice declarations; a declaration has to refer to exactly one consideration; to address several consideration, separate declarations should be defined)
- `declared-by`: connects a `Declaration` (left) to the `Community` (right) that made the declaration (a declaration has to refer to exactly one community; to refer to several communities, separate declarations should be defined)
- `chosen-resource`: connects `ChoiceDeclaration` (left) to the `Resource` (right) that was chosen through the declaration (to refer to several resources, separate choice declarations should be defined)
- `has-open-challenge`: connects a `ChoiceDeclaration` (left) that doesn't have a chosen resource to a `ChallengeDeclaration` that describes a challenge that has to be met before the community can choose a resource (a choice declaration can refer to several challenge declarations)

