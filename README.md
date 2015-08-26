# KV-Constructor
Source files can be found [here](http://www.smalltalkhub.com/#!/~Charlyzzz/KV-Constructor), thanks to smalltalkHub.

Wanna use it? Simply open a workspace in any Pharo distribution and un the following code in a workspace:

    Gofer it
    smalltalkhubUser: 'Charlyzzz' project: 'KV-Constructor';
    configurationOf: 'KVC';
    loadVersion: #stable.

KV-Constructor brings to the table a simple and easy way to teach custom constructors without having the knowledge of static messages!. Just plug&play. Inheritance supported. Zero configuration. Unlimited instanciation fun guaranteed!

Just add TKeyValueConstructor to your class as a Trait and you are ready to go! KV-Constructor expose a single class method for you to use: **newKV:**. 

Feed that method a literal array with this pattern: **{ #var1 -> 10. #var2 -> true}**
But be careful, making a typo in the variable name will produce that value not to be set.

-----

<h1> Integration <h1>

    Object subclass: #MyClass
    uses: TKeyValueConstructor
    instanceVariableNames: 'foo1 foo2'
    classVariableNames: ''
    category: 'KVC'

<h1> Use <h1>

    myInstance := MyClass newKV: {#foo1 -> 'Hello there'. #foo2 -> 'Im just a constructor!'}
