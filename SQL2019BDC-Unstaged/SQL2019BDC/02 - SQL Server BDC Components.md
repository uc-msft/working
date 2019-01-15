![](../graphics/microsoftlogo.png)

# Workshop: Microsoft SQL Server Big Data Clusters Architecture

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h1>SQL Server Big Data Cluster Components</h1>

In this workshop you'll cover using a Process and and various Platform components to create a SQL Server Big Data Cluster solution you can deploy on premises, in the cloud, or in a hybrid architecture. In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover the following topics in this Module:

<dl>

  <dt><a href="#2-0">2.0 SQL Server 2019 Big Data Clusters <i>(Stubbed, needs content, needs updated graphics, needs labs)</i></a></dt>
  <dt><a href="#2-1">2.1 Data Virtualization <i>(Stubbed, needs content, needs updated graphics, needs labs)</i></a></dt>
  <dt><a href="#2-2">2.2 Storage Pools <i>(Stubbed, needs content, needs updated graphics, needs labs)</i></a></dt>
  <dt><a href="#2-3">2.1 SQL Server 2019 Big Data Clusters <i>(Stubbed, needs content, needs updated graphics, needs labs)</i></a></dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png"><a name="2-0">2.0 SQL Server 2019 Big Data Clusters</a></h2>

SQL Server 2019 Big Data Clusters (BDC) provides three ways to work with large sets of data:

 - **Data Virtualization**: Query multiple sources of data technologies using the Polybase SQL Server feature
 - **Storage Pools**: Create sets of disparate data sources that can be queried as a single "Data Mart"
 - **SQL Server Big Data Clusters**: Create, manage and control clusters of SQL Server Instances that co-exist in a Kubernetes cluster with Apache Spark and other technologies to access and process large sets of data 

Each of these functions are available separately based on the requirements of your solution. You'll cover each of these components in the sections that follow, and the 

The next module covers planning the solution and creating the end-to-end system to support it using each of these components.

<h3><a name="2-1">2.1 Data Virtualization</a></h3>

Using a series of *connectors*, SQL Server BDC can query data using the PolyBase feature. PolyBase enables your SQL Server instance to process Transact-SQL queries that read data from external data sources. Starting in SQL Server 2019, you can access external data in Hadoop and Azure Blob Storage and external data in SQL Server, Oracle, Teradata, and MongoDB - as well as Generic ODBC sources. PolyBase pushes as much of the query as possible to the source system, which optimizes the query.

<br>
<img style="height: 150; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);" src="https://docs.microsoft.com/en-us/sql/big-data-cluster/media/big-data-cluster-overview/data-virtualization.png">
<br>

In PolyBase, you define the external table, configure the connection and security, and then use standard Transact-SQL statements to join and work with the data as if it were an internal table. 

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Description</b></p>

TODO: Enter activity description with checkbox

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>


<h2><a name="2-2">2.2 Storage Pools (aka Data Mart)</a></h2>

The storage pool consists of storage nodes comprised of SQL Server on Linux, Spark, and HDFS. All the storage nodes in a SQL big data cluster are members of an HDFS cluster. You can use these as a "Data Mart" construct to work with large sets of data stored on disparate data sources. 

Inside the Storage Pool, the Storage nodes are responsible for data ingestion through Spark, data storage in HDFS (Parquet format). HDFS also provides data persistency, as HDFS data is spread across all the storage nodes in the SQL big data cluster. The Storage Nodes also provide data access through HDFS and SQL Server endpoints.

<br>

<img style="height: 200; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);" src="https://docs.microsoft.com/en-us/sql/big-data-cluster/media/big-data-cluster-overview/data-mart.png">

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Description</b></p>

TODO: Enter activity description with checkbox

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>


<h2><a name="2-3">2.3 SQL Server Cluster Architecture</a></h2>

TODO: Topic Description

<br>

<img style="height: 400; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);" src="https://docs.microsoft.com/en-us/sql/big-data-cluster/media/big-data-cluster-overview/architecture-diagram-planes.png">

<br>

SQL Server Big Data Clusters can be installed in three ways:

 - Locally for Testing
 - In a Cloud Service
 - On premises

These architectures are not mutually exclusive - you can install some components on-premises, and others as a service. Your connections can interconnect across these environments. You'll explore more about installing SQL Server BDC in the <i>Planning, Installation and Configuration</i> module.


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Description</b></p>

TODO: Enter activity description with checkbox

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>


<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://docs.microsoft.com/en-us/sql/big-data-cluster/big-data-cluster-overview?view=sqlallproducts-allversions" target="_blank">Official Documentation for this section</a></li>
		<li><a href = "https://cloudblogs.microsoft.com/sqlserver/2018/09/26/sql-server-2019-celebrating-25-years-of-sql-server-database-engine-and-the-path-forward/" target="_blank">Update on 2019 Blog</a></li>
		<li><a href = "https://www.youtube.com/watch?v=-XgraEtnrF4" target="_blank">Introduction Webinar on Big Data</a></li>
		<li><a href = "https://info.microsoft.com/ww-landing-SQL-Server-2019-Big-Data-WhitePaper.html" target="_blank">Big Data Whitesheet</a></li> 
		<li><a href = "http://download.microsoft.com/download/8/B/6/8B643729-6224-4ECC-8C50-3292B8156F0E/SQL_Server_2019_Transform-Data_into_Insights_Infographic_EN_US.pdf" target="_blank">Infographic on Big Data</a></li>
		<li><a href = "https://docs.microsoft.com/en-us//sql/big-data-cluster/big-data-cluster-overview?view=sqlallproducts-allversions" target="_blank">Books Online on this topic</a></li>
		<li><a href = "https://www.dataonstorage.com/resource/video/msignite2018/brk4021-deep-dive-on-sql-server-and-big-data/" target="_blank">Session on Big Data at at Ignite</a></li> 
    <li><a href = "https://www.youtube.com/watch?v=gyiIB_6wfcI" target="_blank">Session on Containers at Ignite - Inside SQL Server containers - BRK4017</a></li> 
</ul>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/geopin.png"><b >Next Steps</b></p>

Next, Continue to <a href="03%20-%20Planning,%20Installation%20and%20Configuration.md" target="_blank"><i> Planning, Installation and Configuration</i></a>.
