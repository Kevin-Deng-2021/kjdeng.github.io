---
layout: post
title:  Cloud Dataware house solution, what and how?
date:   2020-03-01 10:48:16
description: Snowflake and Teradata
---
In 2020, many technology companies spend on developing its own cloud-based data warehouse solution. 
Different than a typical local database or semi-cloud database, some service like Snowflake is basically 100% cloud-based DAAS (Data Warehouse As A Service.)
Cloud-based services benefit computing speed, cost, storage, and security, especially the flexibility on computing and storage resource usage.
Micro-Partition is one of the important database technologies which provides many key functions and solutions for enterprise. 


#### Data Warehouse Key Metrics
<ul>
	<li>Robustness of SQL</li>
	<li>Built-in optimization</li>
	<li>On-the-fly elasticity</li>
	<li>Dynamic Environment Adaption</li>
	<li>Separation of computing from storage</li>
	<li>Support for diverse data</li>
</ul>

In terms of using SQL to parse or fetch data from a data warehouse, the SQL command or language will not be much different. 
Most of the cloud dataware house services follows ANSI, which is the most common standard. 
Exact command like SELECT, DELETE, DROP, etc. On top of that, S


<hr>
<br/>
It will be powerful functions if the dataware house can let users easily command in SQL for clone or temporary tables. 
With micro-partition infrastructure, the service can ‘CREATE OR REPLACE’ a table at the same time without deleting or dropping first, and using much less resource. 
It even can ‘time travel’ datasets, database, table, so the user can get data at the specific past moment (hours to days.) 

<blockquote>
	<li>The cloud now offers attractive options with better economics, such as pay-as-you-go which
is easier to justify and budget, better logistics (streamlined administration and management),
and better scale (elasticity and the ability to expand a cluster within minutes).</li>
<br/>
	<li>Many enterprises are fully embracing a cloud-based analytics strategy and making it
accessible across their current infrastructure and data ecosystems. Many others are
adopting it as a secondary platform for purposes such as disaster recovery and offloading
analytic and data transformation workloads.</li>
<br/>
	<li>Depending on needs, customers may choose to weight the Disruption Vectors differently
than we have here. Ultimately all of these databases are viable. You should know what
you’re acquiring, what you are missing and what it is costing you.</li>
<br/>
	<li>Being “born in the cloud” does appear to offer advantages. While on-premises-first
development brings a robust database to the table, not all functions are always part of the
cloud solution and not all of the organizations behind them have made the transition to
cloud.</li>
<br/>
	<li>Down the road, cloud database capabilities will likely include being able to dynamically spin
up a cloud instance, migrate workloads, and synchronize small-scale data on the fly.</li>
<br/>
	— William McKnight
</blockquote>

<div>
	<img class="col three caption" src="{{ site.baseurl }}/img/datawarehouse_comparing.png" >
</div>

Snowflake support with JDBC or ODBC connection, which means you can use normal SQL interface software to connect. It’s like a teradata studio regarding Teradata. You can use ‘SQL Assistant’, ‘DBeaver’ to connect.
