rhino
=====

Rhino is an open-source implementation of JavaScript written entirely in Java

This Fork
=========

This is a fork from the rhino project to allow goog.base() calls in closure library, that allows us to run tests on 
closure code without without code complaints about goog.base() calls. This is still exprimental, 
but seems to work so far.

HowTo
==========

checkout this fork somewhere and run `ant jar` to get the js.jar file.

if you're using maven, drop the .jar file in your project's lib directory and add this entry into pom.xml:

    <dependency>
      <groupId>org.mozilla</groupId>
      <artifactId>rhino</artifactId>
      <version>1.7R5-20130827-1</version>
      <scope>system</scope>
      <systemPath>${project.basedir}/lib/js.jar</systemPath>
    </dependency>

This build of rhino should support goog.base() now, but it will also have some performance impacts on rhino.
