JAVA program execution commands with debug options:-

java \
  -XX:+PrintCompilation \
  -XX:CompileOnly=HelloWorld::workload \
  HelloWorld



java \
  --module-path=/home/vishnu/Projects/GRAAL/graal/sdk/mxbuild/modules/org.graalvm.graal_sdk.jar:/home/vishnu/Projects/GRAAL/graal/truffle/mxbuild/modules/com.oracle.truffle.truffle_api.jar \
  --upgrade-module-path=/home/vishnu/Projects/GRAAL/graal/compiler/mxbuild/modules/jdk.internal.vm.compiler.jar \
  -XX:+UnlockExperimentalVMOptions \
  -XX:+EnableJVMCI \
  -XX:+UseJVMCICompiler \
  -XX:-TieredCompilation \
  -XX:+PrintCompilation \
  -XX:CompileOnly=HelloWorld::workload \
  HelloWorld


-Xcomp  -- foce compile all of java
search HotSpotJVMCIRuntime.java

java -XX:+UnlockExperimentalVMOptions   -XX:+EnableJVMCI   -XX:+UseJVMCICompiler   -XX:-TieredCompilation   -XX:+PrintCompilation   -XX:CompileOnly=HelloWorld::workload HelloWorld

-XX+PrintInterpreter  --> for printing template interpreter code
