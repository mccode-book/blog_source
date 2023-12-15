---
layout: post
title:  "Java 21, Hello World"
date:   2023-12-13 17:48:53 +0800
categories: jekyll update
---
# Exercise J001-001-hello

## Introduction

"Hello World" is often the first program that aspiring programmers learns to write a program. This should be regarded as your first program in Java pogramming language.

What you need to do:

To complete the exercise, students usually need to:

Write the program code: This involves using the appropriate syntax to print the "Hello, World!" message. The code can vary depending on the programming language being used, so students should refer to their learning materials or online resources for guidance.

Run the program: Once the code is written, students need to run the program to see the output. This can be done by executing the program through a compiler or interpreter specific to the programming language.

Verify the output: Students should ensure that the program outputs the expected result, which in this case is the phrase "Hello, World!". If the output is correct, they have successfully completed the exercise.

Completing the "Hello World" exercise helps students gain confidence in their programming skills and serves as a starting point for more complex coding challenges. It also allows them to practice the fundamental concepts of programming, such as syntax, variables, and output.

## Prerequisite

To successfully complete this exercise, it is important to have a good understanding of both shell scripting and Markdown language. Therefore, it is recommended that students have prior knowledge of these concepts before attempting this particular exercise.

## The source code

### The standard format

The source code is stored inside "Hello.java" file. "java" is the common file extension for java programming language. You can see the content of the file by typing:

{% highlight shell %}
cat Hello.java
{% endhighlight %}

The result should look like:

{% highlight java %}
class Hello {
    public static void main(String[] args) {
        java.lang.System.out.println("Hello, World!"); 
    }
}
{% endhighlight %}

### The simplified format
Since java version 21, the new feature, simplified format has bee provided to allow programers to write a shorter program.  We still use the ".java" as the extension. You can see the content of the simplified file by typing:

{% highlight shell %}
cat Hello21.java
{% endhighlight %}

The result should look like:

{% highlight java %}
void main() {
    System.out.println("Hello, Java 21!");
}
{% endhighlight %}

## Remove previous compiled file
It is necessary to check and remove any previous compiled file before any new compilation.  The command for checking and removing the compiled file should be:

{% highlight shell %}
rm *.class
{% endhighlight %}

There should not display any error or warning after execution.

## Compilation
Compilation is important in java programming language. You can compile the standard version by:

{% highlight shell %}
javac Hello.java
{% endhighlight %}

You can compile the simplified version by 

{% highlight shell %}
javac --release 21 --enable-preview Hello21.java
{% endhighlight %}

The screen should not display any error or warning after execution. For the simplified version, there will be extra notes show in the screen:

{% highlight shell %}
Note: Hello21.java uses preview features of Java SE 21.
Note: Recompile with -Xlint:preview for details.
{% endhighlight %}

### class file
After compilation, you will notice files with ".class" extension will be generated. These are java class file which is / are required in execution. In order to see if the file is there, you can use the following command: 
{% highlight shell %}
ls *.class
{% endhighlight %}

The execution may be similar to:
{% highlight shell %}
Hello.class
Hello21.class
{% endhighlight %}

## Execution of the compiled file
The compiled standard java class file, "Hello.class" can be execute by:

{% highlight shell %}
java Hello
{% endhighlight %}

The compiled simplified java version 21 class file, "Hello21.class" can be execute by:

{% highlight shell %}
java --enable-preview Hello21
{% endhighlight %}

The expected result should be:

{% highlight shell %}
Hello World!
{% endhighlight %}

