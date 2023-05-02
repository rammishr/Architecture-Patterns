
# Strangler Pattern

The Strangler Pattern is a software development approach that helps developers to modernize legacy applications by incrementally migrating functionality to a new system over time. This pattern is particularly useful for large, complex applications with a lot of legacy code that needs to be updated or replaced.

The Strangler Pattern involves the creation of a new system that gradually takes over functionality from the old system, until eventually the old system is completely replaced. The new system can be built using modern technologies, while the old system continues to function as it always has.

## How it works

The Strangler Pattern works by intercepting requests to the legacy system and routing them to the new system. This is done using a combination of middleware, APIs, and other techniques. As the new system takes on more functionality, it becomes increasingly integrated with the legacy system, until eventually the legacy system is no longer needed.

One of the key benefits of the Strangler Pattern is that it allows developers to modernize their applications in a way that is safe and controlled. By gradually migrating functionality to the new system, developers can ensure that the new system is stable and reliable before turning off the old system.
![image](https://user-images.githubusercontent.com/43367262/235585012-b42db00c-7030-473f-a168-d4ae6781d278.png)


## Benefits of the Strangler Pattern

- Incremental modernization: The Strangler Pattern allows developers to modernize their applications in a gradual, incremental way, which reduces risk and minimizes disruption.
- Improved stability and reliability: By gradually migrating functionality to the new system, developers can ensure that the new system is stable and reliable before turning off the old system.
- Reduced maintenance costs: Legacy systems can be expensive to maintain and update. The Strangler Pattern helps to reduce maintenance costs by allowing developers to migrate functionality to a new system that is easier and less expensive to maintain.

## How to implement the Strangler Pattern

Here are some basic steps to follow when implementing the Strangler Pattern:

1. Identify the functionality to be migrated: Start by identifying the functionality that needs to be migrated from the legacy system to the new system. This can be done by analyzing user requirements, system documentation, and other sources of information.

2. Create a new system: Create a new system that can handle the functionality identified in step 1. This system should be built using modern technologies and should be designed to integrate with the legacy system.

3. Add routing middleware: Add routing middleware to intercept requests to the legacy system and route them to the new system. This can be done using APIs, proxies, or other techniques.

4. Migrate functionality: Begin migrating functionality from the legacy system to the new system. This should be done in small, incremental steps to reduce risk and ensure that the new system is stable and reliable.

5. Test and validate: Test and validate the new system to ensure that it is functioning correctly. This can be done using automated testing tools, user acceptance testing, and other techniques.

6. Switch off the legacy system: Once all functionality has been migrated to the new system and the new system has been validated, the legacy system can be switched off.

## Demo
A sample web application example is provided in this folder where we will implement a simple server using the architecture pattern. You can download the strangler.zip and run it by `"node app.js"`. You need to install the dependencies by using `"npm install"`. You can test it by opening the `test.html` file in browser and submitting the form.

## Conclusion

The Strangler Pattern is a powerful technique for modernizing legacy applications. By gradually migrating functionality to a new system, developers can reduce risk, improve stability, and lower maintenance costs. If you have a legacy application that needs updating, consider using the Strangler Pattern to help make the process smoother and more efficient.
