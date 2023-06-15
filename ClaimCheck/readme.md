# Claim Check Pattern

The Claim Check pattern is a messaging pattern used to manage large payloads or data objects between components or services. It allows decoupling the sender and receiver by storing the payload in an external storage system, such as a file or a database, and passing a lightweight identifier (claim check) between them.

## Problem

In distributed systems, components or services often need to exchange large payloads or data objects. This can introduce challenges when the payload size exceeds the limitations of message queues, network bandwidth, or memory. Additionally, passing the entire payload with each message can introduce latency and increase message processing time.

## Solution

The Claim Check pattern addresses the problem of handling large payloads by storing the payload in a separate storage system and passing a claim check or identifier between the sender and receiver. The claim check can be a unique identifier, such as a UUID, which is used to retrieve the payload when needed.

The solution involves the following components:

1. **Sender**: The component or service responsible for creating the payload and storing it using the claim check.
2. **Storage System**: An external storage system, such as a file system or a database, used to store the payload associated with the claim check.
3. **Receiver**: The component or service that receives the claim check and retrieves the payload from the storage system when needed.

![image](https://github.com/rammishr/Architecture-Patterns/assets/43367262/e8011f9a-382a-4401-857d-bee482cfc14c)


## Implementation

### Sender

1. Generate or create the payload that needs to be sent to the receiver.
2. Store the payload in the storage system using a unique claim check as the identifier.
3. Send the claim check to the receiver.

### Receiver

1. Receive the claim check from the sender.
2. Retrieve the payload associated with the claim check from the storage system.
3. Process the payload as needed.

## Benefits

The Claim Check pattern provides several benefits:

- **Reduced payload size**: By storing the payload externally and passing only the claim check, the size of the messages or requests can be significantly reduced.
- **Scalability**: The decoupling between the sender and receiver allows for scalability and distributed processing.
- **Efficient resource utilization**: Large payloads can be stored in a dedicated storage system optimized for efficient storage and retrieval.

## Use Cases

The Claim Check pattern can be applied in various scenarios, including:

- **File transfers**: Large files can be stored in a file system or object storage, and the claim check can be used to manage the transfers between systems.
- **Messaging systems**: When messages contain large data objects, the claim check can be used to optimize message processing and reduce the memory footprint.
- **Microservices architectures**: Microservices can leverage the Claim Check pattern to exchange large payloads without burdening the messaging infrastructure.

## Demo
You can extract the compressed file in this folder and run the sender program with `node sender.js`. Please note down the clain id and put it in `receiver.js` file. You can then run the receiver file by `node receiver.js`. 
This will print the payload on console. 

## Conclusion

The Claim Check pattern is a valuable technique for managing large payloads in distributed systems. By storing the payload in an external storage system and passing a claim check between components, it enables efficient and scalable communication. This pattern reduces the burden on network resources and enhances overall system performance.

Using the Claim Check pattern, developers can design systems that effectively handle large payloads while maintaining flexibility and decoupling between components or services.

