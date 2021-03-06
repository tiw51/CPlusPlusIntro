# CPlusPlusIntro
Just a short intro to C++
## Basics
Syntax is more or less the same as C except, if you want to use standard library objects, like 
the traditional input (`cin`) or output (`cout`). To relay to these objects you use the shift (>>
or <<) operator. These denote bitwise shifts. In the case of `cin` and `cout`, they denote transfer of data. 
If you would like to perform the hello world program (without the surrounding function headers), you write
```cpp
std::cout<<"Hello World!"<<endl;
```
The traditional variable types should all be the same, (int, double, long, etc.) For strings, 
import the `#include <string>`. 

`if` statements are the same as C, for instance

```cpp
if ()
statement ;
else 
statement;
```
or, for multiline statements: 
```cpp
if (){
statement;
statement;
}
else {
statement;
statement;
}
```
The keyword `const` also comes up a lot. This keyword just makes makes the compiler raise an error if the value 
of the `const` variable is changed. `constexpr` is a more focused version of `const`, in which the variable must 
not change and also be interprettable during compilation of the program (no variablility like user input).

Operator Expressions

<table>
<tbody><tr class="alt">
<th>Prec/Ass</th>
<th>Operator</th>
<th>Description</th>
<th>Pattern</th>
</tr>
<tr class="">
<td>1 None</td>
<td>
::<br>
::
</td>
<td>
Global scope (unary)<br>
Class scope (binary)
</td>
<td>
::name<br>
class_name::member_name<br>
</td>
</tr>
<tr class="alt">
<td>2 L-&gt;R</td>
<td>
()<br>
()<br>
()<br>
{}<br>
type()<br>
type{}<br>
[]<br>
.<br>
-&gt;<br>
++<br>
––<br>
typeid<br>
const_cast<br>
dynamic_cast<br>
reinterpret_cast<br>
static_cast
</td>
<td>
Parentheses<br>
Function call<br>
Initialization<br>
Uniform initialization (C++11)<br>
Functional cast<br>
Functional cast (C++11)<br>
Array subscript<br>
Member access from object<br>
Member access from object ptr<br>
Post-increment<br>
Post-decrement<br>
Run-time type information<br>
Cast away const<br>
Run-time type-checked cast<br>
Cast one type to another<br>
Compile-time type-checked cast
</td>
<td>
(expression)<br>
function_name(parameters)<br>
type name(expression)<br>
type name{expression}<br>
new_type(expression)<br>
new_type{expression}<br>
pointer[expression]<br>
object.member_name<br>
object_pointer-&gt;member_name<br>
lvalue++<br>
lvalue––<br>
typeid(type) or typeid(expression)<br>
const_cast&lt;type&gt;(expression)<br>
dynamic_cast&lt;type&gt;(expression)<br>
reinterpret_cast&lt;type&gt;(expression)<br>
static_cast&lt;type&gt;(expression)
</td>
</tr>
<tr class="">
<td>3 R-&gt;L</td>
<td>
+<br>
-<br>
++<br>
––<br>
!<br>
~<br>
(type)<br>
sizeof<br>
&amp;<br>
*<br>
new<br>
new[]<br>
delete<br>
delete[]
</td>
<td>
Unary plus<br>
Unary minus<br>
Pre-increment<br>
Pre-decrement<br>
Logical NOT<br>
Bitwise NOT<br>
C-style cast<br>
Size in bytes<br>
Address of<br>
Dereference<br>
Dynamic memory allocation<br>
Dynamic array allocation <br>
Dynamic memory deletion<br>
Dynamic array deletion
</td>
<td>
+expression<br>
-expression<br>
++lvalue<br>
––lvalue<br>
!expression<br>
~expression<br>
(new_type)expression<br>
sizeof(type) or sizeof(expression)<br>
&amp;lvalue<br>
*expression<br>
new type<br>
new type[expression]<br>
delete pointer<br>
delete[] pointer
</td>
</tr>
<tr class="alt">
<td>4 L-&gt;R</td>
<td>
-&gt;*<br>
.*
</td>
<td>
Member pointer selector<br>
Member object selector
</td>
<td>
object_pointer-&gt;*pointer_to_member<br>
object.*pointer_to_member
</td>
</tr>
<tr>
<td>5 L-&gt;R</td>
<td>
*<br>
/<br>
%
</td>
<td>
Multiplication<br>
Division<br>
Modulus
</td>
<td>
expression * expression<br>
expression / expression<br>
expression % expression
</td>
</tr>
<tr class="alt">
<td>6 L-&gt;R</td>
<td>
+<br>
-
</td>
<td>
Addition<br>
Subtraction
</td>
<td>
expression + expression<br>
expression - expression
</td>
</tr>
<tr>
<td>7 L-&gt;R</td>
<td>
&lt;&lt;<br>
&gt;&gt;
</td>
<td>
Bitwise shift left<br>
Bitwise shift right
</td>
<td>
expression &lt;&lt; expression<br>
expression &gt;&gt; expression
</td>
</tr>
<tr class="alt">
<td>8 L-&gt;R</td>
<td>
&lt;<br>
&lt;=<br>
&gt;<br>
&gt;=
</td>
<td>
Comparison less than<br>
Comparison less than or equals<br>
Comparison greater than<br>
Comparison greater than or equals
</td>
<td>
expression &lt; expression<br>
expression &lt;= expression<br>
expression &gt; expression<br>
expression &gt;= expression
</td>
</tr>
<tr>
<td>9 L-&gt;R</td>
<td>
==<br>
!=
</td>
<td>
Equality<br>
Inequality
</td>
<td>
expression == expression<br>
expression != expression
</td>
</tr>
<tr class="alt">
<td>10 L-&gt;R</td>
<td>
&amp;
</td>
<td>
Bitwise AND
</td>
<td>
expression &amp; expression
</td>
</tr>
<tr>
<td>11 L-&gt;R</td>
<td>
^
</td>
<td>
Bitwise XOR
</td>
<td>
expression ^ expression
</td>
</tr>
<tr class="alt">
<td>12 L-&gt;R</td>
<td>
|
</td>
<td>
Bitwise OR
</td>
<td>
expression | expression
</td>
</tr>
<tr>
<td>13 L-&gt;R</td>
<td>
&amp;&amp;
</td>
<td>
Logical AND
</td>
<td>
expression &amp;&amp; expression
</td>
</tr>
<tr class="alt">
<td>14 L-&gt;R</td>
<td>
||
</td>
<td>
Logical OR
</td>
<td>
expression || expression
</td>
</tr>
<tr>
<td>15 R-&gt;L</td>
<td>
?:<br>
=<br>
*=<br>
/=<br>
%=<br>
+=<br>
-=<br>
&lt;&lt;=<br>
&gt;&gt;=<br>
&amp;=<br>
|=<br>
^=
</td>
<td>
Conditional (see note below)<br>
Assignment<br>
Multiplication assignment<br>
Division assignment<br>
Modulus assignment<br>
Addition assignment<br>
Subtraction assignment<br>
Bitwise shift left assignment<br>
Bitwise shift right assignment<br>
Bitwise AND assignment<br>
Bitwise OR assignment<br>
Bitwise XOR assignment
</td>
<td>
expression ? expression : expression<br>
lvalue = expression<br>
lvalue *= expression<br>
lvalue /= expression<br>
lvalue %= expression<br>
lvalue += expression<br>
lvalue -= expression<br>
lvalue &lt;&lt;= expression<br>
lvalue &gt;&gt;= expression<br>
lvalue &amp;= expression<br>
lvalue |= expression<br>
lvalue ^= expression
</td>
</tr>
<tr class="alt">
<td>16 R-&gt;L</td>
<td>
throw
</td>
<td>
Throw expression
</td>
<td>
throw expression
</td>
</tr>
<tr>
<td>17 L-&gt;R</td>
<td>
,
</td>
<td>
Comma operator
</td>
<td>
expression, expression
</td>
</tr>
</tbody>
</table>


## Files and Pointers
Pointers are defined using the * operator on assignment and dereferenced with the same * operator. 
The & reference operator gets the address of an object. This is often used to define a pointer. 

The traditional pointer is very easy to use, in that it can be created using the basic definition using the
`*` operator. 

More advanced pointers include the `unique_ptr`, `shared_ptr` and `weak_ptr`.

The unique pointer is suppored depending on the compiler, and can be most often defined as:
 ```cpp
 std::unique_ptr<type> name(new type());
 //to delete:
 name.reset();
  ```
  The unique pointer cannot actually be passed directly to a function because its address is unique and connot
  be copied. In order to be used, the unique pointer actually needs to be passed by reference. 

In order to make copies of pointers, use shared_ptr, 

## Functions and Function Pointers
Some high level uses of functions involve passing addresses of objects in order to not 
create a large copy on the runtime stack. This is done with the & operator. as in: 
```cpp
void getPrintMe(const string & aString){
    printf("%s", aString.c_string());
  }
```
Static variables are used when you want to have a value of something defined in a function remain
on memory. For instance, if you would like to return the reference to a string, the 
value of the string cannot be passed as a reference if it is originally defined in memory. 
In order to accomplish this, you need to pass the `static` keyword.

Function pointers are reassigning the function name to another reference. For instance, if you 
had a function named `func()` then you can create the function pointer with the assignment:
```cpp
void (*functionPointer)() =func;
// this is identical to 
void (*functionPointer)() =&func;
```
After this `functionPointer` can be used in the same way that `func` can be used 
sometimes a dereference is done as well in order to show that the pointer is
there and be more explicit. Be 
sure to match the return type ( in this case `void`). The main time this is useful is
when defining an array of function pointers. So long as the return 
type is constant, this array can be defined This can be done by the below declaration:
```cpp
    void (*funcs[])()={fa, fb, fc, fd, fe, nullptr};
    //this defines functions fa... fe as pointers. 
```
Also, it is possible to redefine an operator (like `+`) by using the `operator` keyword. 
This is most applicable using classes. 
## Classes
Classes can be defined two different ways in C++. The first is a very readable way that is included directly in the
file itself and the second is through defining it in a header file, the same can be completed inside the
file. To do this, just include the function header and have the function defintions later. 

Some simple things to note: class variables default to private while struct variables default to 
public, a pointer to an object is dereferenced using the `->` operator, make sure to mark a function
as `const` safe by adding the `const` keyword at the end of the function definition. 

Below is an example of a class and its implementation in C++
```cpp
// class.cpp by Bill Weinman <http://bw.org/>
#include <cstdio>
using namespace std;

// a very simple class
class Class1 {

    int i=0 ;
public:
    
    void setvalue( const int value );
    int getvalue() const;
};
void Class1::setvalue(const int value ){ i = value; }
int Class1::getvalue() const
{ return i; }
int main( int argc, char ** argv ) {
    int i = 47;
    Class1 object1;
    
    object1.setvalue(i);
    printf("value is %d\n", object1.getvalue());
    return 0;
}

```
Defining namespaces is as simple as defining the namespace around the things you would like included in
the namespace. See some code below:
```cpp
    namespace anExampleNamespace{
    // some class definitions 
    class blahBlah{
    //some more class stuff
    }
    }
```
## Common C++ Bugs
* Always check bounds of array before hard indexing! ( make it in a try catch block ) For example: 
    
    ```cpp
    std::vector<int> a= {5,6};
    a[3];
    ```
    
    To fix this, you can just pass `-fsanitize=address` to your favorite compiler. 
 * Maps can have really bad issues if you do not write the correct key (misspell "hey" with "hye"). If this happens, the map will return 0. Imagine you are looking for the timeout of a network.... network["timeout"]. This will cause infinite timeouts. 
* Passing by reference can break if you send a nonstatic string reference. For instance, if you declare a string inside a function, and return it by reference, you will break everything because it will pass a reference to a object that has been destroyed. To fix this, pass `-fsanitize-address-use-after-scope`
* Just don't use `volitile`. This can make the code not thread safe. Use `std::atomic` instead. 
## Advanced Standard Library

## Data Structure Implementations
