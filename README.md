# arch-ilities
The following architecture qualities will guide technical design of applications and services.  The "-ilities" can be handled during development or during run-time.

[12 Factor App](https://12factor.net/) is a great example of an end to end implementation methodology.

## Architectural Dimensions
A compliment to qualities are dimensions.  Dimensions are higher level concerns.  These are some common dimensions defined in the book [Building Evolutionary Architectures by Patrick Kua, Rebecca Parsons, and Neal Ford](https://www.amazon.com/Building-Evolutionary-Architectures-Support-Constant/dp/1491986360).

### Technical
The implementation parts of the architecture: the frameworks, dependent libraries, and the implementation language(s).

### Data
Database schemas, table layouts, optimization planning, etc. The database administrator generally handles this type of architecture.

### Security
Defines security policies, guidelines, and specifies tools to help uncover deficiencies.

### Operational/System
Concerns how the architecture maps to existing physical and/or virtual infrastructure: servers, machine clusters, switches, cloud resources, and so on.

## Ilities
The following will provide descriptions and examples for the ilities I've used across recent products.

### Vulnerability
Data is gold.  This ility is handled during development by omitting credentials in code, by encrypting data in transit and at rest, by scanning source code, and during run-time with penetration testing.

### Confidentiality
Personal data is subject to [Global Data Protection Regulations](https://www.eugdpr.org/gdpr-faqs.html).

### Maintainability
There are many facets to maintainability.  
* Write code in a standard format and style; use a linter to check during development
* Use verbosity to make code more intuitive when read by others, i.e. use intuitive function and variable names
* Document complex code inline and provide readmes for more comprehensive coverage
* Reduce copy and paste development with abstractions; look for similar patterns as candidates for functions or generators

### Reliability
Data apps and services need to be reliable to ensure maximum data integrity.  Applications can use offline mode to deal with network connectivity issues.  Services are deployed to elastic infrastructure.

### Availability
Internal applications should be made available 100% of the time during business hours.  External applications should be available 24/7.

### Scalability
Applications should be made to scale to the 80th percentile of users.  Services need to handle 80th percentile of data volume.  The percentiles should reflect the need to mitigate risk to active users and revenue generation.

### Usability
Applications should be intuitive to use and quick to respond.  Views should load in a few seconds and services should respond in milliseconds.  Internal applications need to provide new capabilities or improve current processes.  

### Modifiability
Applications and services are in a constant state of flux.  When the effort vs cost tradeoff is favorable, system designs should account for anticipated growth areas.

### Portability
Applications and services should be able to be deployed in multiple environments across various platforms.  Minimize the dependencies on external systems.

### Integratability
Applications and services either provide or consume or both; full autonomy is rare.  Be empathetic to consumers of the service you provide and develop a relationship with the team of any service you consume.

### Reusability
Applications and services should keep in mind reusability during design.  Either parts of wholes of systems can be made for reuse by other systems or teams.  Applications can be decomposed into modules and published to a registry.  Services can be developed in an abstract way to be driven by domain specific configuration or business logic as data.

### Testability
Automated unit and integration testing should be built into production applications and services.  Prototypes and proof of concepts need to use effort vs cost tradeoff to determine need for comprehensive testing.

## Comprehensive List of Ilities
The [list](https://en.wikipedia.org/wiki/List_of_system_quality_attributes) is long and many are similar or redundanct.  Prioritize focal points based on product needs.
