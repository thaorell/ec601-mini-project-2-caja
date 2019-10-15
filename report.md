Caja 
## Summary on Cybersecurity 
Protection of computer systems from the theft of or damage to their hardware, software, or electronic data, as well as from the disruption or misdirection of the services they provide

Most common types of cyber attacks:
Phishing/ social engineering: Sending fraudulent communications, usually through email, to steal sensitive data like credit card and identity information.
Malware: malicious software that could block access to some parts of the system or install harmful software. It includes viruses, trojan horses and spyware. 
SQL injection: inserts malicious code into a server that uses SQL and forces the server to reveal information it normally would not
DoS: flooding systems, servers with excessive traffic and bandwidth to exhaust the server, therefore disabling the system 

## CAJA
Caja compiler is a tool for making third HTML, CSS and JavaScript embedding secure 

Uses object-capability security model for flexible security policies, to limit the third party app's scope of control over user data. 

### Pros:
1. Opensource
2. New JavaScript features: new features of ES5 on older browsers
3. Mashups: safe to inline in a page to allow many third party apps. Allowing them to exchange styles adn objects. Host page is protected from the apps: cannot redirect, sniff internal networks or browser history or steal cookies
4. Safely extends JSON with code:  a service can supply both JSON and JavaScript, and websites can compile the JavaScript using Caja to make it safe to embed in their page

### Cons
Outdated and not well maintained

### Example user stories
As a creator of a social sites, I would like to embed some games into my page without allowing untrusted developers to steal my users’ data
→ The developer may use Caja API to plug the games in and limit their policy/permission scope

### Architecture
![alt text](https://developers.google.com/caja/docs/about/guestInsideHost.png)


### Steps:
Include Caja, write a <div> and defensive objects
Tame objects and establish defensive DOM boundary
Cajole and run
Cajoling: The process of making Web content -- HTML with CSS and JavaScript -- safe for inclusion in a host page running Caja. Cajoling involves adding inline checks to make sure the code does not break the invariants Caja needs, and ensuring that the code cannot refer to variables in the host page that are not explicitly given to it.
Caja then runs the code
#### What guest code sees: 
It runs with W3C DOM compliant document object and aan ECMAScript 5 compliant JS VM. 
### API reference: https://google.github.io/caja/docs/cajajs/
 

