<!-- markdownlint-disable-next-line -->
<h1 align="center">filou-dialog-modal</h1>


## Installation

filou dialog modal is available as an [npm package](https://www.npmjs.com/package/filou-dialog-modal).


```sh
// with npm
npm i filou-dialog-modal
// with yarn
yarn add filou-dialog-modal
```

## Usage

Here is a quick example to get you started, **it's all you need**:

```jsx
import React, { useState } from "react";
import { AlertDialog } from 'filou-dialog-modal';

export const App = () => {
  const [openModal, setOpenModal] = useState(false);
  
  const onOpenModal = () => setOpenModal(true);
  const onCloseModal = () => setOpenModal(false);

  const handleClickOpen = (e) => {
    onOpenModal();
  };
  return (
      <>
        <Button onClick={handleClickOpen}>
          Open alert dialog
        </Button>
        
        <AlertDialog
            title="Modal Dialog Title"
            description="Praesent sapien massa, convallis a pellentesque nec."
            btnCloseContent="Close"
            open={ openModal }
            onCancel={ onCloseModal }
        />
      </>
  );
};
ReactDOM.render(<App />, document.querySelector('#app'));
```

Yes, it's really all you need to get started as you can see in this live and interactive demo:

[![Edit Button](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/)