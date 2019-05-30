# nullness-exercise

A software engineering exercise to find a (seeded) nullness bug 
in an example file from Apache Commons IO via static analysis.

Two static analyzers are enabled:
* [SpotBugs](https://spotbugs.github.io/), a heuristic bug-finding tool
* The [Nullness Checker](https://checkerframework.org/manual/#nullness-checker) of the Checker Framework, a pluggable typechecker

To run SpotBugs, run the `spotBugsMain` gradle task.

To run the Nullness Checker, run the `compileJava -PuseCheckerFramework` gradle task.
