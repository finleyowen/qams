# QAMS Scorecards

A scorecard defines criteria and their associated scores. The following class diagram is provided to show the relationships between scorecards, criteria, and criterion scores. Note that the 'classes' in the class diagram are actually implemented as Rust `struct`s, and the "interfaces" are actually implemented as Rust `trait`s.

![Class diagram for the scorecard module](../uml/scorecard.png)

Note that the `ScorecardComponent` trait achieves the **Composition** design pattern since it provides a unified interface between scorecards and criteria, where a scorecard consists of many criteria.

The QAMS handles creation and editing of scorecards. Scorecards are used to produce [reviews](./reviews.md).