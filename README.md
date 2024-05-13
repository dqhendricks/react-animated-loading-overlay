# react-animated-loading-overlay
This JS react component will display an animated loading overlay and disable user input.

For a working example, view the code sandbox [here](https://codesandbox.io/p/devbox/react-bootstrap-toast-queue-provider-8flm3m), or see below.

**Example usage:**

*1) Wrap any children that need to use the Toast Queue Provider. Available props { postion, autohideDelay, maxToasts }.*
```
import ToastQueueProvider from "./components/ToastQueueProvider";
import ExampleConsumer from "./components/ExampleConsumer";

export default function App() {
  return (
    <ToastQueueProvider>
      <ExampleConsumer />
    </ToastQueueProvider>
  );
}
```

*2) Child components may import and use context to gain access to `createToast({ title, body, autohide = true, bg = undefined })` function*
```
import { useContext } from "react";

import { ToastQueueContext } from "./ToastQueueProvider";

export default function ExampleConsumer() {
  const { createToast } = useContext(ToastQueueContext);

  return (
    <button
      onClick={() => createToast({ title: "Success", body: "You have queued a toast!" })}
    >
      Create New Toast
    </button>
  );
}
```
