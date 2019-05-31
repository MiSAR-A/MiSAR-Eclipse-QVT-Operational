# RQ1: PSM Metamodel

Source artifacts of each microservice architecture projects used in our study were packaged and uploaded into one GitHub repository. Artefacts contained in each repository can be classified into two main elements:

### 1. SystemProjectArtifactsModel

PSM concepts that map to *system-level* classifiaction of artifacts are provided in the table below: 

PSM Concept | PSM Attribute(s) | Description
------------ | ------------- | -------------
`SystemProjectArtifactsModel` | `ProjectName`, `ArtifactsRepositoryURI` | Represents the *system-level* project artefacts. `SystemProjectArtifactsModel` is described by architecture’s project name and its root repository URI. 
`SystemProjectArtifactFile`| `FileName` | this element generalizes files that configure building, orchestrating and integrating all modules/application projects aggregated in a microservice-based architecture project. `SystemProjectArtifactFile` element is described by its file name including full path as well as by the system’s project name to which this file belongs. According to our empirical study, there were two classes of such file type appeared in all stud-ies, namely, `DockerComposeFile` and `SystemProjectBuildFile`. Aiming to make our PSM extendible and reusable, we assumed that there may be more than two subtypes of such file.
`DockerComposeFile` | | this element maps to Docker compose file, i.e. a YAML file that defines orchestration of microservice applica-tions’ containers at runtime and other network-related information, i.e. links among containers. One `DockerComposeFile` represents one consolidated Docker compose file that has many service definition keys, mapped to `ContainerDefinition` elements, each has zero or many ‘links’ / ’depends_on’ keys, mapped to `ContainerDependency` elements.
`ContainerDefinition` | `ServiceName`, `ImageField`, `BuildField`, `LoggingField`, `VolumesLogField` | A `ContainerDefinition` element may refer to a local microservice project, mapped by `MicroserviceProjectArtifactsModel` element, or to an image of an external service, e.g. located in Docker hub repository.  
`ContainerDependency` | `DependencyOrder` | A `ContainerDependency` element represents an ordered dependency association between one dependent / consumer `ContainerDefinition` element to one or many `ContainerDefinition` ‘provider’ elements.  

### 2. MicroserviceProjectArtifactsModel

Represents *microservice-level* project artefacts.  `MicroserviceProjectArtifactsModel` element is composed of many elements that model different types of system project artefacts and their content as explained in the following:

PSM Concept | PSM Attribute | Description
------------ | ------------- | -------------
