# react-animated-loading-overlay
This JS react component will display an animated loading overlay and disable user input.

For a working example, view the code sandbox [here](https://codesandbox.io/p/devbox/react-animated-loading-overlay-x72dzk), or see below.

**Example usage:**

*Just feed the loading state into the LoadingOverlay using props, and place whatever visual loading elements you want to display in the center of the overlay, as children.*
```
import { useState } from 'react';
import LoadingOverlay from "./components/LoadingOverlay";

export default function App() {
  const [isLoading, setIsLoading] = useState(false);

  return (
    <LoadingOverlay isLoading={isLoading}>
      <p>Loading...</p>
    </LoadingOverlay>
  );
}
```
