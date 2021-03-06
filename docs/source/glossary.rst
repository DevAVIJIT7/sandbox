Glossary
========

DataONE Terms
~~~~~~~~~~~~~

.. glossary::

  DataONE
    Data Observation Network for Earth

    https://dataone.org


  DataONE Common Library for Python
    Part of the DataONE :term:`Investigator Toolkit (ITK)`. Provides
    functionality commonly needed by projects that interact with the
    :term:`DataONE` infrastructure via Python. It is a dependency of
    :term:`DataONE Client Library for Python`, :term:`GMN` and currently all
    other DataONE components written in Python.


  DataONE Client Library for Python
    Part of the DataONE :term:`Investigator Toolkit (ITK)`. Provides
    programmatic access to the DataONE infrastructure and may be used to form
    the basis of larger applications or to extend existing applications
    to utilize the services of DataONE.


  GMN
    DataONE Generic Member Node

    GMN is a complete implementation of a :term:`MN`. It provides an
    implementation of all MN APIs and can be used by organizations to expose
    their science data to DataONE if they do not wish to create their own,
    native MN. GMN can also be used as a workbone or reference for a 3rd party
    MN implementation. If an organization wishes to donate storage space
    to DataONE, GMN can be set up as a :term:`replication target`.


  Metacat
    Metacat is a flexible, open source metadata catalog and data repository that
    targets scientific data, particularly from ecology and environmental
    science. Metacat accepts XML as a common syntax for representing the large
    number of metadata content standards that are relevant to ecology and other
    sciences. Thus, Metacat is a generic XML database that allows storage,
    query, and retrieval of arbitrary XML documents without prior knowledge of
    the XML schema.

    Metacat provides a complete implementation of all :term:`MN` APIs.

    http://www.dataone.org/software-tools/metacat


  Replication target
    A :term:`MN` that accepts replicas (copies) of science data from other MNs
    and thereby helps ensuring that science data remains available.


  Vendor specific extensions
    Functionality that is not part of the DataONE APIs but is supported by a
    DataONE component. Vendor specific extensions are activated by adding custom
    HTTP headers when calling the existing DataONE API methods. When activated,
    they modify the behavior of the method in a vendor specific way. DataONE has
    reserved the namespace starting with `VENDOR_` for such custom headers.


  Investigator Toolkit (ITK)
    The Investigator Toolkit provides a suite of software tools that are useful
    for the various audiences that DataONE serves. The tools fall in a number of
    categories, which are further developed here, with examples of potential
    applications that would fit into each category.

    http://mule1.dataone.org/ArchitectureDocs-current/design/itk-overview.html


  MN
    DataONE Member Node.


  CN
    DataONE Coordinating Node.


  client
    An application that accesses the DataONE infrastructure on behalf of
    a user.


  SciData
    An object (file) that contains scienctific observational data.


  SciMeta
    An object (file) that contains information about a SciData object.


  SysMeta
    An object (file) that contains system level information about a SciData or a
    SciMeta object.


  Workspace
    The Workspace is an online storage area where users can store search filters
    and references to DataONE objects. It follows the files and folders metaphor
    of regular filesystems. Objects are added to the Workspace from the
    ONEMercury search engine.


Authentication and security
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

  X.509
    An ITU-T standard for a public key infrastructure (PKI) for single sign-on
    (SSO) and Privilege Management Infrastructure (PMI). X.509 specifies, amongst
    other things, standard formats for public key certificates, certificate
    revocation lists, attribute certificates, and a certification path validation
    algorithm.

    http://en.wikipedia.org/wiki/X509


  CA
    Certificate Authority

    A certificate authority is an entity that issues digital :term:`certificate`
    s. The digital certificate certifies the ownership of a public key by the
    named subject of the certificate. This allows others (relying parties) to
    rely upon signatures or assertions made by the private key that corresponds
    to the public key that is certified. In this model of trust relationships, a
    CA is a trusted third party that is trusted by both the subject (owner) of
    the certificate and the party relying upon the certificate. CAs are
    characteristic of many public key infrastructure (PKI) schemes.

    http://en.wikipedia.org/wiki/Certificate_authority


  CA signing key
    The private key which the :term:`CA` uses for signing :term:`CSR`\ s.


  Server key
    The private key that Apache will use for proving that it is the owner
    of the :term:`certificate` that it provides to the client during the
    SSL handshake.


  CSR
    Certificate Signing Request

    A message sent from an applicant to a :term:`CA` in order to apply for a
    :term:`certificate`.

    http://en.wikipedia.org/wiki/Certificate_signing_request


  Certificate
    A public key certificate (also known as a digital certificate or identity
    certificate) is an electronic document which uses a digital signature to bind
    a public key with an identity -- information such as the name of a person or an
    organization, their address, and so forth. The certificate can be used to
    verify that a public key belongs to an individual.

    http://en.wikipedia.org/wiki/Public_key_certificate


  CA certificate
    A certificate that belongs to a :term:`CA` and serves as the root
    certificate in a term:`chain of trust`.


  Self signed certificate
    A :term:`certificate` that is signed by its own creator. A self signed
    certificate is not a part of a :term:`chain of trust` and so, it is not
    possible to validate the information stored in the certificate. Because of
    this, self signed certificates are useful mostly for testing in an
    implicitly trusted environment.

    http://en.wikipedia.org/wiki/Self-signed_certificate


  Chain of trust
    The Chain of Trust of a Certificate Chain is an ordered list of
    certificates, containing an end-user subscriber certificate and intermediate
    certificates (that represents the Intermediate CA), that enables the
    receiver to verify that the sender and all intermediates certificates are
    trustworthy.

    http://en.wikipedia.org/wiki/Chain_of_trust


  DN
    Distinguished Name. Information in a :term:`X.509` certificate that uniquely
    identifies something. In DataONE, the DN is used for identifying the owner
    of the certificate. The owner can be either a physical person or a software
    system that is part of and/or that interacts with the DataONE
    infrastructure.


  OpenSSL
    Toolkit implementing the :term:`SSL` v2/v3 and :term:`TLS` v1 protocols as
    well as a full-strength general purpose cryptography library.


  SSL
    Secure Sockets Layer

    A protocol for transmitting private information via the Internet. SSL uses a
    cryptographic system that uses two keys to encrypt data − a public key known
    to everyone and a private or secret key known only to the recipient of the
    message.


  SSL handshake
    The initial negotiation between two machines that communicate over SSL.

    http://developer.connectopensource.org/display/CONNECTWIKI/SSL+Handshake

    http://developer.connectopensource.org/download/attachments/34210577/Ssl_handshake_with_two_way_authentication_with_certificates.png


  TLS
    Transport Layer Security

    Successor of :term:`SSL`.


  Client side authentication
    :term:`SSL` Client side authentication is part of the :term:`SSL handshake`,
    where the client proves its identity to the web server by providing a
    :term:`certificate` to the server. This is the opposite of :term:`server
    side authentication`, in which the server authenticates itself to the
    client. Server side authentication is mandatory and client side
    authentication is optional in the SSL/TLS protocol. Both types of
    authentication are used between DataONE Nodes. Only server side
    authentication is used between DataONE Nodes and DataONE clients.

    The certificate provided by the client must be signed by a :term:`CA` that
    is trusted by the server. In the DataONE infrastructure, client side
    certificates are issued by the DataONE CA, which must be trusted by all
    Nodes.

    The server validates the client side certificate and permits access to the
    APIs and Science Objects for which the subject (:term:`DN`) in the
    certificate has been granted access. Connecting to a Node without providing
    a certificate will cause the Node to consider the client to be
    unauthenticated and allow access only to objects and functionality that is
    available to public, untrusted subjects. Typically, this means that no
    create, update or delete operations can be performed.


  Server Side Authentication
    :term:`SSL` Server Side Authentication is part of the :term:`SSL handshake`,
    where the server proves its identity to the client by providing a
    :term:`certificate` to the client. This is the opposite of :term:`client
    side authentication`, in which the client authenticates itself to the
    server. Server side authentication is mandatory and client side
    authentication is optional in the SSL/TLS protocol. Both types of
    authentication are used between DataONE Nodes. Only server side
    authentication is used between DataONE Nodes and DataONE clients.

    The certificate provided by the server must be a valid certificate issued by
    a publicly trusted :term:`CA` such as VeriSign or Thawte.


  Client side certificate
    :term:`Certificate` that is provided by the client during :term:`client side
    authentication`.


  Server side certificate
    :term:`Certificate` that is provided by the server during :term:`server side
    authentication`.


  Identity Provider
    A system that authenticates users and provides identity assertions.

    Typically, an Identity Provider accepts a username and password from a
    person and, after succesful validation, issues a security token. The person
    then uses the token to prove their identity on systems that trust the
    Identity Provider.


Misc
~~~~

.. glossary::

  Subversion
    Version control system

    http://subversion.apache.org/


  Bash
    GNU Bourne-Again Shell

    http://www.gnu.org/software/bash/


  Apache
    HTTP server

    http://httpd.apache.org/


  MPM
    Multi-Processing Module

    The component within Apache that manages the processes and threads used for
    serving requests.

    http://httpd.apache.org/docs/2.0/mpm.html


  Python
    A dynamic programming language.

    http://www.python.org


  Django
    High-level Python Web framework that encourages rapid development and clean,
    pragmatic design.

    https://www.djangoproject.com/


  WSGI
    Web Server Gateway Interface

    http://www.wsgi.org/wsgi/


  mod_wsgi
    An :term:`Apache` module that implements :term:`WSGI`.


  mod_ssl
    An :term:`Apache` module that interfaces to :term:`OpenSSL`.


  PyXB
    Python XML Schema Bindings

    http://pyxb.sourceforge.net/


  lxml
    A library for processing XML and HTML with Python

    http://lxml.de/


  minixsv
    A Lightweight XML schema validator

    http://www.familieleuthe.de/MiniXsv.html


  python-dateutil
    Extends the standard datetime module

    http://labix.org/python-dateutil


  PostgreSQL
    A freely available object-relational database management system (ORDBMS).

    http://www.postgresql.org/


  MySQL
    A freely available object-relational database management system (ORDBMS).

    http://www.mysql.com/


  SQLite3
    A freely available object-relational database management system (ORDBMS).

    http://www.sqlite.org/


  Oracle
    A object-relational database management system (ORDBMS) that is available
    in both free and commercial versions.

    http://www.oracle.com/


  Psycopg2
    Psycopg is a PostgreSQL database adapter for :term:`Python`.

    http://initd.org/psycopg/


  OpenSSL
    An open source implementation of the Secure Sockets Layer (SSL v2/v3) and
    Transport Layer Security (TLS v1) protocols as well as a full-strength
    general purpose cryptography library.

    http://www.openssl.org/


  cron
    cron is a time-based job scheduler in Unix-like computer operating systems.
    cron enables users to schedule jobs (commands or shell scripts) to run
    periodically at certain times or dates.


  python-setuptools
    A package manager for Python

    http://pypi.python.org/pypi/setuptools


  ISO8601
    International standard covering the exchange of date and time-related data

    http://en.wikipedia.org/wiki/ISO_8601


  python-iso8601
    Python library implementing basic support for :term:`ISO8601`

    http://pypi.python.org/pypi/iso8601/



  CILogon
    The CILogon project facilitates secure access to CyberInfrastructure (CI).

    http://www.cilogon.org/


  LOA
    Levels of Assurance

    CILogon operates three Certification Authorities (CAs) with consistent
    operational and technical security controls. The CAs differ only in their
    procedures for subscriber authentication, identity validation, and naming.
    These differing procedures result in different Levels of Assurance (LOA)
    regarding the strength of the identity contained in the certificate. For
    this reason, relying parties may decide to accept certificates from only a
    subset of the CILogon CAs.

    http://ca.cilogon.org/loa


  REST
    Representational State Transfer

    A style of software architecture for distributed hypermedia systems such as
    the World Wide Web.

    http://en.wikipedia.org/wiki/Representational_State_Transfer


  SolR
    Apache Solr

    Solr is the popular, blazing fast open source enterprise search platform
    from the Apache Lucene project. Its major features include powerful
    full-text search, hit highlighting, faceted search, dynamic clustering,
    database integration, rich document (e.g., Word, PDF) handling, and
    geospatial search. Solr is highly scalable, providing distributed search and
    index replication, and it powers the search and navigation features of many
    of the world's largest internet sites.

    http://lucene.apache.org/solr/


  OAI-ORE Resource Map
    Open Archives Initiative Object Reuse and Exchange (OAI-ORE) defines
    standards for the description and exchange of aggregations of Web resources.

    http://www.openarchives.org/ore/1.0/