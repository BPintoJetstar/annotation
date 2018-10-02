# Motivavion
XML was conceived as a solution to this kind of problem (intercommunication); it is meant to make passing data between
different components much easier and relieve the need to continually worry about different formats
of input and output, freeing up developers to concentrate on the more important aspects of coding
such as the business logic. 
XML is also seen as a solution to the question of whether files should be
easily readable by software or by humans; XML’s aim is to be both
Browsers use an XML stylesheet or transformation to display XML files. An XML stylesheet is a textbased file with an XML format that can transform one format into another. They are most commonly
used to convert from a particular XML format to another or from XML to HTML, but they can also
be used to process plain text

# Uses
One of the aims of XML is to implement a clear separation between data and presentation.
This means that the same underlying data can be used in multiple presentation scenarios. It also
means that when moving data, across a network for example, bandwidth is not wasted by having
to carry redundant information concerned only with the look and feel. This separation is simple
with XML as there are no built-in presentational features such as exist in HTML, and is one of
its main advantages

# XML origin
XML was developed by an XML Working Group (originally known as the SGML Editorial Review Board) formed under the auspices of the World Wide Web Consortium (W3C) in 1996. It was chaired by Jon Bosak of Sun Microsystems with the active participation of an XML Special Interest Group (previously known as the SGML Working Group) also organized by the W3C. The membership of the XML Working Group is given in an appendix. Dan Connolly served as the WG's contact with the W3C.

The design goals for XML are:

XML shall be straightforwardly usable over the Internet.
XML shall support a wide variety of applications.
XML shall be compatible with SGML.
It shall be easy to write programs which process XML documents.
The number of optional features in XML is to be kept to the absolute minimum, ideally zero.
XML documents should be human-legible and reasonably clear.
The XML design should be prepared quickly.
The design of XML shall be formal and concise.
XML documents shall be easy to create.
Terseness in XML markup is of minimal importance.
This specification, together with associated standards (Unicode and ISO/IEC 10646 for characters, Internet RFC 1766 for language identification tags, ISO 639 for language name codes, and ISO 3166 for country name codes), provides all the information necessary to understand XML Version 1.0 and construct computer programs to process it.

This version of the XML specification may be distributed freely, as long as all text and legal notices remain intact.

# XML structure

`<?xml version="1.0" encoding="UTF-8"?>`

// more tags

# Namespaces
Basically, namespaces serve as a way of grouping XML.
XML Namespaces provide a method to avoid element name conflicts.The namespace can be defined by an `xmlns` attribute in the start tag of an element.The namespace declaration has the following syntax:`xmlns:prefix="URI"`
Note: The namespace URI is not used by the parser to look up information.
The purpose of using an URI is to give the namespace a unique name.
However, companies often use the namespace as a pointer to a web page containing namespace information.

```xml
<root>

<h:table xmlns:h="http://www.w3.org/TR/html4/">
  <h:tr>
    <h:td>Apples</h:td>
    <h:td>Bananas</h:td>
  </h:tr>
</h:table>

<f:table xmlns:f="https://www.w3schools.com/furniture">
  <f:name>African Coffee Table</f:name>
  <f:width>80</f:width>
  <f:length>120</f:length>
</f:table>

</root>
```

# Default Namespaces
Defining a default namespace for an element saves us from using prefixes in all the child elements. It has the following syntax:
```xml
<table xmlns="http://www.w3.org/TR/html4/">
  <tr>
    <td>Apples</td>
    <td>Bananas</td>
  </tr>
</table>
``` 
# XML Schema
The XML Schema language is also referred to as **XML Schema Definition (XSD)**.
DTDs and XML Schemas both document type definitions (DTDs) and XML Schemas serve to describe the definition of
an XML document, its structure, and what data is allowed where. They can then be used to test
whether a document that has been received is consistent with the prescribed format, a process
known as `validation`.
```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

<xs:element name="note">
  <xs:complexType>
    <xs:sequence>
      <xs:element name="to" type="xs:string"/>
      <xs:element name="from" type="xs:string"/>
      <xs:element name="heading" type="xs:string"/>
      <xs:element name="body" type="xs:string"/>
    </xs:sequence>
  </xs:complexType>
</xs:element>

</xs:schema>
```


The <schema> element is the root element of every XML Schema:
 xmlns:xs="http://www.w3.org/2001/XMLSchema"
  indicates that the elements and data types used in the schema come from the "http://www.w3.org/2001/XMLSchema" namespace. It also specifies that the elements and data types that come from the "http://www.w3.org/2001/XMLSchema" namespace should be prefixed with xs:


```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema"
targetNamespace="https://www.w3schools.com"
xmlns="https://www.w3schools.com"
elementFormDefault="qualified">
...
...
```

# Elements and Attributes
An element can contain:

- text
- attributes
- other elements
- or a mix of the above

Simple elements cannot have attributes. If an element has attributes, it is considered to be of a complex type. But the attribute itself is always declared as a simple type.

The syntax for defining an attribute is:
`<xs:attribute name="xxx" type="yyy"/>`
See Ww3schools for **fixed ,default,optinal** and **required** attirbutes 

```xml
<!--Element -->
<price someAttribute="someVaue">29.99</price>
```
# Parser and DOM
The XML DOM (Document Object Model) defines the properties and methods for accessing and editing XML.
All modern browsers have a built-in XML parser that can convert text into an XML DOM object.
Although the DOM was used for many years, it has a reputation for being a bit unwieldy and difficult to use. It also tends to take up a lot of memory (in reallity DOM is a intermidate step of the process of parsin). 
However, if you need to extract just a few pieces of information from XML or HTML the DOM is widely supported,
especially across browsers, and is used a lot by many of the script libraries that are popular nowadays such as jQuery.

#  Path 
XPath uses path expressions to select nodes or node-sets in an XML document. These path expressions look very much like the expressions you see when you work with a traditional computer file system. XPath expressions can be used in JavaScript, Java, XML Schema, PHP, Python, C and C++, and lots of other languages.

XPath Expression | Result
------------ | -------------
//title[@lang='en']	| Selects all the title elements that have a "lang" attribute with a value of "en"
/bookstore/book[price>35.00]	| Selects all the book elements of the bookstore element that have a price element with a value greater than 35.00

# XSl and XSLT
**XSL (eXtensible Stylesheet Language)** is a styling language for XML.
**XSLT stands for XSL Transformations** 
 XSLT Laguange used to transform xml documents into another documents as HTML
seee : [W3Schools - XSLT](https://www.w3schools.com/xml/tryxslt.asp?xmlfile=cdcatalog&xsltfile=cdcatalog)

# XQuery
XQuery is to XML what SQL is to databases.
XQuery was designed to query XML data.


# Types
# Complex type and Simple type
 simple element is an XML element that contains only text. It cannot contain any other elements or attributes.

`<xs:element name="xxx" type="yyy"/>`
see  W3Schools for  fixed and defatul values elements

# Mandatory

# Cardinality

# Restriction
Also refered as **Facets**, restrictions are used to define acceptable values for XML elements or attributes.
The following example defines an element called "age" with a restriction. The value of age cannot be lower than 0 or greater than 120:
```xml
<xs:element name="age">
  <xs:simpleType>
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0"/>
      <xs:maxInclusive value="120"/>
    </xs:restriction>
  </xs:simpleType>
</xs:element>
```


