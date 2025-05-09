XHamlet: XML Speech Extractor for Hamlet

A Java-based XML parser that extracts speeches by a specified character from Shakespeare’s *Hamlet* and writes them to a new XML file.

Description

XHamlet is a simple DOM-based XML parsing tool built in Java. It processes an XML-encoded version of *Hamlet* and allows users to isolate and extract speeches made by any given character. The filtered speeches are saved into a well-structured XML file for further analysis or reuse.

Technologies Used

- **Java SE**
- **DOM Parser (`javax.xml.parsers` and `org.w3c.dom`)**
- **XML Transformation (`javax.xml.transform`)**

Features:
- Reads and parses large XML documents using DOM
- Filters `<SPEECH>` elements based on the speaker
- Collects all corresponding `<LINE>` elements
- Outputs to a new, readable XML structure

How It Works

1. Load and parse `hamlet.xml` using `DocumentBuilderFactory`.
2. Traverse the DOM tree to find `<SPEECH>` nodes.
3. Match the `<SPEAKER>` element to the user-specified character.
4. Collect all `<LINE>` elements within that speech.
5. Generate a new DOM document with the results.
6. Write the new XML document to an output file using `Transformer`.

How to Run

1. Ensure you have JDK 8+ installed.
2. Compile the Java files:
   ```bash
   javac Task1.java
