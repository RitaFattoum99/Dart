## Welcome To Dart Doc
##### Installing dart & Basic 

## System requirements:
###### Windows
- Supported versions: Windows 10.
- Supported architectures: x64, ia32.

###### Linux
- Supported versions: Debian stable and Ubuntu LTS under standard support.
- Supported architectures: x64, ia32, arm, arm64.
## 1. Install on Windows:
 ##### Step 1: Download Dart SDK [click](https://storage.googleapis.com/dart-archive/channels/stable/release/2.14.4/sdk/dartsdk-windows-ia32-release.zip)
 ##### Step 2: Extract zip file
 ##### Step 3: Run Dart Command
 ##### Step 4: Add Dart Path to PATH Environment Variable
 ##### Step 5: Restart Command Prompt


## Conclusion
we learned how to install Dart on Windows, to work with Dart programming.
## 1. Install Dart on Linux:
Install using apt-get
Perform the following one-time setup:

```
$ sudo apt-get update
$ sudo apt-get install apt-transport-https
$ sudo sh -c 'wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
$ sudo sh -c 'wget -qO- https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
```
Then install the Dart SDK:
```
$ sudo apt-get update
$ sudo apt-get install dart
```
Install a Debian package
Alternatively, download Dart SDK [as a Debian package](https://storage.googleapis.com/dart-archive/channels/stable/release/latest/linux_packages/dart_2.14.4-1_amd64.deb) in the .deb package format.

Modify PATH for access to all Dart binaries
After installing the SDK, add its bin directory to your PATH. For example, use the following command to change PATH in your active terminal session:
```
$ export PATH="$PATH:/usr/lib/dart/bin"
```
To change the PATH for future terminal sessions, use a command like this:
```
$ echo 'export PATH="$PATH:/usr/lib/dart/bin"' >> ~/.profile
```

## Conclusion
we learned how to install Dart on Linux, to work with Dart programming.
## 3.The basic concepts of Dart programming language:
Now we will learn a very basic Dart program.


###### Dart – Hello World

This sample program, prints Hello World to the console.
Open a text editor and paste the following code.
```
void main(){
    print('Hello World');
}
```
Save the file as hello.dart (hello is just a file's name)
Open Command Prompt and go to the folder, in which the hello.dart file is saved.
Execute the following command to run hello.dart present in the current working directory.

![execute hello word](C:\Users\ريتا\Desktop\dart-hello-world.png)
The program is run successfully and Hello World string is printed to console.
- Every Dart application has a main function main()
- void represents that the function returns nothing.
- Empty parenthesis after main () represents that currently our main function does not take any arguments.
- The body of main() function is enclosed in curly braces  { } .
- print() is a high level Dart function that prints to console.

## Conclusion
We learned how to write a simple hello world program in Dart programming language and run it using dart command.

Now we will learn variable in dart.

#Dart Variables

Dart is type-safe. So, most variables does not require explicit type declaration.
##### Create a Variable
You can create a variable using `var` keyword.

```
var a;
```
As no value is assigned to the variable, and we did not mention the type explicitly, the type of variable would be Null and the value stored would be null.

##### Assign Value to Variable
You can assign a value to the variable using assignment operator =.
```
var a = 'Hello World';
```
If you assign a value to variable, the type of the variable would be inferred from the value.
##### Explicit Declaration
```
String a = 'Hello World';
```

##### Re-assign Variable with value of Different Datatye
Using dynamic keyword, you can reassign a variable with different datatype from the one that it is actually referencing.

```
void main(){
    dynamic a = 'Hello World';
    a = 10;
}
```

## Conclusion
Now, we learned how to declare and initialize variables, inference and explicit declaration.

# Dart Comments
We will learn three different types of comments supported by Dart programming language.

- Single Line Comments
- Block (Multi-line) Comments
- Documentation Comments

##### Single Line Comments
To write single line comments, use double forward slash //
```
void main(){
    //this is comment
    //this is another comment
}
```
##### Block (Multi-Line) Comments
You can write multiple line comments enclosed between /* and */.
```
void main(){
    /*
    This is a block comment.
    It can contain multiple lines as comment.
    Another line in this block comment.
    */
}
```
##### Documentation Comments
These comments are similar to single line comments. But are specially treated by IDEs and dartdoc libraries. You can use these documentation comments for documenting your classes, methods, etc., in the dart libraries you develop.

Using some documentation preparation tools, you can generate documentation from code automatically.
```
///Documentation Comments
///Some description about main() method.
void main(){

}
```
## Conclusion
We learned different types of commenting techniques and how to use them.


# Dart Conditional Statements
###### Dart – If, If-Else, If-Else-If
We will learn the syntax of Dart If statement, Dart If-Else statement and Dart If-Else-If.

##### Syntax of Dart If Statement
The syntax of if statement in Dart is shown below.
```
if (boolean_expression) {
     //statement(s)
 }
```

##### Dart If-Else
The syntax of if statement in Dart is shown below.
```
if (boolean_expression) {
     //if block statement(s)
 } else {
     //else block statement(s)
 }
```
##### Dart If-Else-If
 The syntax of if statement in Dart is shown below.
```
if (boolean_expression_1) {
     //statement(s)
 } else if (boolean_expression_2) {
     //statement(s)
 } else {
     //else block statement(s)
 }
```
## Conclusion
We learned about Dart Conditional Statements: If, If-Else and If-Else-If ladder.

# Dart For Loop
We will learn the syntax of for loop
##### Syntax of Dart For Loop
Following is the syntax of For Loop in Dart programming language.
```
for (initialization; boolean_expression; update) {
     //statement(s)

 }
```
###### In the following example, we will use Dart For Loop to calculate the factorial of a given number.
```
void main(){ 
    var n = 6;
    var factorial = 1;

    //for loop to calculate factorial
    for(var i=2; i<=n; i++) {
        factorial = factorial*i;
    }

    print('Factorial of ${n} is ${factorial}');
}
```
###### Output

`Factorial of 6 is 720`

```flow
st=>start: start
op=>operation: loop body
cond=>condition: loop condition
e=>end: End of loop

st->op->cond
cond(yes)->e
cond(no)->op
```

## Conclusion

We learned the syntax and how to use for loop with the help of example progra.

# Dart List
A List is simply an ordered group of objects.
#### Step 1 − Declaring a list

The syntax for declaring a fixed length list is given below −
```
var list_name = new List(initial_size)
```
The above syntax creates a list of the specified size. The list cannot grow or shrink at runtime. Any attempt to resize the list will result in an exception.
#### Step 2 − Initializing a list

The syntax for initializing a list is as given below −
```
lst_name[index] = value;
```
###### Example
```
void main() {
   var lst = new List(3);
   lst[0] = 12;
   lst[1] = 13;
   lst[2] = 11;
   print(lst);
}
```
###### Output
`[12, 13, 11]`
### Growable List
A growable list’s length can change at run-time. The syntax for declaring and initializing a growable list is as given below −
#### Step 1 − Declaring a List
- creates a list containing the specified values

```
var list_name = [val1,val2,val3]
```
###### OR
- creates a list of size zero

```
var list_name = new List()
```

#### Step 2 − Initializing a List
The index / subscript is used to reference the element that should be populated with a value. The syntax for initializing a list is as given below −

`list_name[index] = value;`
###### Example

The following example shows how to create a list of 3 elements.

```
void main() {
   var num_list = [1,2,3];
   print(num_list);
}
```
###### Output
`[1, 2, 3]`

###### Example

The following example creates a zero-length list using the empty List() constructor. The `add()` function in the List class is used to dynamically add elements to the list.
```
void main() {
   var lst = new List();
   lst.add(12);
   lst.add(13);
   print(lst);
}
```
###### Output
`[12, 13] `

## Was it helpful?
I hope you have got the desired interest
to see more click [here](https://github.com/RitaFattoum99/Rita).

