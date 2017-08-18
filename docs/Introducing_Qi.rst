Introducing Qi
##############

.. contents:: Topics in this section:
    :depth: 3


Qi is a highly flexible cloud-based sequential data store that you use to store, retrieve, and analyze data. You 
create and write data to *streams* using a simple REST (*REpresentational State Transfer*) API (*Application 
Programming Interface*). The streams you create can be used to store simple or complex data types to suit 
your application needs. You can define simple or complex indexing to arrange and relate your data. An assortment 
of methods with customizable behaviors are available to read data and easily obtain needed information.


Access to Qi
------------

You must acquire a Tenant, security credentials, and a Namespace before interacting with Qi. If you do not 
have a Tenant, you can request access to the Qi Preview at `OSIsoft Cloud Services <cloudservices@osisoft.com>`__.

The Qi Preview program is limited, so contacting OSIsoft does not assure participation.


If you are chosen to
participate in the preview, you will receive an email notifying you of the name of your Tenant. 
Use the credentials you were provided to sign into the portal[EG1]. Signing in grants you access 
to additional functionality.



Architecture
------------

The primary object of the Qi architecture is the *tenant*. Within a tenant you create one or more 
*Namespaces*, in which data types are defined and data is stored. 

.. image:: images/ContainersA.png

You use Namespaces to separate tenants into logical entities. For example, 
you might want to have one Namespace for production, one for development, and 
perhaps another to serve as a pre-production staging area where your QA 
group can run certification testing.

Within a Namespace, Qi defines three different objects in which to store and manage data:

-  **Type**: A user-defined structure that denotes a single measured event or
   object for storage. In Qi, a type is called a QiType.
-  **Stream**: A basic unit of storage consisting of an ordered series of
   objects that conform to a type definition. In Qi, a stream is called a QiStream.
-  **Stream Behavior**: Defines how Qi interpolates or extrapolates
   data during event retrieval when requests occur before, after, or between
   existing data events.

.. image:: images/Containers_1A.png

Each Namespace stores a separate and independent list of Type, Stream, and Stream Behavior objects.

Product prerequisites
---------------------

To use the Qi REST API in your applications, make sure you have
the following:

-  A computer
-  A set of tools that you feel comfortable using to consume and use
   RESTful Web Services
-  If consuming the .NET Qi Client Libraries, you must be using tools
   capable of using the .NET 4.5.2 Runtimes in your environment
-  A Qi Preview tenant from OSIsoft and corresponding set of OAuth2
   authentication keys


Getting help
------------

The following email address is available to participants of the Qi
Preview for both product support and feedback:

`QiSupport@osisoft.com <mailto://QiSupport@osisoft.com>`__

The OSIsoft team will respond to all support requests as
quickly as possible during business hours (Pacific Time).


Security
--------

There are two types of security accounts for Qi users:

+----------------+------------------------------------------------------------------+
| Account Type   | Description                                                      |
+----------------+------------------------------------------------------------------+
| Administrator  | Accounts with administrator authority are allowed to perform all |
|                | CRUD (Create, Read, Update, Delete)                              |
|                | operations on Qitype, stream, and stream                         |
|                | behavior objects. Accounts also allowed to read and write data   |
|                | to streams                                                       |
+----------------+------------------------------------------------------------------+
| User           | Accounts with user authority are allowed read operations on      |
|                | Qi objects and allowed to read data from streams                 | 
+----------------+------------------------------------------------------------------+

Code samples
------------

Code samples for Python, .NET, Node.js, and Java can be found in the
Qi-Samples repository on GitHub. Obtain Qi REST API access keys from
`qi.osisoft.com <https://qi.osisoft.com>`__ before running the sample code.



