## Setting up a local java development environment
The setup of a local java development environment is about installing JDK and setting environment variables such as JAVA_HOME and CLASSPATH.

## How to use the console to compile, execute and package (Running Java using command)
After properly installing JDK

* Create .java extension file with source code

* Compile the source code with  

    `javac <myJavaFile.java>`
    
   Or to compile all source/.java files insede a folder called source. And with -d parameter to indicate classes' folder.
  
    `javac source/*.java -d classes/`
* And execute the .class file generated
    
    `java <MyClassFileclass>`

     for packages 
    `java <package_path>.<Main Class>`

* To package the entire project in a jar file 
    

     First manually create txt filme MANIFEST.txt (should be in  the same folder as your package ) and execute de following command:
    
    `jar cfm MyJar.jar Manifest.txt MyPackage/*.class`
    
    To show you manifest file
    `unzip -p some-jar-file.jar META-INF/MANIFEST.MF`



## Java classpath
Classpath is an environment variable that JVM uses in order to locate the java classes.

* Setting the classpath

    `export CLASSPATH="your classpath"`
    
    Adding a path
    
    `export CLASSPATH="$CLASSPATH:$HOME/java/lib/foebar.jar`

* By default CLASSPATH in Java points to current directory denoted by "." and it will look for any class only in the current directory.
If two classes with the same name exist in Java Classpath then the class which comes earlier in Classpath will be picked by Java Virtual Machine.
When you use the -jar command line  option to run your program as an executable JAR, then the Java CLASSPATH environment variable will be ignored, and also the -cp and -classpath switches will be ignored and, In this case, you can set your java classpath in the META-INF/MANIFEST.MF file by using the Class-Path attribute.
In Unix of Linux, Java Classpath contains names of the directory with colon “:” separated, 
To check the environment variable within you application:
    
    `System.getProperty("java.class.path");` 





## How to configure the MANIFEST.MF file
Every jar package has a MANIFEST.MF FILE. This is a meta file about the jar. Useful for things like package sealing.

* The last line must be new line character.

* You should leave a space between a property and value

    `Manifest-Version: 1.0`

* To modify the manifest, you must first prepare a text file containing the information you wish to add to the manifest.
* You then use the Jar tool's `m` option to add the information in your file to the manifest:

    `jar cfm jar cf <jar-name> [ files to be packaged]`
