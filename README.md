# MiniJava_Compiler
An implementation of a MiniJava compiler using Ant to build the layout of the project </br>
This was built using JavaSE8 </br>
The link below is the reference for the MiniJava grammar that was used for this compiler </br>
http://www.cambridge.org/resources/052182060X/MCIIJ2e/grammar.htm

### Running
* Open the parent directory in the terminal and type ant to build the "build.xml" file
* The entirety of the project is built out of smaller pieces that are implemented as whole, so there are multiple command line arguments to run the different portions which will supply various outputs to display the current process
  * java MiniJava -h(/-H) is the help menu that displays the commands
  * java MiniJava -S filename.java will run only the Scanner
  * java MiniJava -P filename.java will run only the Parser, and any parent process
  * java MiniJava -T filename.java will run only the SymbolTable, and any parent process
  * java MiniJava -A filename.java will run only the SemanticAnalysis, and any parent process
  * java MiniJava -C filename.java will run the entire compiler
  * If the above does not run then the class path needs to be included in the command line depending on system it will vary
    * java -cp "build/classes;lib/java-cup-11b.jar" MiniJava -S filename.java
    * java -cp "build/classes:lib/java-cup-11b.jar" MiniJava -S filename.java
    
