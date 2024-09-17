# Rubeus

<br>

***Spawn another powershell process under a different user using their credentials***

- $ `.\Rubeus.exe createnetonly /program:powershell /show /username:marth /password:Winner77 /domain:lab.local`

<br>

***Request a ticket-granting-ticket from the KDC using user credentials and pass the ticket to memory.***

- $ `.\Rubeus.exe asktgt /user:martha /password:Winner77 /domain:lab.local /ptt /nowrap`
    - Sometimes you have to start a process using the users credentials with **createnetonly** and then request the ticket-granting-ticket from that process so you don't get hit with access denied.

<br>

***Sometimes enumeration with Bloodhound will reveal vulnerable ACL that would be impossible to enumerate using PowerView. Use both.***
- Make sure that the SharpHound.exe you are using is compatible with the Bloodhound version you are using otherwise it will throw "bad JSON" error.
