- 3 Principles of Distributed Systems :
  - Single responsibility principle - Each component present in System Design should have a single job to perform.
  - No single point of failure principle - The system should never have any component whose failure will result in the failure of the entire system.

  - No bottleneck principle - Since we design for scalability our system should not have performance bottlenecks. Ideally we should horizontally scale our system to handle the large amounts of processing.
<br />

- 5 Steps for System Design :
  - Requirement analysis - Here we first discuss the functional requirements i.e. what this system should do. Then we discuss the non-functional requirements i.e. how the system should behave.
  - API design - Here we define the interfaces we expose to the outside world using which the communication happens. Here we have to define the name of the apis, the parameters it takes and the return values.
  - Define data model
  - High level design
  - Scale the design
