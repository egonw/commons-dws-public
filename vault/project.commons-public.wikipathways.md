---
id: 2et0vj32w2vlqhsq0yhv5qa
title: Wikipathways
desc: ''
updated: 1646569661686
created: 1646563156580
---

Most likely THE place to start learning about Wikipathways https://new.wikipathways.org/academy/

Ran into the following issues

➜  pathvisio-3.3.0 sh pathvisio.sh
Problem creating boot delegation class loader: java.lang.reflect.InaccessibleObjectException: Unable to make protected java.security.SecureClassLoader(java.lang.ClassLoader) accessible: module java.base does not "opens java.security" to unnamed module @49b70bc7
Installing bundles that are embedded in the jar.
Detected embedded bundle: org.apache.batik.svggen_1.7.0.v201011041433.jar
Loading jar:file:/Applications/pathvisio-3.3.0/pathvisio.jar!/org.apache.batik.svggen_1.7.0.v201011041433.jar
^C^C%
➜  pathvisio-3.3.0 java --version
openjdk 17.0.1 2021-10-19
OpenJDK Runtime Environment (build 17.0.1+12-39)
OpenJDK 64-Bit Server VM (build 17.0.1+12-39, mixed mode, sharing)


Pathvisio aparently only supports java 8 https://github.com/PathVisio/pathvisio/issues/155


https://medium.com/@brunofrascino/working-with-multiple-java-versions-in-macos-9a9c4f15615a

Adapted line for java8 to

https://stackoverflow.com/a/28635465


Needed to echo eval "$(jenv init -)" >> /Users/pma/.zshrc

Documented here https://github.com/PathVisio/pathvisio/issues/155#issuecomment-1059946761

Stopped here https://new.wikipathways.org/academy/stages/wp-publish/index.html
Now waiting for an auth from Wikipathways to upload

