#Zuora Query for Python

Zuoraquery is an easy way to query the Zuora SOAP API using Zuora's query language ZOQL.

For more information on ZOQL: https://knowledgecenter.zuora.com/DC_Developers/SOAP_API/M_Zuora_Object_Query_Language

##Installation
```python
pip install zuoraquery
```

##Example
```python
import zuoraquery

user = 'mike@example.com'
pw = 'examplepassword'
wsdl_file_path = 'C:\Users\Download\zuora_wsdl_file.wsdl'
query = "select accountid,amount from payment where createdDate = 2016-06-01T00:00:00"

zuoraquery.z_query(user,pw,wsdl_file_path,query)
```

Maximum results returned in ZOQL query is 2000 results.

Larger datasets must be iterated through to receive full dataset by passing the querylocator id as follows:

```
zuoraquery.z_query_more(query_locator)
```

##Author

[Mike Peralta] (https://twitter.com/MichaelPeralta) 
