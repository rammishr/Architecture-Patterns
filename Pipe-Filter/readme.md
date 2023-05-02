# PIPE and FILTER
The pipe and filter architecture is a software architecture pattern that involves processing data by passing it through a sequence of processing elements (filters) connected by pipes. Each filter is responsible for performing a specific transformation or manipulation on the data, and the pipes connect the filters to create a pipeline. It can be shown as below.

![image](https://user-images.githubusercontent.com/43367262/233911409-a90c672d-c6fd-4a07-8917-80cc7efd574b.png)

# Example
Many Unix command-line tools such as grep, awk, and sed are examples of the pipe and filter pattern being used in practice. These tools can be combined using pipes to perform complex data processing tasks on the command line.

Another example of the pipe and filter pattern being used in practice is in web application frameworks. These frameworks use the Model-View-Controller (MVC) pattern, which is a variation of the pipe and filter pattern. The request-response cycle in these frameworks can be thought of as a pipeline, with each component (request handler, controller, model, view) performing a specific task and passing the output to the next component through pipes.

# Benefits
The pipe and filter architecture pattern is useful for processing complex data through a series of discrete steps. However, it may not be the best fit for all scenarios, especially those involving simple data processing, real-time systems, or small applications. There are many frameworks and tools that provide the pipe and filter architecture pattern such as `Apache NiFi`, `Node.js streams`, `Apache Beam`, etc. Servicenow also provides the capability by use of `data source` and `transform maps`. 

## Demo
A sample web application example is provided in this folder where we will implement a simple file upload functionality using the Pipe and Filter architecture pattern. We will create a pipeline of filters that will process the uploaded file and save it to the server. You can download the Pipe-Filter.zip and run it by `"node index.js"`. You need to install the dependencies by using `"npm install"`.

