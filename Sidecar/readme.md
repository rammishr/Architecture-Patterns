## Sidecar Pattern

The Sidecar Pattern is a software architecture pattern in which an application is decomposed into two separate parts: a primary component and a secondary component, or "sidecar." The primary component is responsible for performing the application's core functionality, while the sidecar provides additional features, such as monitoring, logging, or data processing. This pattern is useful in distributed systems where a single application needs to perform multiple tasks, but each task requires different resources and dependencies.

For example, suppose you have a microservice that processes user data. In that case, the primary component might be responsible for handling requests, retrieving and updating data from a database, and returning responses to clients. However, you might also want to collect and analyze data on how the microservice is performing or add authentication and authorization features to secure the service. These additional features can be implemented as a sidecar, which runs alongside the primary component and provides these features.
        ![image](https://user-images.githubusercontent.com/43367262/235587641-69faea8f-4d6d-4791-a9b8-8986926ac3c0.png)


### How it works

The Sidecar pattern involves deploying a Sidecar container or process alongside the main container of a microservice. The Sidecar is responsible for handling certain tasks that are necessary for the application to function properly, but that are not directly related to the business logic of the main container.

The Sidecar typically handles tasks such as service discovery, load balancing, and security. For example, it may be responsible for registering the main container with a service registry, and for routing traffic to the appropriate instance of the main container.

By offloading these tasks to the Sidecar, the main container can focus on its core business logic, and the overall complexity of the application is reduced.

The sidecar can be implemented in various ways, such as a separate process, a container, or a library. The sidecar communicates with the primary component through an API or shared memory, depending on the implementation. The primary component remains agnostic to the sidecar's implementation, as the sidecar is treated as an independent module.

Following are some frameworks which provide tools to implement sidecar with in distributed systems. 

	• Istio: https://istio.io/
	• Linkerd: https://linkerd.io/
	• Consul: https://www.consul.io/
	• NGINX: https://www.nginx.com/

### Advantages

The Sidecar pattern offers several advantages:

- **Improved scalability**: By offloading tasks such as service discovery and load balancing to the Sidecar, the main container is free to focus on its core business logic, which can help to improve scalability.

- **Reduced complexity**: The Sidecar can help to reduce the overall complexity of the application by handling tasks that are not directly related to the business logic of the main container.

- **Improved modularity**: The Sidecar can be deployed independently of the main container, which can help to improve modularity and make it easier to update or replace individual components of the application.

- **Improved security**: The Sidecar can handle tasks such as authentication and authorization, which can help to improve the overall security of the application.

### Disadvantages

There are also some disadvantages to using the Sidecar pattern:

- **Increased resource usage**: Deploying a Sidecar container or process alongside each main container can increase resource usage, which can be a concern for applications that need to scale to handle large workloads.

- **Increased complexity**: Although the Sidecar can help to reduce the overall complexity of the application, it also introduces additional complexity by adding an additional component to the application.

- **Increased maintenance**: Maintaining the Sidecar can be more complex than maintaining the main container, as it requires additional configuration and management.

### Use cases

The Sidecar pattern is often used in microservices architectures to handle tasks such as service discovery, load balancing, and security. It is particularly useful in environments where scalability is important, as it can help to offload tasks that might otherwise limit the ability of the application to scale.

### DEMO
A sample web applictaion is present in this folder. You can extract `sidecar.zip` and run it using `node main.js`.

### Conclusion

The Sidecar pattern is a useful microservices pattern that can help to improve the scalability, modularity, and security of microservice applications. By offloading certain tasks to a separate container or process, the Sidecar can reduce the complexity of the main container and allow it to focus on its core business logic.
