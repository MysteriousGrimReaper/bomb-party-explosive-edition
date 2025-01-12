# BombParty: Explosive Edition

[My Notes](notes.md)

BombParty: Explosive Edition is a new twist on the fast-paced word game BombParty, featuring new gamemodes.


> [!NOTE]
>  This is a template for your startup application. You must modify this `README.md` file for each phase of your development. You only need to fill in the section for each deliverable when that deliverable is submitted in Canvas. Without completing the section for a deliverable, the TA will not know what to look for when grading your submission. Feel free to add additional information to each deliverable description, but make sure you at least have the list of rubric items and a description of what you did for each item.

> [!NOTE]
>  If you are not familiar with Markdown then you should review the [documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) before continuing.

## 🚀 Specification Deliverable

> [!NOTE]
>  Fill in this sections as the submission artifact for this deliverable. You can refer to this [example](https://github.com/webprogramming260/startup-example/blob/main/README.md) for inspiration.

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [x] Proper use of Markdown
- [x] A concise and compelling elevator pitch
- [x] Description of key features
- [x] Description of how you will use each technology
- [x] One or more rough sketches of your application. Images must be embedded in this file using Markdown image references.

### Elevator pitch

BombParty is an explosively fast party game where players must think of a word on the spot or get eliminated. BombParty: Explosive Edition takes this up to the next level with brand new gamemodes to shake up how the game is played.

### Design
- All gameplay features from vanilla BombParty (BP). Here is a screenshot of what gameplay looks like in vanilla BP:
![[BombParty Demo Image.png]]
- Login page design: 
![[Login Page.png]]

Here is a sequence diagram that shows how the server would handle giving prompts and also receiving words:

```mermaid
sequenceDiagram
    actor A as Alice
    actor B as Bob
    participant S as Server
    S->>A: Prompt: NE
    S-->>B: Prompt: NE
    A->>S: Send word: SCENE
    S-->>B: Alice sent word: SCENE
    S->>B: Prompt: TA
    S-->>A: Prompt: TA
    B->>S: Send word: DATA
    S-->>A: Bob sent word: DATA
```

### Key features

- Secure login over HTTPS
- Ability to play BP, which includes:
	- Hosting and setting up a private game lobby
	- Gameplay:
		- Players take turns in a circle, with each player having a limited time to respond.
		- On a player's turn, they are presented with a prompt consisting of a few letters.
		- The player must type a word (usually 3 letters or more) that contains the given letters in the same order before the "bomb" explodes.
		- If a player fails to input a valid word before the time runs out, they lose a life or are eliminated.
- New BP:EE features:
	- New gamemodes selectable by the host:
		- Tag - Players with the bomb chooses who the bomb goes to next.
		- Red Light Green Light - Players score points by typing words with the given letters, but lose lives if they type while a red light is shown.

### Technologies

I am going to use the required technologies in the following ways.

- **HTML** - Views for login, lobby entry, and game
- **CSS** - Application styling for different devices and screens, responsive design
- **React** - Login, handling game logic
- **Service** - Endpoints for authentication, call to Google's reCaptcha to block bots
- **DB/Login** - Store users and credentials in database, as well as word list
- **Websocket** - As users play, their words update live to other players

## 🚀 AWS deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Server deployed and accessible with custom domain name** - [My server link](https://yourdomainnamehere.click).

## 🚀 HTML deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **HTML pages** - I did not complete this part of the deliverable.
- [ ] **Proper HTML element usage** - I did not complete this part of the deliverable.
- [ ] **Links** - I did not complete this part of the deliverable.
- [ ] **Text** - I did not complete this part of the deliverable.
- [ ] **3rd party API placeholder** - I did not complete this part of the deliverable.
- [ ] **Images** - I did not complete this part of the deliverable.
- [ ] **Login placeholder** - I did not complete this part of the deliverable.
- [ ] **DB data placeholder** - I did not complete this part of the deliverable.
- [ ] **WebSocket placeholder** - I did not complete this part of the deliverable.

## 🚀 CSS deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Header, footer, and main content body** - I did not complete this part of the deliverable.
- [ ] **Navigation elements** - I did not complete this part of the deliverable.
- [ ] **Responsive to window resizing** - I did not complete this part of the deliverable.
- [ ] **Application elements** - I did not complete this part of the deliverable.
- [ ] **Application text content** - I did not complete this part of the deliverable.
- [ ] **Application images** - I did not complete this part of the deliverable.

## 🚀 React part 1: Routing deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Bundled using Vite** - I did not complete this part of the deliverable.
- [ ] **Components** - I did not complete this part of the deliverable.
- [ ] **Router** - Routing between login and voting components.

## 🚀 React part 2: Reactivity

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **All functionality implemented or mocked out** - I did not complete this part of the deliverable.
- [ ] **Hooks** - I did not complete this part of the deliverable.

## 🚀 Service deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Node.js/Express HTTP service** - I did not complete this part of the deliverable.
- [ ] **Static middleware for frontend** - I did not complete this part of the deliverable.
- [ ] **Calls to third party endpoints** - I did not complete this part of the deliverable.
- [ ] **Backend service endpoints** - I did not complete this part of the deliverable.
- [ ] **Frontend calls service endpoints** - I did not complete this part of the deliverable.

## 🚀 DB/Login deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **User registration** - I did not complete this part of the deliverable.
- [ ] **User login and logout** - I did not complete this part of the deliverable.
- [ ] **Stores data in MongoDB** - I did not complete this part of the deliverable.
- [ ] **Stores credentials in MongoDB** - I did not complete this part of the deliverable.
- [ ] **Restricts functionality based on authentication** - I did not complete this part of the deliverable.

## 🚀 WebSocket deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Backend listens for WebSocket connection** - I did not complete this part of the deliverable.
- [ ] **Frontend makes WebSocket connection** - I did not complete this part of the deliverable.
- [ ] **Data sent over WebSocket connection** - I did not complete this part of the deliverable.
- [ ] **WebSocket data displayed** - I did not complete this part of the deliverable.
- [ ] **Application is fully functional** - I did not complete this part of the deliverable.
