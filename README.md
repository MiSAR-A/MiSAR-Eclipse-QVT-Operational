# Refining The Micro Service Architecture Recovery Approach: An Empirical Study

<br/>

This repository includes the `Eclipse QVT Operational` project for `MiSAR` model-based architecture recovery. Along with explanations and illustrations for the theory behind it.  

<br/>

Folder Name | Description 
----------- | -----------
[RQ1-PSM](https://github.com/MiSAR-A/MiSAR-A-QVT/tree/master/RQ1-PSM) | Theory and Implementation of PSM model 
[RQ2-PIM](https://github.com/MiSAR-A/MiSAR-A-QVT/tree/master/RQ2-PIM) | Theory and Implementation of PIM model 
[RQ3-MAPPING](https://github.com/MiSAR-A/MiSAR-A-QVT/tree/master/RQ3-MAPPING) | Theory and Implementation of PSM-to-PIM Mapping Rules
[RQ4-RECOVERY](https://github.com/MiSAR-A/MiSAR-A-QVT/tree/master/RQ4-RECOVERY) | Theory and Implementation of Transformation using `Eclipse QVT Operational`

<br/><br/>

## Abstract

[Micro Service Architecture](https://microservices.io/) is considered as a well-known architectural style in the current era. It assesses each system as a collection of tiny components that may incorporate one or more modules. In the highly dynamic enterprise domain, micro services are developed quickly to achieve a fast time-to-market, and new features have to be introduced regularly in order to stay competitive. However, the practice shows that the software architects are often facing the challenge of not knowing carefully the real software architecture of the system they architect and there is  a chasm between the conceptual software architecture in the minds of the architects and the concrete architecture that is found in the micro-services orchestration and implementation.

In this regard, this paper aims at providing an approach that would help to enhance the architecture recovery of a microservice software system that can expose the architectural aspects perceived as crucial for the developers. **MiSAR** is an architecture recovery approach based on the main concepts of the model-driven paradigm. In this paper, an empirical study is conducted with the aim of validating the capability of **MiSAR** artefacts in recovering the architecture of 8 microservice systems. The study resulted in a refinement of **MiSAR** existing artefacts: the meta-model, mapping rules. 

## Introduction

<img src="https://github.com/MiSAR-A/Journal-Results/blob/master/images/image.png" alt="Kitten" title="Misar" width="600" />

**MiSAR** is an approach for recovering the architecture of microservice systems. **MiSAR** has been designed to follow the [Model Driven Engineering](https://ict.eu/model-driven-engineering/). The main elements of **MiSAR** includes three different abstraction levels defined as `L0`, `L1` and `L2`. As described in the above Figure, `L0` level includes the microservice software system in the real world as a set of physical artifacts. It currently includes the source code files, configuration files, Docker files, Docker compose file, build file and project build file. 

Further, the `L1` level (also abbreviated as `PSM model`) can represent the software artifacts of different models at `L0`. `PSM` consists of artifacts that has more than one model according to specific metamodels which show six models at `PSM` level, each conforming to their own meta-model, respectively. E.x Source code model as described by the Java metamodel for Java file and Container build model as described by the Containerization build metamodel for Docker file. 

**MiSAR** artefacts have been designed by conducting empirical studies where our experience in analyzing microservice systems as presented in the above Figure. This has resulted in an approach that has been built bottom up. 
