### Joke Website ###

This website uses the Jokes API to fetch random jokes and display them in a responsive, user-friendly interface.

#### Files ####

- `index.html`: The main HTML file that loads the jokes and displays them.
- `jokes.js`: The JavaScript file that fetches the jokes from the API and adds them to the DOM.
- `style.css`: The CSS file that styles the website.

#### Implementation Details ####

**1. Fetching Jokes**

The `jokes.js` file uses the Fetch API to fetch a random joke from the API.

```
fetch('https://icanhazdadjoke.com/')
  .then(response => response.json())
  .then(data => {
    const jokeText = data.joke;

    // Add the joke to the DOM
    const jokeElement = document.createElement('li');
    jokeElement.textContent = jokeText;
    document.querySelector('ul').appendChild(jokeElement);
  })
  .catch(error => {
    console.error('Error fetching joke:', error);
  });
```

**2. Adding Jokes to the DOM**

Once a joke has been fetched from the API, it is added to the DOM as a list item.

```
const jokeElement = document.createElement('li');
jokeElement.textContent = jokeText;
document.querySelector('ul').appendChild(jokeElement);
```

**3. Styling**

The `style.css` file styles the website using CSS.

```
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

ul {
  list-style-type: none;
  display: flex;
  flex-direction: column;
  gap: 1em;
  padding: 0;
}

li {
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 5px;
}
```

#### Documentation ####

The following documentation is available for the Jokes API:

- [API Documentation](https://icanhazdadjoke.com/api)
- [API Reference](https://icanhazdadjoke.com/api/reference)
- [API Examples](https://icanhazdadjoke.com/api/examples)