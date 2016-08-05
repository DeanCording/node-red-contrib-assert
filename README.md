# node-red-contrib-assert
A Node Red node for asserting message properties within a flow.

This node will check all of the specified properties in a message or in the global or flow contexts
to confirm that they meet the required format.

The assert node is configured with a list of rules.  Each rule tests one specific property using either the usual comparison operators, ranges, regex, null, not null, boolean values, or type.  Comparisons can be made against static values, other properties, and the property's previous value.  The specification of the property to be checked is quite powerful, allowing the probing inside objects and arrays.

For a message to pass through the assert node, all tests must pass.  The first failing test is reported as an error which can be caught and processed out of band.  Failed messages are dropped from the flow.
