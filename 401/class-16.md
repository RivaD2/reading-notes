# Access Control

![dennis](https://media.giphy.com/media/FmyCxAjnOP5Di/giphy.gif)

**Access control models are responsible for granting or restricting access to resources. They depend on two things: user identification (verified by one or more authentication schemes) and feature authorization.**

ACCESS CONTROL asks, **"ARE YOU WHO YOU SAY YOU ARE? AND SHOULD YOU HAVE ACCESS TO THIS PARTICULAR RESOURCE?"**
- Before you grant access to a resource, you need to know that the user is they are claiming to be (authentication) and whether or not the user should have access to a given resource (authorization).**



### Questions related to accesss control:

1. Why is access control important? 
 - Access control is important because it helps to verify that a user is not someone else and that they can verify this. It is essential in the protection of data/confidential information. It mitigates risks greatly by ensuring that someone has the permission to do certain things. 
  
2. Describe an application that would need access control. 
   - There are so many examples where apps would need access control. A user logging into a banking website, any mobile application, basically any app that has login capabilites or that stores user information. A basic website wouldn't really need it but every other app out there that asks users to login.
  
3. What is a role used for?
   A role is used to say which users have certain types of access. A role provides different access rights based off the type of role assigned to a user. Some users may be able to update or change information, others may only be able to read information, which means they can only look at data (whatever the app is serving.) Some users have admin roles which means they can read, write, delete, and change data. Basically a role is a way to protect sensitive information and mitigate risks. It is additional security layer.

4. Why is role based access control more scalable than discretionary or mandatory access control?
With role based access control, you can create rules and change permissions easier as you can update them all at once. With the other forms of access control, you would have to go in individually to update each users permissions.


### New Vabulary to Learn:

- **Authorization**:** In simple terms, authorization is the process of verifying what a user has access to.
  
- **Role Based Access Control:** RBAC restricts system access. It involves setting permissions and privileges to enable access to authorized users. 
  
- **Capabilities:** These are the rights that a role has. Read, write, delete, change are capabilities. They are essentially a set of access rights. 
