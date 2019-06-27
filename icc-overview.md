# Overview of the FAIR Implementation Choices and Challenges Model (Draft)

## Namespace

    https://w3id.org/fair/icc/terms/

## Classes

- `Choice`: The kind of choice communities have to make (can be expressed as a question; choices are represented as rows in the Matrix)
- `Community`: A non-empty set of people and/or organizations that form a self-declared community with the aim to implement the FAIR principles for their fields of interest (communities are represented as columns in the Matrix)
- `Choice Declaration`: The expression of a community of their choice made (corresponds to an answer to a question, i.e. a cell in the Matrix)
- `Resource`: An artifact or service that can contribute to the implementation of the FAIR principles (corresponds to the possible values of the cells in the Matrix)

## Properties (= Relations)

- `refers-to-principle`: connects a `Choice` (left) to the FAIR principle (right) it refers to
- `refers-to-choice`: connects a `Choice Declaration` (left) to the `Choice` (right) it is derived from (indicates row of the Matrix)
- `declared-by`: connects a `Choice Declaration` (left) to the `Community` (right) that made the declaration
- `chosen-resource`: connects `Choice Declaration` (left) to the `Resource` that was chosen through the declaration

## TODO

Include `Challenge` and `Challenge Declaration`...
