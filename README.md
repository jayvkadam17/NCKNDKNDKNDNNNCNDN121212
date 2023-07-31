import React from 'react';

const Person = ({ name, age }) => {
  return (
    <p>
      Name: {name}, Age: {age}
    </p>
  );
};

export default Person;


////////////////////////////////////////////
import React from 'react';

const Button = ({ text, onClick }) => {
  return (
    <button onClick={onClick}>
      {text}
    </button>
  );
};

export default Button;

/////////////////////////////////
import React from 'react';

const Header = ({ title }) => {
  return (
    <h1>{title}</h1>
  );
};

export default Header;
/////////////////////////////////////////////////////////////////////



import React from 'react';

const List = ({ items }) => {
  return (
    <ul>
      {items.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
};

export default List;

///////////////
import React from 'react';
import Person from './Person';
import Button from './Button';
import Header from './Header';
import List from './List';

const App = () => {
  const handleButtonClick = () => {
    alert('Button clicked!');
  };

  const listItems = ['Item 1', 'Item 2', 'Item 3'];

  return (
    <div>
      <Header title="React Components Example" />
      <Person name="John Doe" age={30} />
      <Button text="Click Me" onClick={handleButtonClick} />
      <List items={listItems} />
    </div>
  );
};

export default App;
