# Motivavion
XML was conceived as a solution to this kind of problem (intercommunication); it is meant to make passing data between
different components much easier and relieve the need to continually worry about different formats
of input and output, freeing up developers to concentrate on the more important aspects of coding
such as the business logic. XML is also seen as a solution to the question of whether files should be
easily readable by software or by humans; XML’s aim is to be both

Browsers use an XML stylesheet or transformation to display XML files. An XML stylesheet is a textbased file with an XML format that can transform one format into another. They are most commonly
used to convert from a particular XML format to another or from XML to HTML, but they can also
be used to process plain text


One of the aims of XML is to implement a clear separation between data and presentation.
This means that the same underlying data can be used in multiple presentation scenarios. It also
means that when moving data, across a network for example, bandwidth is not wasted by having
to carry redundant information concerned only with the look and feel. This separation is simple
with XML as there are no built-in presentational features such as exist in HTML, and is one of
its main advantages


The Document Object Model
Once an XML parser has done its work, it produces an in-memory representation of the XML.
This model exposes properties and methods that let you extract information from and also modify
the XML

Although the DOM was used
for many years, it has a reputation for being a bit unwieldy and difficult to use. It also tends to take
up a lot of memory. 

However, if you need
to extract just a few pieces of information from XML or HTML the DOM is widely supported,
especially across browsers, and is used a lot by many of the script libraries that are popular nowadays such as jQuery.

# XML origin

# XML structure

`<?xml version="1.0" encoding="UTF-8"?>`

// more tags

# Namespaces
Basically, namespaces serve as a way of grouping XML.
XML Namespaces provide a method to avoid element name conflicts.The namespace can be defined by an `xmlns` attribute in the start tag of an element.The namespace declaration has the following syntax:`xmlns:prefix="URI"`



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

# Elements and Attributes

An element can contain:

- text
- attributes
- other elements
- or a mix of the above

```xml
<!--Element -->
<price someAttribute="someVaue">29.99</price>
```

# Types
# Complex type and Simple type
# Mandatory
# Cardinality
# Restriction
