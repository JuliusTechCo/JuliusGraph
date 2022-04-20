# Frequently Asked Questions

By Julius Technologies Inc (email: info@juliustech.co)

Julius is an auto-scaling, low-code and visual graph computing solution. It can build and run sophisticated data and analytical pipelines as directed acyclic graphs (DAG) with very little coding. Readers are referred to [this blog](https://www.juliustech.co/blog/why-graph-computing-is-stellar) for a high level overview of the benefits of graph computing, and [this repo](https://github.com/JuliusTechCo/JuliusGraph) for [tutorials](https://juliustechco.github.io/JuliusGraph) and instructions to sign up for free developer access.

This FAQ page answers some of the most common questions from our users and clients. They are organized by subjects.

### Graph Computing and RuleDSL

1. What is graph computing?

   Conceptually, any computation, from the simplest formulas in a spreadsheet to the most complex enterprise systems, reduces to a directed acyclic graph (DAG). Graph computing, at its core, is to define, orchestrate and optimize computations using the generic DAG representation. Please refer to [this blog](https://www.juliustech.co/blog/amazing-graph) for an introduction to graph computing.

2. What are the benefits of graph computing and why do we need computational DAGs (directed acyclic graphs)? 
 
    Graph computing solves the most fundamental and challenging problems for building complex data and analytical pipelines and systems. These challenges include scalability, transparency, explainability, lineage, adaptability and reproducibility. Not only computational DAG is a generic representation of any data and analytical pipeline, it is 
    also an ideal representation for building generic solutions for these common challenges. Please refer to [this blog](https://www.juliustech.co/blog/why-graph-computing-is-stellar) for a full explanation.

    Julius Graph Engine is the first solution that delivers the full benefits of graph computing using a low-code RuleDSL, allowing a small development team to build sophisticated, scalable and transparent pipelines and systems with very little code. 

1. How does Julius build data and analytical pipelines as computational DAGs?

    `Atom` and `RuleDSL` are the two fundamental constructs in Julius for creating computational DAGs.

    `Atom` stands for atomic operation, it encapsulates the functions being performed at individual nodes in Julius' computational DAG. Atom is the minimal unit of distribution and caching in Julius' computational DAG. `Atom` can be implemented in any mainstream programming languages, such as C++, Python, Java, Julia, .Net and R, by inheriting from an Atom base class or interface. Existing libraries written in these languages can be easily wrapped up under the `Atom` interface.

    `RuleDSL` is a high level declarative domain specific language (DSL) for defining computational DAGs. RuleDSL features an easy to use and low-code syntax that connects individual Atoms to create the computational DAG, which can represent the entire data and analytical pipeline or workflow.

    Please refer to Julius [tutorials](https://juliustechco.github.io/JuliusGraph) for more detailed explanations and examples of using Atom and RuleDSL.

1. How does Julius Graph Engine access data?
   
    Julius Graph Engine creates and runs computational DAGs in two stages:
    
      * Build the data and analytical pipeline as a computational DAG (directed acyclic graph) from `RuleDSL` 
      * Run the computational DAG to process the data and produce the desired results
    
    Julius can access data in both stages, from any data source, such as a database, web URL, static files etc.
    
    The key advantage of the two stage data feeds is that the first stage usually requires a small amount of data for constructing the DAG. Once the DAG is built, it can be distributed to multiple computers, so that the heavy lifting of data processing in stage 2 can be done in parallel. This achieves much better performance for both graph creation and execution. A developer has full control over which types of data are fed at each stage through the `RuleDSL`. 

1. How does `RuleDSL` differ from ordinary programming languages such as Python/C++/Java? 

    General purpose programming languages like Python, C/C++ and Java are low-level and imperative, a developer has to specify the program's entire execution step by step, which requires a lot of coding. In comparison, the RuleDSL is a high level declarative domain specific language (DSL) for constructing computational DAGs. Using RuleDSL, a developer doesn't need to explicitly specify every step of a program's execution, instead they only need to declare the key data or analytical concepts and their logical dependencies. The Julius Graph Engine then automatically creates an executable computational DAG from the RuleDSL declarations. 
    
    Therefore it requires much less code in RuleDSL to specify the same data or analytical logic compared to the traditional programming languages, as most of the boilerplate flow control code is automatically generated by the Julius Graph Engine. The RuleDSL therefore doesn't need any of the complex flow control syntax in the traditional programming languages, such as variables, loops, branches, functions, classes, or inheritances etc. It is much easier then for a non-programmers to learn and use. Furthermore, RuleDSL's declarative syntax gives the Julius Graph Engine a lot more freedom to optimize its execution at run time, which allows for efficient auto-scaling and parallelization over multiple machines. 
    
    Julius RuleDSL is an exemplification of how less can be more: less coding in RuleDSL actually facilitates much better scalability and performance.

1. How can a computational DAG, which is acyclic, support loops? 

    It is true that there can't be any loops in the DAG by construction. However, it doesn't mean that we can't express looping logic in a DAG. There are multiple ways to do so in a DAG:

      * loops can be created inside an Atom (i.e., within a single node in the DAG)
      * create a set of nodes, where each node represents a batch of iterations in the loop (for example, if a Monte Carlo simulation runs with 100,000 paths, we can create 100 nodes, each running 1,000 MC paths) 
      * use recursion in RuleDSL if there are dependencies between loops 
      * run the computational DAG multiple times or in streaming mode

    Any of these options can be implemented easily using RuleDSL, without the need for any special syntax for looping. There are examples of recursion and Monte Carlo via streaming in the [tutorials](https://juliustechco.github.io/JuliusGraph).

1. How can you express conditional branches in RuleDSL and computational DAGs?

    Similar to looping, conditional branches can also be expressed in multiple ways:

      * via rule polymorphism in RuleDSL, where a different rule is invoked depending on the type or values of the rule parameter during DAG creation
      * write an Atom with a select logic, where one of the inputs is selected as output according to certain conditions at run time

    The first approach is more efficient as the branch condition is resolved during DAG construction. The second 
    approach is required for branching that depends on data at run time. Either of these options can be easily expressed in RuleDSL, without the 
    need for any special branching syntax.

### Capabilities and Use Cases

8. What are the ideal use cases for graph computing and Julius Graph Engine? 

    The Julius Graph Engine is well suited for any data and analytical use case. Julius adds more value to enterprise systems with complex data and analytical pipelines which tend to suffer more from poor transparency, lineage, scalability and visibility. Business decisioning that requires complex rules, regular updates, and quick responses are ideal applications for Julius as well. Opaque processes that demand explainability and auditability to minimize operational risk are also applicable. In addition, Julius excels at processing large data sets and heavy workloads because of its auto-scaling capabilities.
    
1. Can I use Julius for building machine learning applications and workflows?

    Definitely. A ML pipeline or workflow is by definition a DAG, and Julius can automatically create and execute them. Julius' computational DAG offers tremendous transparency, explainability and auditability for building ML pipelines and applications. It can incorporate all the steps in a typical ML pipeline, including data cleansing, feature engineering, training, inference and hyper parameter tuning. It also offers great ML Ops support, such as easy persisting and recovery of ML experiments. Please refer to Julius [tutorials](https://juliustechco.github.io/JuliusGraph) for examples of ML use cases.
    
1. Can Julius Graph Engine handle large data sets and heavy computational loads?

    Absolutely, Julius can automatically distribute the computational DAG to many computers, without the need for any code changes.  The ability to scale without code change is a huge advantage of Julius, as it allows for efficient parallel processing of large data set and heavy computations. This can facilitate the quick migration of a model from development to production. The distributed machine learning in Julius [tutorials](https://juliustechco.github.io/JuliusGraph) shows how easy it is to automatically distribute computational DAGs.

1. Does Julius Graph Engine support streaming and live use cases?

    Absolutely, the same computation DAG can run in either batch or streaming mode, without much code change. Please see the [tutorials](https://juliustechco.github.io/JuliusGraph) for examples of streaming use cases.

1. How big can Julius' computational DAG be?

    Julius Graph Engine can quickly create DAGs with tens of millions of nodes from a single computer. Julius also supports parallelism for DAG creation, so graphs with even billions of nodes can be efficiently created in parallel. Once created, Julius can automatically distribute the computations to hundreds of computers for efficient execution.

1. Are the intermediate results in the computational DAG cached by Julius?

    Yes, Julius automatically cache the intermediate results for every node in the computational DAG. The cached results are tremendously useful to both developers and users. This includes the ability to:

      * explain, audit and verify the correctness of the entire process 
      * debug and track issues 
      * enable fast scenario runs, as only dependent nodes needs to be re-computed from any input changes
      * facilitate adjoint algorithmic differentiation (AAD)

    The storage cost to cache all intermediate node level results in memory is small, as Julius can automatically distribute the computational DAG to a large number of computers and access an almost unlimited amount of memory.

1. How do I access and visualize intermediate results in the computational DAG?

    Julius comes with an intuitive and easy-to-use web UI, where a user can navigate the computational DAG and visualize all the intermediate data by simply clicking on individual nodes. All the data is accessible via Julius API as well. Please refer to the [tutorials](https://juliustechco.github.io/JuliusGraph) for examples of using the web UI and Julius API.

1. Does Julius Graph Engine support adjoint algorithmic differentiation (AAD) ?
    
    Yes, the Julius computational DAG supports AAD. The best part is that it doesn't need a tape, as all the primal calculations results are already cached in the DAG. Please refer to the [tutorials](https://juliustechco.github.io/JuliusGraph) for more information and examples on AAD.

### Integration

16. What programming languages can I use with Julius Graph Engine?

    Atoms can be written in any mainstream programming language such as C/C++, Python, Java, .Net, R and Julia etc. Existing data and analytical libraries written in these languages can be wrapped up as `Atoms` and used by Julius Graph Engine.

    The Julius Graph Engine also features easy-to-use APIs that can be called from any programming language. 

1. How do I convert my Python/C++/Java/.Net/R/Julia/SQL applications to Julius, and get the benefits of Graph?

    The great news is that your existing data and analytical libraries in these languages can be reused. You don't have to abandon your battle tested libraries and restart from scratch! The migration of an application or system to Julius involves two easy steps:
    
      * wrap the existing data and analytical classes and functions using the Julius' `Atom` interface. Julius offers generic wrappers that work out of the box for modern programming languages that support reflection, such as Python, Java, R, .Net and Julia etc. This generic reflection based Atom wrapper works automatically for any classes and functions in these languages. For older languages that do not support reflection such as C/C++, there is some additional effort needed to write Atom wrappers for individual functions and classes. But this work is largely mechanical and can be completed quickly by experienced developers. 
      * declare the entire data and analytical pipeline using Julius RuleDSL, which can reference and use the existing libraries via the `Atom` wrappers. This step only requires minimal effort and a small amount of coding, thanks to the low-code nature of RuleDSL. A complex data and analytical pipeline with hundreds or thousands of nodes can be built with a few dozen lines of rules in RuleDSL, as shown in Julius' [tutorials](https://juliustechco.github.io/JuliusGraph).
      
   The conversion is straight forward if the existing system is built in a modern programming language.  Our experience shows that a complex real world system can be fully converted in a few weeks by developers who are knowledgeable with the system's business logic and code base. For C/C++ applications and systems, it would require some more work for writing and testing the wrappers manually.

1. Can I mix and match Atoms written in different programming languages in the same computational DAG?

    Yes! Julius automatically takes care of the interop between them if these Atoms' inputs and outputs are all of standard types. Additional development work, such as serialization, is only required if you want to pass a non-standard object from one language to another.

1. How do I integrate Julius Graph Engine with an existing system or application?

    Existing systems and applications can access Julius' Graph Engine via Julius' easy-to-use APIs. Julius supports a low level API for Julia, C/C++ and Python clients, as well as a high level REST API that can be called from any programming language. The low-level API is faster and more granular, which is recommended for building high performing systems. The high-level API is easy to use and integrate, which is recommended for general use cases.
   
1. What databases and data sources does Julius support?

   Julius comes with a rich set of data connectors out of box, including relational databases, NoSQL databases (Hadoop/Spark etc), data files, web data sources etc. If you need additional data connectors Julius does not yet support, you can easily write your own connectors through the Atom interface, using any mainstream programming languages.
   
1. Can I use data visualization tools such Tableau and Qlik with Julius?

   Absolutely. Results from Julius graph can be fed into Tableau and Qlik for visualization and reporting.


### Installation
22. How do I install Julius?

    Julius installation is super easy: Julius ships with a single docker image. A client can simply install this docker image on whatever number of computers he/she chooses to run, which can be on a public cloud or private on-premise cluster. Julius only requires minimal configurations after installation, as most of the orchestration and configuration is handled automatically within the Julius docker container.
    
    Julius can also configure and host the installation in the cloud on behalf of the client.
  
1. What operating systems does Julius Graph Engine support?

    Both Linux and Windows.

1. What hardware environment can Julius Graph Engine run on?

    The Julius Graph Engine can be deployed to any cloud computer provider or private on-premise clusters in an organization.

1. How can a client protect its intellectual property when running the Julius Graph Engine in the cloud?

    The Julius Graph Engine can be integrated to a client's internal authentication process, so that only authorized personnel have access. Julius can be deployed on premise or in a single tenant environment on the cloud, providing additional protection. 

1. How much does it cost to license Julius?
   
   Developers can access and use Julius for free. The instructions to sign up for developer access is [here](https://github.com/JuliusTechCo/JuliusGraph). The cost of commercial licenses depend on the use case and the level of support required, please email info@juliustech.co for licensing questions. Julius does offer educational discounts for universities and other research institutions.

### Comparables

27. What is the main difference between the Julius Graph Engine from a collaborative development platform like Beacon?

    Platforms like Beacon offer integrated and collaborative development/deployment environments so that firms can be more efficient in managing and deploying complex code bases. In contrast, Julius Graph Engine attacks the problem from its root by dramatically reducing the amount of coding and efforts required for building complex systems. Using Julius, there is much less need for sophisticated collaborative development tools, as there is much less code to write and manage.

1. How does Julius Graph Engine's RuleDSL and computation DAG differ from Excel's worksheet formula and its dependency graph?

    Julius RuleDSL is much more generic and expressive than Excel's worksheet formulae. The RuleDSL supports both type and value based polymorphism, allowing sophisticated logic to be expressed succinctly. In comparison, Excel formulas are hard coded with specific cells or ranges. An Excel workbook often has thousands of formulae created by copy/paste, which is error prone and difficult to audit and change. 

    In addition, the Julius Graph Engine is much more performant and scalable than Excel, as it can handle large volume of data and computation by running in parallel on many computers. That allows Julius to be used as a production solution for enterprise systems, while Excel is mainly a personal and office application.

1. How does Julius Graph Engine differ from other software packages that also use computational DAGs, such as Dask, Tensorflow and Dagger.jl?

    Julius RuleDSL is specifically designed for efficient creation and execution of computational DAGs. It offers much better performance and scalability, as shown in our [tutorials](https://juliustechco.github.io/JuliusGraph) and [benchmark](https://juliustechco.github.io/JuliusGraph/dev/pages/t007_benchmark.html). In addition, Julius RuleDSL is low-code, and requires much less effort to implement the same functionality than other tools. This makes future adaptations and changes much easier as well.

1. The Julius Graph Engine sounds almost too good to be true, why hasn't anyone else done this before?

    The answer is twofold: the first is that there are a myriad of technological hurdles to overcome in order to design and implement such a generic and scalable graph computing solution; secondly the solution leverages many new technologies that have only become mature in recent years, such as cloud computing.

### Development Environment
31. What IDE does Julius support?

    Since RuleDSL is just regular code in plain text, developers are free to user their preferred IDEs. Jupyter lab/notebook and VScode are the most popular choices when working with Julius Graph Engine. 

1. How do I debug a large computational DAG?

    Julius offers efficient and easy-to-use tools for debugging. With the Julius web UI, a developer can quickly navigate and visualize every intermediate result in the DAG, allowing them to quickly track down bugs to individual nodes. Julius provides an API call for developers to download the entire state (including data and analytical logic) of any node in the distributed DAG, to recreate the error conditions on their local computer. Then the developer can use a debugger on a local computer to step through the execution to pin down the error. 

1. What if there is an error in the computational DAG?

    Julius offers great error handling and recovery capabilities. When an error occurs, the web UI will highlight the affected node and bring the user directly there with one click. By default, the DAG execution will halt until the error is corrected. Julius also supports a trigger mechanism that allows errors to be automatically reported and handled, so that the DAG execution can proceed even with errors.


