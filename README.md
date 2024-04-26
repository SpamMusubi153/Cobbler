# Cobbler
Interact with the Gemini REST API using Pure Apple Shortcuts

---

This set of shortcuts provides a pure Apple Shortcut interface for users to interact with Google's 1.5 Pro Gemini model.

Right now, these shortcuts are capable of taking care of:

- The (sometimes tedious) process of constructing and extracting information from the JSON requests used to communicate with the Gemini REST API.

- Through **Gemini Conversations**, keeping track of and sending conversation history so users can have multi-turn interactions.

- Through **Gemini Conversations**, providing system instructions to shape model responses.

Originally, I created this series of shortcuts for my grandmother, who haden't yet been able to try a "chatbot". Using this shortcut, I was able to bridge the currently free Gemini LLM (Large Language Model, from Machine Learning) to Apple's iMessage, a service she is familiar with.

If enough users are interested, I might investigate adding additional features to these shortcuts, such as:

- Additional Gemini configuration options
- Multi-user conversations
- A demonstration of integration with Apple iMessages to automatically reply to messages

---

### How to Get Started

1. Register for a Gemini API Key from Google at
https://ai.google.dev/


> API stands for "Application Program Interface". It is a common way **two programs exchange data.** In this exchange, your API Key is **like a password**, so make sure to keep it safe! Here, we'll be using it to connect Google Gemini to our Apple Shortcut.

2. Run the **Save API Key** shortcut below to save a copy of your key to your device. This should only have to be done once when you setup each device, or if you need to manually change your API Key.

> If you want to do this manually, you can copy and save your API key to a file called "Key.txt" at the following path:
>
>iCloud Drive > Apps > Gemini > Preferences > Key.txt

3. Follow the instructions below for either running the **Gemini Basic** or **Gemini Conversations** shortcut.

**Congratulations!** You can now interact with Gemini on your device through Apple Shortcuts!


## The Shortcuts

### [Save API Key 1.0](https://github.com/SpamMusubi153/Cobbler/blob/main/Save%20API%20Key/Cobbler%20%7C%20Save%20API%20Key%201.0.shortcut)

This shortcut helps you save your Gemini API Key to a device.


### [Gemini Basic 1.0](https://github.com/SpamMusubi153/Cobbler/blob/main/Gemini%20Basic/Cobbler%20%7C%20Gemini%20Basic%201.0.shortcut)

This shortcut enables single-turn conversations with Gemini. It can be used directly by a user, immediately displaying Gemini's response and copying it to the clipboard. It can also respond to a text prompt from another shortcut, providing Gemini's response as the shortcut's response.


### [Gemini Conversations 2.0](https://github.com/SpamMusubi153/Cobbler/blob/main/Gemini%20Conversations/Cobbler%20%7C%20Gemini%20Conversations%202.0.shortcut)

This shortcut enables multi-turn Gemini conversations with separate conversation histories. It must be run by another shortcut which passes in a dictionary with the following three items:

- A unique "user_identifier" that identifies the specific user a conversation should be attributed to.
- A "user_prompt" that contains the user's most recent prompt.
- A "system_instruction" that can contain conversation-style directives and instructions to Gemini that can help guide its response.

The shortcut then automatically saves the conversation history and returns Gemini's text response.

<br>

---

<br>

<noscript><a href="https://liberapay.com/MusubiToTheMax/donate"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a></noscript>

Thank you for stopping by! At this time, I am still working through college. If you found this project helpful, I would appreciate any support you are able to lend.