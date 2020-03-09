
# ChatBot-COSC-310

Chatbot Topic: **Software Development Life Cycle**

Language: ``` JavaScript ```

### Why JavaScript 
JavaScript has enough to tools to build the same chatbot that we would have made with a programming langauge but with additional perks. Writing it in JavaScript provides us to easily integrate into a hosted website and develop an aesthetic UI.

### Input Examples:
Try to ask these statements to chatbot!

```
What is agile?
```
```
What are some incremental drawbacks?
```
```
Are there any benefits to Extreme Programming?
```

## The Code
### Frontend

The website is a single page application developed in Vue.js with a Vuetify(UI) component gramework. This makes it easy to implmenent stylish Material Design based components.

### Backend 

#### Search Methods
At the very core, we implemented a hashmap in JavaScript (thanks to freeCodeCamp) that allows us to put and get data at O(1) time. 

#### Word Search
In regards to word search, we decided that we would have a bank of key words that would dictate the response of the chatbot based on
matching key words. 

We take the user input, seperate the words, and check if each word exists in the hashmap. If more than one matched key word exists, concatenate the words in alphabetica order. Once all words are check, take the concatenated string and search it up in the hashmap. Note, an issue is lots of data is required; However, the project is small enough to write this data and the topics are specific enough to acquire the general intent of the user response with a 1-3 words. If it no words are matched, there are multiple default sentences to use and guide the user into asking something the chatbot can response. Finally, we will add responses that are a bit more humane such as reponses in greetings, jokes, and farewells.

#### Functions:

Here, we will be describing the process from when the user input their message to the user reeciving a response from chatbot.

Once the user types something in the search bar and presses the send button, the first function is called. Here, a ```<li>``` is created with the text content being the user's input message and is printed in the messenging box. Next, the user's input is sent to be analyzed(see *Word Search* above). Once the matched or default response is selected, it becomes the text content of another ```<li>``` tag and placed into the messenging box.

#### Hosting:

Google Firebase is currently hosting our [site](https://chatbot-310-app.firebaseapp.com/).

Apart from hosting, Firebase includes other features such as a database. Cloud Firestore is a noSQL document based database and we could eventually move our data there. Future plans...


