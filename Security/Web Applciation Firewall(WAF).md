Provides protection against web attacks
Saves time with managed rules
Improves web traffic visibility
Offers Real-time metrics

To control web requests we can use WAF ACLs, rules and rules groups.


Every rule includes a statement that:
 - Defines criteria for inspecting web requests. 
   Criteria: IP address (originating from), Strings that appear in req, Country of origin, Presence of malicious code or scripts.

 - Specifies an action (allow,block or count) if criteria is met.
 
We can combine multiple statements in a rule using AND, OR and NOT.  

In case no match is found, default action is mentioned.

### Demo
check the Usecases