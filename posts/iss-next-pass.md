 This project grew out of want to practice implementing APIs in [React](https://reactjs.org). React is great for handling asynchronous processes because state is built into its components. Almost without telling it, the app understands how to wait until the data is available before rendering it. And if you need to call the API again, its easy just to revert back to the waiting state.

 The project was also a great oportunity to practice React's method of abstracting the layout from the application itself. If you aren't familiar, React works like this: you write "components" which are functions or classes; these components do some processing on data they recieve, and then return a block of HTML-like markup called JSX (JavaScript extended) which constitutes the component's visual output. Components recieve data as their `props` (properties) and can pass data to other components only by rendering them as elements in their JSX returns and passing the data as attributes. For example in this app the `Controller` component renders a `Presentational` component like so,

```jsx
return (
  <Presentational
    latitude={this.state.latitude}
    longitude={this.state.longitude}
    nextPass={this.state.nextPass}
  />
);
```

passing the information `Presentational` will render. `Presentational` then renders

```jsx
<p>
  Your location: latitude {props.latitude},
  longitude {props.longitude}
</p>
```

In both cases, `{}` are used to interpolate JS variables into the JSX.

  You may notice that there is no indication of CSS layout or classes in any of this code, and that is not because I edited it out. The `Controller` component is itself rendered by a `Layout` component like so:

```jsx
const Layout = () =>
  <div className="App-container">
    <div className="App">
      <Controller />
    </div>
  </div>
 ```

This layer of abstraction allows me to modify and scale the layout without ever touching the app itself— `Layout` can live in another file! While it is a common practice to separate concerns by using nested templates like this on large webpages, it is often impractical to do so with small apps.

 I hope you enjoy this one. I know I do. Using it reminds me of the incredible strength of the internet for providing realtime information about the things in your world. Or just off it, for that matter.
