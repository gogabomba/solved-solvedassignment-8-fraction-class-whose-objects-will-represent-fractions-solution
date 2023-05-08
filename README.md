Download Link: https://assignmentchef.com/product/solved-solvedassignment-8-fraction-class-whose-objects-will-represent-fractions-solution
<br>
Write a fraction class whose objects will represent fractions. You should provide the following member functions:

Two constructors, a default constructor which assigns the value 0 to the fraction, and a constructor that takes two parameters. The first parameter will represent the initial numerator of the fraction, and the second parameter will represent the initial denominator of the fraction.Arithmetic operations that add, subtract, multiply, and divide fractions. These should be implemented as value returning functions that return a fraction object. They should be named addedTo, subtract, multipliedBy, and dividedBy.A boolean operation named isEqualTo that compares two fraction objects for equality.An output operation named print that displays the value of a fraction object on the screen in the form numerator/denominator.Your class should have exactly two data members, one to represent the numerator of the fraction being represented, and one to represent the denominator of the fraction being represented.

When adding or subtracting fractions, remember that you must first find the common denominator. The easy way to do this is to multiply the denominators together and use that product as the common denominator.

I am providing a client program for you below. You should copy and paste this into a file and use it as your client program. The output that should be produced when the provided client program is run with your class is also given below, so that you can check your results. Since you are not writing the client program, you are not required to include comments in it.

I strongly suggest that you design your class incrementally. For example, you should first implement only the constructors and the output function, and then test what you have so far. Once this code has been thoroughly debugged, you should add additional member functions, testing each one thoroughly as it is added. You might do this by creating your own client program to test the code at each stage; however, it would probably be better to use the provided client program and comment out code that relates to member functions that you have not yet implemented.

As you can see from the sample output given below, you are not required to change improper fractions into mixed numbers for printing. Just print it as an improper fraction. You are, however, required to reduce fractions, as illustrated in the sample output. Make sure that your class will reduce ANY fraction, not just the fractions that are tested in the provided client program. Fractions should not be simply reduced upon output, they should be stored in reduced form at all times. In other words, you should ensure that all fraction objects are reduced before the end of any member function. You are also not required to deal with negative numbers, either in the numerator or the denominator.

You must create your own algorithm for reducing fractions. Don’t look up an already existing algorithm for reducing fractions or finding GCF. The point here is to have you practice solving the problem on your own. In particular, don’t use Euclid’s algorithm. Don’t worry too much about efficiency, just create something of your own that works correctly on ANY fraction.

Before you submit your assignment, make sure to carefully read section 1D of the Style Conventions, “Commenting in Classes”.

Here is the client program.

#include &lt;iostream

#include “fraction.h”

using namespace std;

int main()

{

fraction f1(9,8);

fraction f2(2,3);

fraction result;

cout &lt;&lt; “The result starts off at “;

result.print();

cout &lt;&lt; endl;

cout &lt;&lt; “The product of “;

f1.print();

cout &lt;&lt; ” and “;

f2.print();

cout &lt;&lt; ” is “;

result = f1.multipliedBy(f2);

result.print();

cout &lt;&lt; endl;

cout &lt;&lt; “The quotient of “;

f1.print();

cout &lt;&lt; ” and “;

f2.print();

cout &lt;&lt; ” is “;

result = f1.dividedBy(f2);

result.print();

cout &lt;&lt; endl;

cout &lt;&lt; “The sum of “;

f1.print();

cout &lt;&lt; ” and “;

f2.print();

cout &lt;&lt; ” is “;

result = f1.addedTo(f2);

result.print();

cout &lt;&lt; endl;

cout &lt;&lt; “The difference of “;

f1.print();

cout &lt;&lt; ” and “;

f2.print();

cout &lt;&lt; ” is “;

result = f1.subtract(f2);

result.print();

cout &lt;&lt; endl;

if (f1.isEqualTo(f2)){

cout &lt;&lt; “The two fractions are equal.” &lt;&lt; endl;

} else {

cout &lt;&lt; “The two fractions are not equal.” &lt;&lt; endl;

}

const fraction f3(12, 8);

const fraction f4(202, 303);

result = f3.multipliedBy(f4);

cout &lt;&lt; “The product of “;

f3.print();

cout &lt;&lt; ” and “;

f4.print();

cout &lt;&lt; ” is “;

result.print();

cout &lt;&lt; endl;

}

This client should produce the output shown here:

The result starts off at 0/1

The product of 9/8 and 2/3 is 3/4

The quotient of 9/8 and 2/3 is 27/16

The sum of 9/8 and 2/3 is 43/24

The difference of 9/8 and 2/3 is 11/24

The two fractions are not equal.

The product of 3/2 and 2/3 is 1/1

You may not change the client program in any way, except that you can add the system(“pause”) statement if you are using Dev-C++. Changing the client program will result in a grade of 0 on the project.