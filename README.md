
# **Basic Conversation**
IBM Watson® Conversation is a question-and-answer system that provides a dialog interaction between the conversation system and users. This style of interaction is commonly called a chatbot.

**Requirements:**
1. IBM Cloud account http://www.bluemix.net

# **Building the Conversation**
**1-  Create an instance of Watson Conversation on IBM Cloud**
Make sure that you are logged in to your IBM Cloud account. Click **Catalog** and then click **Services > Watson > Conversation> choose a name> hit Create**

**2-Click Launch tool to open the Watson Conversation workspace**

**3-Create a Workspace.**

**4-Add intents.**

An intent is a group of examples of things that a user might say to communicate a specific goal or idea. To identify intents, start with something that a user might want and then list the ways that the user might describe it. For each intent, think of the various ways that a user might express his or her desire—those are the examples. Examples can be developed by using a crowdsourcing approach.

For example, in a discussion with the support team, you might gather this set of standard questions that support received from users:

    What is the status of the business application? I could not access it.
    How to get access to a business application?
    How to reset my password for a specific application?
    
**5-Create a new intent.**

For each intent, add examples to train the conversation for intent recognition. 

**5-Test your intent.**
As soon as you create an intent, you can test it by clicking Ask Watson icon in the top, right-hand side of the conversation editor.


**6-Create Your Entity**
entity is a portion of the user's input that you can use to provide a different response to a particular intent.
Click Entities. On the Entities page, click Create new.

Each entity definition includes a set of specific entity values that can be used to trigger different responses. Each value can have multiple synonyms that define different ways that the same value can be specified in user input.

Create entities to represent to the application what the user wants to access.     
Fuzzy logic is a feature that allows Watson Conversation to accept misspelled words. You can enable this feature at the entity level.

**7-Building the Dialog**
A dialog is made up of nodes that define steps in the conversation.


# IMAGE
In the previous image, two dialog nodes are shown. The first node is the standard welcome message. The other node is a catch-all node named "Anything else." Dialog nodes are chained in a tree structure to create an interactive conversation with the user. The evaluation starts at the top, so the welcome node is assessed before the "Anything else" node.

If you click the welcome node, the standard Watson response is "Hello. How can I help you?" To validate how the flow works, you can click the Ask Watson icon.


**8-Define Greeting Node**

The first node addresses greetings in a response to a query such as "hello." Click the welcome node and click Add node below
# IMAGE


A new node is added between the welcome and "Anything else" nodes.

At each node level, you can expand the conversation by adding nodes. If you add nodes at the same level, the flows are parallel. Adding a child node creates a dependent track of conversation, and the conversation branches out into a tree structure.

Name the new node Handle Greetings. In the If bot recognizes field, change the value to #Greetings. The number sign (#) represents a prefix for intent. The condition is triggered when the Watson natural language classifier classifies the query as a greeting intent

**9-Add Responses **

# Image
The previous image also illustrates how to use the multiple responses pattern to avoid being repetitive. The bot can present different answers to the same query. You can allow the system to randomly select an answer from the list of potential responses.


**10- Test your bot by clicking Ask Watson icon **

## Web Application Template for Watson Conversation API Demonstration
Main steps:

1. **"clone or Download"**  this code
2. Create and instance of **Watson Conversation Service**.
4. Create a workspace
5. Configure the Intents
6. Configure the Dialog
7. Take note of Watson Conversation Serice's **Credentials** and **workspace_id**
8. Edit the file **app.js** and fill the fields: *username*, *<password>* and *<workspace_id>* with the data collected in the last step.
```css
var conversation = watson.conversation({
  username:"<username>",//replace with the username from service credential
  password:"<password>",//replace with the password from service credential
  version: 'v1',
  version_date: '2016-07-11'
});
```
```css
var workspace = "<workspace_id>"; //replace with the workspace_id from service credential

```
open a terminal and Change the directory where you saved your code
write the command 
  
  CD C:\Users\NailahALTayyar\Desktop\projects\Basic-Conversation-master;



