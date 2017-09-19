## Fellowship (Journey to MorDOMr) Solution

Below is one of *many* solutions to this weekend's homework.

```javascript
$(() => {

  console.log("Linked.");

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

  // we don't need a var to hold body with jQuery.  
  // const body = document.querySelector('body');

  // Chapter 1
  makeMiddleEarth() => {
      // create a section tag with an id of middle-earth
      const middleEarth = $('<section>');
      for(let i = 0; i < lands.length; i++) {
        // add each land as an article tag
        const land = $('<article>');
        // inside each article tag include an h1 with the name of the land
        const landName = $('<h1>');
        landName.text(lands[i]);
        land.append(landName);
        middleEarth.append(land);
      }
      // append middle-earth to your document body
      $('body').append(middleEarth);
  }

  makeMiddleEarth();

  const theShire = $('article').eq(0);
  const rivendell = $('article').eq(1);
  const mordor = $('article').eq(2);;

  // Chapter 2
  makeHobbits() => {
    // display an unordered list of hobbits in the shire (which is the first article tag on the page)
    const hobbitList = $('<ul>');
    for(let i = 0; i < hobbits.length; i++) {
    // give each hobbit a class of hobbit
      const hobbit = $('<li>');
      hobbit.addClass('hobbit');
      hobbit.text(hobbits[i]);
      hobbitList.append(hobbit);
    }
    theShire.append(hobbitList);
  }

  makeHobbits();

  const frodo = $('li').eq(0);

  // Chapter 3
  keepItSecretKeepItSafe() => {
    // create a div with an id of 'the-ring'
    const theRing = $('<div>');
    theRing.prop('id', 'the-ring');
    // give the div a class of 'magic-imbued-jewelry'
    theRing.addClass('magic-imbued-jewelry');
    // add an event listener so that when a user clicks on the ring, the nazgulScreech function (provided) is invoked
    // theRing.addEventListener('click', nazgulScreech);
    // add the ring as a child of Frodo
    frodo.append(theRing);
  }

  keepItSecretKeepItSafe();


  // Chapter 4
  makeBuddies() => {
    // create an aside tag
    const aside = $('<aside>');
    const buddyList = $('<ul>');
    for(let i = 0; i < buddies.length; i++) {
      // attach an unordered list of the 'buddies' in the aside
      const buddy = $('<li>');
      buddy.text(buddies[i]);
      buddyList.append(buddy);
    }
    // insert your aside as a child element of rivendell
    aside.append(buddyList);
    rivendell.append(aside);
  }
  makeBuddies();

  const strider = rivendell.find('li').eq(3);


  // Chapter 5
  beautifulStranger() => {
    // change the 'Strider' text to 'Aragorn'
    strider.text('Aragorn');
  }

  beautifulStranger();

  const hobbits = theShire.find('ul').eq(0);

  // Chapter 6
  leaveTheShire() => {
    // assemble the hobbits and move them to Rivendell
    rivendell.append(hobbits);
  }
  leaveTheShire();

  const fellowshipMembers = rivendell.find('li');


  // Chapter 7
  forgeTheFellowShip() => {
    // create a new div called 'the-fellowship' within rivendell
    const theFellowship = $('<div>');
    theFellowship.prop('id', 'the-fellowship');
    for(let i = 0; i < fellowshipMembers.length; i++) {
      theFellowship.append(fellowshipMembers.eq(i));
      alert(fellowshipMembers.eq(i).text() + ' has joined the fellowship!');
    }
    // add each hobbit and buddy one at a time to 'the-fellowship'
    // after each character is added make an alert that they have joined your party
    rivendell.append(theFellowship);
  }

  forgeTheFellowShip();

  const gandalf = fellowshipMembers.eq(0);

  // Chapter 8
  theBalrog() => {
    // change the 'Gandalf' textNode to 'Gandalf the White'
    gandalf.text('Gandalf the White');
    // apply style to the element
    gandalf.css('border', '3px solid slategrey');
    // make the background 'white', add a grey border
    gandalf.css('backgroundColor', 'white');
  }

  theBalrog();

  const boromir = fellowshipMembers.eq(4);

  // Chapter 9
  hornOfGondor() => {
    alert('the horn of gondor has blown');
    // pop up an alert that the horn of gondor has been blown
    // put a linethrough on boromir's name
    boromir.css('text-decoration', 'line-through');
    alert('Boromir\'s been killed by the Uruk-hai!');
    // Remove Boromir from the Fellowship
    rivendell.append(boromir);
  }

  hornOfGondor();

  const sam = fellowshipMembers.eq(6);

  // Chapter 10
  itsDangerousToGoAlone() => {
    // take Frodo and Sam out of the fellowship and move them to Mordor
    mordor.append(frodo);
    mordor.append(sam);
    // add a div with an id of 'mount-doom' to Mordor
    const mountDoom = $('<div>');
    mountDoom.prop('id', 'mount-doom');
    mordor.append(mountDoom);
  }

  itsDangerousToGoAlone();

  const gollum, theRing;

  // Chapter 11
  weWantsIt() => {
    // Create a div with an id of 'gollum' and add it to Mordor
    gollum = $('<div>');
    gollum.prop('id', 'gollum');
    theRing = frodo.find('#the-ring').eq(0);
    gollum.append(theRing);
    // Remove the ring from Frodo and give it to Gollum
    // Move Gollum into Mount Doom
    const mountDoom = mordor.find('#mount-doom').eq(0);
    mountDoom.append(gollum);
  }

  weWantsIt();

  // Chapter 12
  thereAndBackAgain() => {
    gollum.remove();
    // remove Gollum and the Ring from the document
    const hobbitUL = $('<ul>');
    const hobbits = $('.hobbit');
    for(let i = 0; i < hobbits.length; i++){
      hobbitUL.append(hobbits.eq(i));
    }
    theShire.append(hobbitUL);
    // Move all the hobbits back to the shire

  }

  thereAndBackAgain();

  golemGotCash() => {
    const bling = $('<div>');
    bling.prop('id', 'lord-of-the-bling');
    $('body').append(bling);
  }

  golemGotCash();

});
```
