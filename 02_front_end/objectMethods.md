## Building Object Methods

* We can add `abilities` (functions) to Objects
* When we assign a function to an Object, it becomes a **method**

```javascript

const err = {
  name: 'Error',
  sayMyName: () => {
    return 'I am ' + this.name;
  },
  makeFunOfGreenClothes: () => {
    return "Your clothes look silly, little elf-man";
  },
  changeName: (newName) => {
    if (typeof(newName) == 'string') {
      const oldName = this.name;
      this.name = newName;
      return 'Name has been changed to: ' + newName + ' and our old name was ' + oldName;
    } else {
      return 'That name is not a valid string';
    }
  }
};
err.sayName();
err.changeName('Solution');

```
