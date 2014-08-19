# ErrorHandling

## Overview

Handles logging and display of script errors. It really doesn't do much more than that, but it is intended to empower the developer to adopt some conventions that make error handling more robust and habitual with less effort.


## Dependencies

* Error table
* "Error" custom functions
* Scripts in ErrorHandling script folder
* Errors Table layout (optional)
* ParamConverter module (optional)


## Usage

It's really up to you. The primary scripts are ".  error . log" and ".  error . display". See the template scripts in this module for basic usage. See the examples for more detailed implementation recommendations.


## Philosophical Assumptions

* Error handling should require very little overhead on the developer's part. It should be habitual.
* Error handling should not distract from the overall goals of the code.
* Errors should be logged as close to the event as possible. This allows us to gather better diagnostic information and prevents other errors from interfering.
* Errors should be reported as close to the initiating action as possible. This allows errors from a generic subscript to bubble up to the button script, for example, where it can be customized for the context.
* Any particulars about an error (how to abort, message to the user, workflow decisions, etc) should be handled where the affected logic resides. In other words, it should be transparent and customizable for the developer - not burried in a subscript somewhere.


## Download and Installation

There should be a "Download ZIP" button on the [GitHub page](https://github.com/DonovanChan/ErrorHandling). See installation instructions in the README script.


## OPTIONAL MODIFICATIONS

- To customize error dialogs: Provide a custom error_message parameter to the ".  error . display" script or edit that script.
- To customize error notifications when dialogs aren't available: Edit the ".  error . notify" script.
- To customize how errors are logged: Edit the ".  error . log" script.
- To customize default values supplied to the NOTES field, edit the SystemProperties() custom function.
- Feel free to rename the ERROR table, but do it before or after completing the migration process.
- To report errors to the user even when Set Error Capture is on, modify ErrorsAreSuppressed( )


## To Do

- Allow script to override notification recipient
- Register module with solution (pending convention)


## Contact

Donovan Chandler  
donovan_c@beezwax.net
