# useLayoutEffect vs useLayout

`useEffect vs useLayoutEffect`
Both `useEffect` and `useLayoutEffect` are React hooks used for handling side effects in functional components. However, they differ in terms of timing and when they execute.

`useEffect`
Asynchronous Execution: `useEffect `runs asynchronously after the render is committed to the screen.

Non-blocking: It does not block painting on the screen, making it suitable for most side effects that do not require synchronous execution with the render.

Typical Use Cases: It is commonly used for tasks such as data fetching, subscriptions, or any asynchronous operation that doesn't need to be synchronous with the render.

`useLayoutEffect`
Synchronous Execution: `useLayoutEffect` runs synchronously after all DOM mutations but before the browser repaints.

Blocking: It can potentially block painting on the screen, so it's suitable for tasks that require measurements or manipulations on the DOM immediately after the render.

Typical Use Cases: It is often used for tasks such as measuring the dimensions of DOM elements or performing synchronous DOM manipulations.


Choose Wisely: The choice between useEffect and useLayoutEffect depends on the specific use case. If you need to interact with the DOM synchronously, such as for animations or precise measurements, useLayoutEffect might be more appropriate. Otherwise, for most asynchronous tasks, useEffect is generally sufficient and has better performance characteristics.


## Available Scripts

### `yarn start`

### `yarn test`

### `yarn build`

### `yarn eject`

# 


### Components

- HoverComponent:

This component changes its background color based on the hover state. It uses useLayoutEffect to update the background color synchronously after the render.

- SearchUseEffect:

This component makes an API call using `useEffect` when it mounts. It fetches data from the "https://random.dog/woof.json" endpoint and displays either a video or an image based on the file type.

- SearchUseLayoutEffect:

Similar to SearchUseEffect, this component also makes an API call using `useLayoutEffect.` It fetches data from the same endpoint and displays either a video or an image, along with the file size.
App Component
The App component renders SearchUseEffect and SearchUseLayoutEffect components, displaying the results of API calls.
It also renders the HoverComponent.
Steps:

- Component Creation:
1. HoverComponent, 
2. SearchUseEffect, 
3. SearchUseLayoutEffect.


- API Fetching:

Both SearchUseEffect and SearchUseLayoutEffect components fetch data from the `"https://random.dog/woof.json"` endpoint.
Debugging:

Included debugging statements to check if the fetched data contains a video or an image, and you've logged the file size

- Styling:

Applied some styling to make the components visually appealing.

- App Integration:

Integrated all three components into main App component and rendered them within a div with the class App__content.


# uselayouteffect-useffect-difference-react-ts
