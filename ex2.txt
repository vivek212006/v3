function sendMessage() {
  const userInput = document.getElementById("user-input");
  const chatBox = document.getElementById("chat-box");
  const userText = userInput.value.trim();
  if (!userText) return;  
   chatBox.innerHTML += `<div><strong>You:</strong> ${userText}</div>`;
let botResponse = getBotResponse(userText.toLowerCase());
  chatBox.innerHTML += `<div><strong>Bot:</strong> ${botResponse}</div>`;
   chatBox.scrollTop = chatBox.scrollHeight;
  userInput.value = "";
}
function getBotResponse(input) {
  if (input.includes("hello") || input.includes("hi")) {
    return "Hello! How can I help you?";
	  } else if (input.includes("your name")) {
    return "I'm Mini Bot!";
		    } else if (input.includes("bye")) {
    return "Goodbye! Have a great day!";
  } else {
    return "I'm not sure how to respond to that.";
  }
}
