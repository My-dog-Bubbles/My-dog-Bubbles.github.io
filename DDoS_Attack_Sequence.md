## DDoS Attack example 
``` mermaid
sequenceDiagram
participant Attacker
participant BotNets
participant Firewall
participant Webserver

Attacker ->>+ BotNets: I hate this company.<br>I'm going to stop its webserver function.
Attacker ->>+ BotNets: BotNets ATTAAAACK!!!
BotNets ->>+ Firewall: YES BOSS!!!
BotNets ->>+ Firewall: We are on it!
BotNets -->>- Firewall: Taking over the web beep-boop beep-boop
BotNets ->>+ Firewall: No cutomer will be able to in now >=| !!
BotNets ->>+ Firewall: Lets over load the system!!
Firewall -->>- BotNets: Who are these suspcious IPs
BotNets ->>+ Firewall: We are normal I promise
Firewall -->>- BotNets: No you are sus. I will not let you come in.
Webserver ->>+ Firewall: That you for filtering them out firewall.
Webserver ->>+ Firewall: I think that was a DDoS attack!
