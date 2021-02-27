# без бттв
let textArea = document.querySelector('.tw-textarea')
let sendButton = document.querySelector('.tw-mg-l-05 .tw-core-button')
let lastNumber = 0
let sendedByMe = true

let observer = new MutationObserver((items) => {
items.forEach(item => {
let container = item.target.childNodes[item.target.childNodes.length -1]
console.log(container)
let message = container.querySelector('.text-fragment').textContent
if (!isNaN(message)) {
message = Number(message)
if (message > lastNumber) {
console.log(lastNumber)
lastNumber = message
if (!sendedByMe) {
console.log('sended')
const nativeInputValueSetter = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, "value").set;
nativeInputValueSetter.call(textArea, (lastNumber + 1).toString());
let ev2 = new Event('input', { bubbles: true});
document.querySelector('.tw-textarea').dispatchEvent(ev2);
sendButton.click()
lastNumber += 1
sendedByMe = true
} else {
sendedByMe = false
}
}
}
})
});
observer.observe(document.querySelector('.chat-scrollable-area__message-container'), {
childList: true,
subtree: false,
});

с бттв
let textArea = document.querySelector('.tw-textarea')
let sendButton = document.querySelectorAll('.tw-mg-l-05 .tw-core-button')
sendButton = sendButton[sendButton.length - 1]
let lastNumber = 0
let sendedByMe = true

let observer = new MutationObserver((items) => {
items.forEach(item => {
let container = item.target.childNodes[item.target.childNodes.length -1]
let message = container.querySelector('.text-fragment').textContent
if (!isNaN(message)) {
message = Number(message)
if (message > lastNumber) {
lastNumber = message
if (!sendedByMe) {
console.log('sended')
const nativeInputValueSetter = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, "value").set;
nativeInputValueSetter.call(textArea, (lastNumber + 1).toString());
let ev2 = new Event('input', { bubbles: true});
document.querySelector('.tw-textarea').dispatchEvent(ev2);
sendButton.click()
lastNumber += 1
sendedByMe = true
} else {
sendedByMe = false
}
}
}
})
});
observer.observe(document.querySelector('.chat-scrollable-area__message-container'), {
childList: true,
subtree: false,
});


let textArea = document.querySelector('.tw-textarea')
let sendButton = document.querySelectorAll('.tw-mg-l-05 .tw-core-button')
sendButton = sendButton[sendButton.length - 1]
let lastNumber = 3395
let sendedByMe = true

let observer = new MutationObserver((items) => {
items.forEach(item => {
let container = item.target.childNodes[item.target.childNodes.length -1]
let message = container.querySelector('.text-fragment').textContent
if (!isNaN(message)) {
message = Number(message)
if (message > lastNumber && message - 20 < lastNumber) {
console.log(lastNumber)
lastNumber = message
if (!sendedByMe) {
console.log('sended')
const nativeInputValueSetter = Object.getOwnPropertyDescriptor(window.HTMLTextAreaElement.prototype, "value").set;
nativeInputValueSetter.call(textArea, (lastNumber + 1).toString());
let ev2 = new Event('input', { bubbles: true});
document.querySelector('.tw-textarea').dispatchEvent(ev2);
sendButton.click()
lastNumber += 1
sendedByMe = true
} else {
sendedByMe = false
}
}
}
})
});
observer.observe(document.querySelector('.chat-scrollable-area__message-container'), {
childList: true,
subtree: false,
});
