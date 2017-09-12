```
 console.log("loaded bro");

// Dramatis Personae
const hobbits = [
  'Frodo Baggins',
  'Samwise \'Sam\' Gamgee',
  'Meriadoc \'Merry\' Brandybuck',
  'Peregrin \'Pippin\' Took'
];

const buddies = [
  'Gandalf the Grey',
  'Legolas',
  'Gimli',
  'Strider',
  'Boromir'
];

const lands = ['The Shire', 'Rivendell', 'Mordor'];
const body = document.body;

const makeMiddleEarth = function () {
    // create a section tag with an id of middle-earth
    const middleEarth = document.createElement('section');
    for(let i = 0; i < lands.length; i++) {
      // add each land as an article tag
      const land = document.createElement('article');
      // inside each article tag include an h1 with the name of the land
      land.innerHTML = '<h1>' + lands[i] + '</h1>';
      middleEarth.appendChild(land);
    }
    // append middle-earth to your document body
    body.appendChild(middleEarth);
}
makeMiddleEarth();


const theShire = body.getElementsByTagName('article')[0];
const rivendell = body.getElementsByTagName('article')[1];
const mordor = body.getElementsByTagName('article')[2];
const makeHobbits = function () {
  // display an unordered list of hobbits in the shire (which is the first article tag on the page)
  const hobbitList = document.createElement('ul');
  for(let i = 0; i < hobbits.length; i++) {
  // give each hobbit a class of hobbit
    const hobbit = document.createElement('li');
    hobbit.className = 'hobbit';
    hobbit.innerText = hobbits[i];
    hobbitList.appendChild(hobbit);
  }
  theShire.appendChild(hobbitList);
}
makeHobbits();


const frodo = body.getElementsByTagName('li')[0];
const keepItSecretKeepItSafe = function () {
  // create a div with an id of 'the-ring'
  const theRing = document.createElement('div');
  theRing.setAttribute('id', 'the-ring');
  // give the div a class of 'magic-imbued-jewelry'
  theRing.setAttribute('class', 'magic-imbued-jewelry');
  // add the ring as a child of Frodo
  frodo.appendChild(theRing);
}
keepItSecretKeepItSafe();


const makeBuddies =  () => {
  // create an aside tag
  const aside = document.createElement('aside');
  const buddyList = document.createElement('ul');
  for(let i = 0; i < buddies.length; i++) {
    // attach an unordered list of the 'buddies' in the aside
    const buddy = document.createElement('li');
    buddy.textContent = buddies[i];
    buddyList.appendChild(buddy);
  }
  // insert your aside as a child element of rivendell
  aside.appendChild(buddyList);
  rivendell.appendChild(aside);
}
makeBuddies();


const strider = rivendell.getElementsByTagName('li')[3];

const beautifulStranger = function () {
  // change the 'Strider' textnode to 'Aragorn'
  strider.textContent = 'Aragon';
}
beautifulStranger();


const hobbits = theShire.getElementsByTagName('ul');
function leaveTheShire() {
  // assemble the hobbits and move them to Rivendell
  rivendell.appendChild(hobbits[0]);
}
leaveTheShire();

//What is query selector all? Check the docs. 
const fellowshipMembers = rivendell.querySelectorAll('li');

const forgeTheFellowShip = function () {
  // create a new div called 'the-fellowship' within rivendell
  const theFellowship = document.createElement('div');
  theFellowship.setAttribute('id', 'the-fellowship');
  for(let i = 0; i < fellowshipMembers.length; i++) {
    theFellowship.appendChild(fellowshipMembers[i]);
    // alert(fellowshipMembers[i].textContent + ' has joined the fellowship!');
  }
  // add each hobbit and buddy one at a time to 'the-fellowship'
  // after each character is added make an alert that they have joined your party
  rivendell.appendChild(theFellowship);
}
forgeTheFellowShip();


const gandalf = fellowshipMembers[0];
const theBalrog = function () {
  // change the 'Gandalf' textNode to 'Gandalf the White'
  gandalf.textContent = 'Gandalf the White';
  // apply style to the element
  gandalf.style.border = '3px solid gray';
  // make the background 'white', add a grey border
  gandalf.style.backgroundColor = 'white';
}
theBalrog();


const boromir = fellowshipMembers[4];
const hornOfGondor = function () {
  alert('the horn of gondor has blown');
  // pop up an alert that the horn of gondor has been blown
  boromir.style.textDecoration = 'line-through';
  // Boromir's been killed by the Uruk-hai!
  // Remove Boromir from the Fellowship
  boromir.parentNode.removeChild(boromir)
}
hornOfGondor();


const sam = fellowshipMembers[6];
const itsDangerousToGoAlone = function () {
  // take Frodo and Sam out of the fellowship and move them to Mordor
  mordor.appendChild(frodo);
  mordor.appendChild(sam);
  const mountDoom = document.createElement('div');
  mountDoom.setAttribute('id', 'mount-doom');
  mordor.appendChild(mountDoom);
  // add a div with an id of 'mount-doom' to Mordor
}
itsDangerousToGoAlone();


const gollum, theRing;
const weWantsIt = function () {
  // Create a div with an id of 'gollum' and add it to Mordor
  gollum = document.createElement('div');
  gollum.setAttribute('id', 'gollum');
  theRing = frodo.getElementsByTagName('div')[0];
  gollum.appendChild(theRing);
  // Remove the ring from Frodo and give it to Gollum
  // Move Gollum into Mount Doom
  const mountDoom = mordor.getElementsByTagName('div')[0];
  mountDoom.appendChild(gollum);
}
weWantsIt();


const thereAndBackAgain = function () {
  gollum.parentElement.removeChild(gollum);
  // remove Gollum and the Ring from the document
  // remove all the baddies from the document
  const hobbitUL = document.createElement('ul');
  const hobbits = body.querySelectorAll('.hobbit');
  for(let i = 0; i < hobbits.length; i++){
    hobbitUL.appendChild(hobbits[i]);
  }
  theShire.appendChild(hobbitUL);
  // Move all the hobbits back to the shire
}
thereAndBackAgain();
```
