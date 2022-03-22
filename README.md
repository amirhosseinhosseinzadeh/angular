			Angular crash course
-------------------------------------------
Some features =>
	☼ Support TypeScript
	☼ It is completely base on components
	☼ It consist several components which forms a tree structure


Architecture diagram

|-----------------|------------------|
|Module component |  Module service	 |
|		{}		  |		 {}			 |
|-----------------|------------------|
| Module Value    |  Module Fn       |
|       {}        |     {}           |
|-----------------|------------------|

Angular apps are modular and every angular app have its own modurality system called angular module or enshi modules
Every angular app have atleast one angular module class (the root module) convinently named app module  while the root module mybe the 
only module in a small application.

Angular templates are dynamic .when angular renders them it transform the DOM accoarding to the instructions given by directives
Metadata tells angular how to process a class 

			|--------------------|
			|                    |
	 ------>|      Template      |<---------
	|		|       <   >        |          |
	|		|                    |          |
	|		|--------------------|          |
    |Property 					    Event 	|
	|binding|--------------------| binding  |
	|		|		Metadata     |          |			
	|		|--------------------|          |
	|		    							|
	|		|--------------------|          |
	|		|                    |          |
	|		|      Components    |          |
	 ------>|        {     }     |<---------         
			|                    |
			|--------------------|

Service is a board category encompassing any value ,fucntion or feature that the application needs.
Example =>
	☼ login service
	☼ data service
	☼ message bus service .etc

There is nothing specifically about angular services. the angular has no defination of a service 
there is no service base class no place to register a service. 
Yet services are fundamental of any angular application and components are big consumers of services


	Components
Each component consists of =>
	☼ HTML template that declares what renders on the page 
	☼ TYPE_SCIPT class that defines behaviour 
	☼ The CSS selector that defines how the component is used in our template
	☼  Optionally CSS style applied to the component

A component must belong to an NGMODULE In order for it to be available to another component 

Why use componentns 
	☼ reusable 
	☼ component base architecture (easy for error handling)
	☼ breaking down complexity to small pieces

Prequirities =>
	☼ Install angular cli 
	☼ Create an angular workspace 

install command => 
{
	$ npm install -g @angular/cli
}

creating an angular project =>
{
	$ ng new "project_name"
}

alos angular cli is the easiest way to create a component but were gonna to create outr component manually 
to create a componetn well create a .ts file with bellow standard
	"[name:any_string].conponent.ts"

inside of this path
	src/app/.

for the rest read the code :)

import component structure like this
	import { componetn } from "@angular/core";

after the component import statement add decorator
decorator marks a class is an angular component which provide metadata thath decides how component is used at runtime 

@component({
	selector : 'some_string', ==> this will make the component selector name which will be use as a tag in app.component.html like => <some_string></some_string>
	template/templateUrls
})

