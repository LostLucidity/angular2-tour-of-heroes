Continuaton of Angular2 Quickstart Tutorial, 
https://angular.io/docs/ts/latest/tutorial/

Two public properties were added to the AppComponent class to display a hero's
attributes. The @Component template decorator is then modified to with data
bindings to these new properties with double curly brackets. This is the 
"interpolation" form of one-way data binding.

A hero object was created in interface form. This is a lighter weight form of a
class that only does type checking. The hero property of the AppComponent is
then expanded to be a hero type and initialized. The template decorator is then
updated to interpolate an value within the hero type(e.g., hero.name, hero.id).

The decorator template can use template strings to form multi-line strings with
back ticks to make the template more readable.

An input form allows us to make changes to a hero's value. However, the change
is not reflected in the <h2> tag because of the one-way binding setup. Two-way
binding allows us to see the changes reflected. The ngModel built-in directive
enables this.

********************************************************************************
