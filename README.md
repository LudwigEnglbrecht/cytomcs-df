CytoMCS-DF
=======

This is an extended version of CytoMCS for use in digital forensics. It allows to determine a flexible similarity of two data provenance graphs. Please follow the workflow procedure in the section below.

CytoMCS-DF was extended for data-provenance application but builds on the knowledge of Simon J. Larsen and Jan Baumbach (see reference section):
CytoMCS is a Cytoscape 3.0 app for computing the maximum common edge subgraph between two or more large networks.
The app uses an iterative local search algorithm to find large conserved subgraphs, and is able to detect not only fully conserved edges, but also partially conserved. CytoMCS supports both directed and undirected networks.

## Installation

<!--- The Cytoscape app is available through the Cytoscape app store here: http://apps.cytoscape.org/apps/cytomcs. -->

## Compilation

First clone and compile the FaithMCS repository:

```
git clone https://github.com/SimonLarsen/faithmcs.git
cd faithmcs
mvn package
```

Then clone the CytoMCS-DF repository, install the FaithMCS package locally and compile:

```
git clone https://github.com/LudwigEnglbrecht/cytomcs-df.git
cd cytomcs-df
mvn install:install-file -Dfile=/path/to/faithmcs-0.2.jar
mvn package
```

The compiled Cytoscape 3.0 app can then be found in cytomcs/target/cytomcs-1.1.jar.


## Workflow of application

## Source code

The original source code for CytoMCS and FaithMCS is available here:
* https://github.com/SimonLarsen/cytomcs
* https://github.com/SimonLarsen/faithmcs

## License

CytoMCS is licensed under the GPU General Public License v3.0.
See https://www.gnu.org/licenses/gpl-3.0.en.html for more information.

## Reference

Englbrecht Ludwig, Langner Gregor, Pernul Günther and Quirchmayr Gerald. "Enhancing credibility of digital evidence through provenance-based incident response handling." *ARES '19 Proceedings of the 14th International Conference on Availability, Reliability and Security*, ACM, New York, NY, USA (2019).

Larsen, Simon J., and Baumbach, Jan. "CytoMCS: A Multiple Maximum Common Subgraph Detection Tool for Cytoscape." *Journal of Integrative Bioinformatics* 14.2 (2017).
