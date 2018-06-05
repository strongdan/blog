##What is a Data Lake?

_This is a guest post from Austin-based business analytics firm [Tenfold](https://www.tenfold.com/)_

On the early days of modern computation, computers of the 1950s, 60s, and 70s would collect data from physical repositories (cards, keyboard input and tapes) and deal with it in memory, meaning a virtual environment.

In the late 1970s, computers started to cluster data for processing within worksheet alike structures, the grandfather of DataBases.

DataBases were to follow and the logic behind it was for data to be input in a logical manner according to previous human classification, so although raw data (in the sense it hadn’t been previously treated) went into the Database tables, the decision of what would fit where and why was based on human criteria.

Databases are in fact a limited tool since they require specific contexts, meaning there is a Database for Accounting Data which must be a distinct entity than the Database for Logistics Data (although they may need to connect and have mutual referencing structures).

So, most of the Systems and Tools under operation today, still have their own Database structures which interconnect and exchange data towards creating added value information.

The Database evolved to larger clusters of alike data, which are the Data Warehouses and, although the process may somehow differ, Data is grouped in the same manner while pertaining a given common context.

With the event of BigData (for Data tends to grow, exponentially), plus nowadays innovation in data handling/ processing tools, we have reached a stage where large flows of several types of Data may be channeled into extremely large data repositories (Data Lakes), in an ad-hoc manner which nevertheless allows correlation to be established under pre-defined “schema” where from to extract meaningful information.

The main leverage of Data Lakes pertains the following characteristics:

* While Data Warehouses store structured already processed Data, Data Lakes also store semi or unstructured as well as completely raw and (apparently) unrelated data. And, no … it’s not a waste of time and space since most times relationships are only found after processing.
* Data Warehouses architecture implies expensive large data volumes whereas Data Lakes are specifically designed for low-cost
* Data Warehouses obey by a pre-defined structure in which data is stored (pre-defined data classes and families), while Data Lakes have great flexibility towards dynamic structural configuration. And that is more the manner in which humans apprehend information and think.
* Data which goes into Data Warehouses is mature (it has a clearly defined context), yet Data Lakes store Data that is still maturing (still finding its place in the overall context).

By now you should be realizing that without Data /Lakes, the IoT or even AI would be heavy, slow or even impossible technologies to implement in a cost-effective manner.

Think of it as an actual lake, into which data flows from several streams (M2M, log files, real-time data collection, CTI, … you name it …) and then you are able to run appropriated analytics towards it, therefore extracting added value information.

Accessing data from different sources like DB2 based systems or SAP, or any other different IT Systems requires both specific tools as well as licensing, which represents time and money.

Extracting meaningful new added value information out of those distinct IT environments represents creating a detailed map of WHAT data is relevant towards WHICH requirements and then developing code that can gather such Data in the appropriate sequence to produce information that shows new meaningful content.

Let’s imagine one example where your company needs to undergo a Market Analysis on trends and tendencies of a specific group of prospects (potential clients) towards who you wish to promote a new item on your offering portfolio.

Such exercise, if done over existing corporate systems’ existing Databases or Data Warehouses implies getting the accurate answers to the following questions:

* Clearly identifying WHAT characterizes valid Data, meaning Data that pertains prospects who bear the high potential of becoming clients of such new product or service now entering the corporate portfolio?
* WHERE in the different corporate systems’ Data Warehouses lays such data?
* WHICH types or families of Data represent the most potential towards assertively qualifying the prospects with higher potential?
* HOW shall the code that enables such accurate data collection and processing be developed (programming languages, processing logic leading to step stone creation of added value content and so on …)?
* WHAT are the required computing and storage resources that enable the fastest possible processing of all the Data that may be found relevant?
* WHEN could we expect the first results?
* WHICH is the expectable percentage of “false positives”, deviations and errors?
* HOW much will it cost? Is it worthwhile the waiting or once we get the information we need, time to market will be just history?

Data Lakes are an inevitable consequence of widespread access and integration as well as social and tech trends like Social Media or IoT will only make them more common.

However, if there was a cost-effective way to do it, by cross-referencing the Data that you have about those prospects in your corporate systems (including saved conversations over the phone) with a “photographic profile” that you can extract about each of them from, let’s say Social Media, pouring everything into one single dynamically scalable repository (therefore with no need to constantly move data around between existing systems), just within a few hours or even minutes, what would that represent for the potential of successfully launching your new product or service?

A Data Lake needs to enable the features to embed in the ISASA concept which specifically represents the ability to:

* Ingest data from several distinct flow streams through appropriate APIs or Batch processes.
* Store such dynamically unforeseen in size amounts of Data on scalable repositories (the Lake) through all necessary protocols (NFS, CIFS, FTP, HDFS, other)
* Analyze the Data by finding the relevant correlations according to your needs and expectations.
* Surface relevant information in a user-friendly manner that better conveys what you need to see in the most straightforward effective way.
* Act, in the most efficient and cost-effective manner leading you to reach the intended goals.

##The Process

A Data Lake is not the solution to your problem, yet the IT Landscape that will allow you to get there fast and accurately, and that means as in most cases in life that you need to begin by clearly understanding the intended outcome and defining concrete tangible goals, so:

* Start by determining your Business Objectives
* Define and collect the data that will enable you to reach your Business Objectives
* Identify what Success will look like for you

In the above-mentioned case, of your company going after clients for your new product or service, these would translate by:

* Assertively leveraging the value proposition towards the prospects.
* Targeting the right prospects (the ones who will most likely buy the product or service, therefore, becoming clients).
* Increase Sales and Revenue.

##Data Lake Architecture

Still considering our case, a company launching a new Portfolio Item, the Structure that needs to be set in place will resemble the following picture.

##Data Sources

The Data Sources Layer provides data streams from Corporate systems or other sources of both structured or raw data via APIs or other plug-ins regardless of origin storage format.

Processing and Storage Layer

The processing layer starts with Security towards the data streams which mean:

* Visibility classification and control (Authorizations and Permissions)
* Multi-Level stratification: Clustering, DataSets and Attributes
* Labelling towards highly sensitive classes of data
* Authorization Views

The appropriate processing structure needs to define which allows adequate processing of required data extracting valuable information. Here the following steps need to be defined:

* Process and rules towards establishing Joins, Aggregations, and Correlations
* Which will be Streaming and which will be Batching based
* Error track& Tracing, Registry, and Resolution (Data Exceptions, Error Logs, Correction Tables)
* False Positives detection (wrong data types, duplicated data, masking)
* Required specific transformation algorithms that provide business-specific focused new data

##Integration Layer

Upon achieving the collection of valuable information and data out of the processing over the Data Lake content it must be either integrated back on Corporate Systems and/ or made available for several types of user profiles, who according to their roles and responsibilities will use it to leverage and gain efficiencies, such as the role of Integration and Governance.

##User Interfacing Layer

Distinct user profiles will need to visualize data and information in different manners, some more holistic while other more detailed and exposing details and correlations.
Support Tools

As previously mentioned, although Data Lake content processing could be achieved via entirely “homemade” software tools, developing the entire required suite would represent a huge project by itself each time some analysis which requires the use of a Data Lake is in order.

Fortunately, there are several “off the shelves” tools that can be merely configured towards the herein previously mentioned stages and layers of a Data Lake workflow, therefore minimizing the internal effort towards developing code that achieves certainly required functionalities. These can be visually represented towards their specific context of actuation as shown in the picture below.

A bit of advice; tools are growing as flowers in Springtime, make sure to choose not more than the necessary toolkit as per your specific needs and no single two which perform the same role.

Best Practice Towards Implementing a Data Lake

Here are the best practices key elements upon setting up the endeavor towards creating a Data Lake:

* Focus on Architecture which best addresses available data
* The Data Lake needs to be created according to available Data Sources and Type and not according to what is required. Although this may seem counterintuitive, the fact is that your Data structure at the end is not totally devisable when you start the process.
* The Data Lake design must be guided by which type of data will you be able to dispose of during processing and not what will be useful.
* Like the only way to eat an Elephant is to split it into small portions, you should do the same here, meaning Discovery & Ingestion, Storage & Administration, Quality & Transformation and Visualization & Interaction must be addressed separately.
* Focus on native Data Types
* All the architecture components must be able to deal with data in their native format.
* All architecture components must be set in place while being fully aligned with the type of processes and procedures inherent to the specific Market Vertical requirements that the Data Lake will address.
* Service and Governance
* You must assure that the Data Lake structure and processing are capable of fast Data Ingestion independently of its source, not to create a bottleneck at the very beginning of the entire process.
* Data profiling, security, and policies must be defined in advance as well as tagging, correlation rules, and workflows
* Querying
    Proper strong and agile querying processes must be defined and set in place, or the Data Lake will not be responsive as per your Time to Market requirements.
    Proper “guidelines” (algorithms and codding) that allows swift discovery of correlations and unification criteria, must be clearly defined in advance.
    Analytics that mirror human expectations and goals, are most relevant to allow gathering and clustering/ correlation of data that meets those human-driven
    Metadata
    A proper Metadata Catalog needs to be defined in advance, so the Data Lake has the capacity to properly allocate Data has it is being ingested.
    And the process must be fully automated in order not to cause errors os processing blockages.

Bottom line, you must “teach” the Data Lake to “think”.
Data Lake “Core Structures”

How is it possible for Google or Facebook to deal with such large colossal volumes of information simultaneously?

Do you realize that Data will increase exponentially as the IoT expands? We are now gathering data from Cell Phones, Social Media, Cars, Media, Coffee Machines (!!!) and so many other sources that were unthinkable just 5 years ago.

How will we be able to correlate data from such a huge number of streams in a manner that allows us to “see the big picture” in a way never seen before?
Hadoop

In the beginning of our 21st Century, Google was becoming unable to scale their “traditional” Database Engines and processing capabilities in any manner that could deal with the exponentially large amount of new Data flowing in every second, so a new approach was developed an algorithm (called Map Reduce), that started by splitting and channelling Data as it arrived towards separated processing capacities according to its classification. Meaning, XML would be forward for processing to dedicated processing clusters as well as Text, SQL, Logs, Objects and so on would flow to other separated dedicated processing clusters.

This approach was later on used to create an open source initiative that would further as faster foster the evolution of such new “Tech” in a manner that could timely generate results which could keep up with the momentum of Data Streams Growing Volumes, and Hadoop was born.

So, Hadoop allows Data to be processed in parallel in extremely large volumes while maintaining existing and establishing new meaningful correlations.

Only, Hadoop was heavily dependent of coding, in Java, to adapt it towards each specific new context and to overcome the time-consuming endeavor of doing so, the market saw the rise of previously mentioned Tools (Kafka, HIVE, Spark …).
Cassandra

We can say that Cassandra if Facebook’s SQL based Hadoop, and we wouldn’t be far from being accurate.

By default, and having had its development based on a Database Engine architecture, Cassandra works by default in multi-node Clustering mode, therefore the Data is not “merely” spread across processing nodes to split the necessary workload, it is done so at the Database Engine level, therefore not burdening the processing with yet that additional task.

This allows processing capacity to be automatically scaled just by adding new nodes to the DB cluster.

The cluster nodes are all primary nodes, therefore there are no Master and Slave instances, all have the same degree of priority and command & control over the Data handling process, which assures full fault tolerance in case of clustering downtime or communications interruption.
What Sets Them Apart

Hadoop was designed to deal with large amounts of unstructured Data bearing the capacity to process them in parallel and delivering results in a fast-effective manner, and for that purpose, it is usually implemented within a single IT Landscape which further enhances its Operational Approach to Data Processing and Management.

Cassandra, on the other hand, was designed to allow redundant multi-node + multi-geographical simultaneous fault-tolerant parallel data processing capacity, nevertheless, it requires a structured Data Model before its implementation.

This means that Hadoop is very useful for Data Ingestion, Analytics and initial Processing, while Cassandra can enter the workflow later on allowing and assuring further detailed Processing, Security, Storing and Consultation anytime/ anywhere, once the data has been cataloged in a structured manner.
Leveraging Business

Coming back to our company which is launching this new product, and considering an example that comprehends a complete range of available data, meaning existing clients how can a Data Lake supported on this Technological Landscape support the several teams on their roles?

The Data Lake will collect a full data catalog about the clients, like invoicing terms, overdue payments, preferences (via recorded phone conversations, the CRM system or Social Media), product handling capacity (out of the SCM corporate system) and so on …

Then the Data will be processed in a manner towards identifying high-potential prospects for the new product or service, meaning as an example: who has no open payments towards the company + has demonstrated an interest in features that the new product will deliver + has the SCM capacity to deal with it.

This information can then be delivered in different formats, either CxO/ Management reporting style or on demand/ on click upon some phone contact from the client side to Customer Support Hot Lines or from the company Sales and Marketing Department towards the prospect, immediately identifying that current client as a high potential prospect to acquire the new product or service.

How valuable would it be for you, if anytime you either contact a client or the client contacts you, your IT intel installed capacity automatically and accurately informs you of the new additional business potential towards that client?
Where are we Heading?

Being a new field of Computing, which most large corporations do not use yet since their entire IT Landscape (which has been evolving over decades) is necessarily constituted by Systems in “silos” which then interchange Data via API or other interconnect channels, there are several expectations like:

    Can Data Lake ease the burden of ITL? By making it either less time consuming or complex?
    Will we be able to apply several multiple “schemas” over one given Data Lake, simultaneously, and by doing so leveraging multiple “efficiencies” over existing data?
    Will we be able to finally reach “cross-organizational” Data, so instead of having the Data about one given client or partner that Accounting accesses plus other Data about the same 3rd party that Logistics accesses and so on … having a Full Integrated Data Profile about it, which everyone accesses although according to profile permissions? Since the Data Warehouse did not do the trick, isn’t it possible that a Data Lake is just a new name for Data Mart version 2.0?

The entire concept of capturing raw data and applying distinct Schemas to it (logical circumstantial processing) is a very powerful one and in fact, it is precisely what our brain does. We gather raw data and based on our knowledge (rules gathered through past experience and learning) we are able to “issue” a new set of Data that adds value to what we have collected and had stored as “knowledge”.

And this … has everything to do with Artificial Intelligence.
