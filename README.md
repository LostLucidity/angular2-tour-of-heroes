Continuaton of Angular2 Quickstart Tutorial, 
https://angular.io/docs/ts/latest/tutorial/

Chapter One
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

Chapter Two
npm start in command line starts the TypeScript compiler which watches for 
changes and starts the server.

An array of 10 heroes was created with their id and names in the app.component.
This array can be accessed by created a public property that equals the array.
Typescript can infer the type.

In the @Component template an unordered list was created to display the heroes.
To iterate through the array, the built in directive *ngFor is used within the
<li> tag. The * critical part of the syntax since it indicates that the <li> 
element constitutes a master template. The # prefix identifies the hero as a
local template variable where it can be reference within the template to access
the heroe's properties.

Each item in the list can now be displayed with string interpolation {{hero.id}}
and {{heroe.name}}.

Styling is implemented as a decorator property 'styles' for @Component. The CSS
styling is then posted in a multi-string manner using the backticks.

Setting up the connection between the heroes list and the user selection of a
hero to display its details is a UI pattern called 'master-detail'. Master
referring to the heroes list and detail for the selected hero. The component 
property selectedHero will connect the two through a click event. The event
binding (click)="onSelect(hero)" describes the click event as a target with its
paranthesis while the onSelect calls the AppComponent method. hero is passed as
an argument which is the same local template variable defined by ngFor.

The onSelect method does not exist neither does the variable to describe the
the user selected hero. For the latter the static public hero will be replaced
with 'selectedHero: Hero:'. This is followed by the method 'onSelect(hero: Hero) 
{ this.selectedHero: hero; }'. Within the template, replace the the hero 
variable with selectedHero.

A TypeError arises from the selectedHero implementation since an uninitialized
selectedHero is undefined. The hero content details can be wrapped in a <div>
and the built-in directive *ngIf keeps it out of the DOM as long as selectedHero
is undefined.

Finally for styling the selection, the [class.selected]="hero===selectedHero" 
line results in the selection change happening when the value is true. The
brackets is syntax for property binding one way from the data source
"hero===selectedHero" to a property of class.

********************************************************************************
