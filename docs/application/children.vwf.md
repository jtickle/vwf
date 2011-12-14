children.vwf.yaml
=====================

Children are instances of other components to be attached to this component.

	---
	children:

Some simply reference a separate component.
  
	component:


Most reference a component and configure it.

	  configured:
	    extends:
	      http://vwf.example.com/path/to/component.vwf
	    properties:
	      something: value

Some provide a detailed configuration. The format for a child specification is the same as for a component. It may be converted to a component by cutting out the value (from `extends` though `scripts`), placing it in an addressable file, and replacing it with the URI of the new file.

	  literal:
		extends: 
		  http://vwf.example.com/path/to/prototype.vwf
		implements:
		- http://vwf.example.com/path/to/behavior.vwf
		- http://vwf.example.com/a/different/behavior.vwf
		source:
		  asset.dat
		type:
		  mime/type
		properties:
		  name:
			initializer
		  another:
			initializer
		methods:
		  name:
			initializer
		  another:
			initializer
		events:
		  name:
			initializer
		  another:
			initializer
		children:
		- name:
			component
		- another:
			component
		scripts:
		- specifier
		- specifier
		