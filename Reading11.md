# Event Driven Applications

## Questions

- Why is access control important?


>Access control is important because it is a valuable security technique that can be used to regulate who or what can view or use any given resource. ... Without proper access control you could leave your staff and your company wide open to problems such as data loss, theft or breach of privacy and data protection laws.



- Describe an application that would need access control.


>Login credentials (such as usernames and passwords).
PINs and one-time passwords (OTPs).
Virtual private network (VPN) access to internal networks.
Physical access cards, FOBs, tokens, locks, and keys.
Security guards with access lists.


- What is a role used for?


>A role is a collection of privileges that can be granted to one or more users or other roles



- Why is role based access control more scalable than discretionary or mandatory access control?

>In role based access control you can set control for access data by the role of the user, while mandatory access control is limiting access to resources based on the sensitivity of the information that the resource contains





## Terms


**Term** | **Definition**
------------ | -------------
 Authorization | security mechanism to determine access levels or user/client privileges related to system resources based on the user's identity.
 Role Based Access Control | an approach of restricting system access to authorized users based on their role in an organization.
 Capabilities | They are the operations that can the user do depending on the user role.


## Preview 

- In event-driven programming, there is essentially no normal flow-of-control! Only the event handlers exist.
- Flow-of-control in the program is entirely driven by responding to events.
- Program is driven by responding to events
- Two main models:
    * Polling:
                    * Has the event happened yet?
                    * Are we there yet? Are we there yet? Etc.
     * Delegating:
                           * Here is what I want you to do when this event occurs.