```diff

╭━━━╮╱╱╱╱╱╭╮╱╭━━━╮╱╱╱╱╱╱╱╱╭╮╱╭━━━┳╮╱╱╱╱╱╱╱╱╱╱╱╭━━╮╱╱╱╱╱╱╱╱╭╮
┃╭━╮┃╱╱╱╱╱┃┃╱┃╭━╮┃╱╱╱╱╱╱╱╭╯╰╮┃╭━╮┃┃╱╱╱╱╱╱╱╱╱╱╱╰┫┣╯╱╱╱╱╱╱╱╭╯╰╮
┃┃╱╰╋━━┳━━┫┃╱┃╰━╯┣━━┳━━┳━┻╮╭╯┃╰━╯┃╰━┳━━┳━╮╭━━╮╱┃┃╭━╮╭━━┳╮┣╮╭╯
┃┃╱╭┫╭╮┃╭╮┃┃╱┃╭╮╭┫┃━┫╭╮┃╭━┫┃╱┃╭━━┫╭╮┃╭╮┃╭╮┫┃━┫╱┃┃┃╭╮┫╭╮┃┃┃┃┃
┃╰━╯┃╰╯┃╰╯┃╰╮┃┃┃╰┫┃━┫╭╮┃╰━┫╰╮┃┃╱╱┃┃┃┃╰╯┃┃┃┃┃━┫╭┫┣┫┃┃┃╰╯┃╰╯┃╰╮
╰━━━┻━━┻━━┻━╯╰╯╰━┻━━┻╯╰┻━━┻━╯╰╯╱╱╰╯╰┻━━┻╯╰┻━━╯╰━━┻╯╰┫╭━┻━━┻━╯
╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱┃┃
╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╱╰╯
```
---

Cool React Phone Input is a comprehensive React component designed for handling phone inputs. It provides an easy integration for any React application and offers extensive customization options.

## Original Source

This is a fork of https://github.com/bl00mber/react-phone-input-2.

## Added Features

- **File Type Filtering**: Restrict uploads to specific file types.
- **File Size Validation**: Limit the size of the uploads.
- **Customizable Styles**: Adjust the look and feel according to your application design.
- **Persistent State Management**: Maintain image state during component re-renders.

## Installation

You can install the package using npm or yarn:

npm:

```bash
npm install cool-react-phone-input
```

yarn:

```bash
yarn add cool-react-phone-input
```

## Usage

Below is a simple example to demonstrate how to integrate the Cool React Phone Input control into your project:

```javascript
import React, { useState } from 'react';
import CoolImageUploader from 'cool-react-image-upload';

function App() {
  const [imageData, setImageData] = useState('');

  const handleOnFileAdded = (imgObj) => {
    setImageData(imgObj.dataUrl);
  };

  const handleOnFileRemoved = (imgObj) => {
    setImageData('');
  };

  const handleOnError = (errMsg) => {
    console.error("An error occurred: " + errMsg);
  }

  return (
    <div>
      <CoolImageUploader
                onFileAdded={(imgObj) => handleOnFileAdded(imgObj)}
                onFileRemoved={(imgObj) => handleOnFileRemoved(imgObj)}
                acceptedFileTypes="image/jpeg,image/png"
                maxFileSize={1000000}
                style={{
                    height: '150px',
                    width: '150px',
                    color: '#ffb200',
                    backgroundColor: 'white',
                    border: '3px solid #cccccc',
                    borderRadius: '50%'
                }}        
                btnWrapperStyle={{
                    top: '15px',
                    right: '30px'
                }}
                imageData={imageData}  
                onError={(errMsg) => handleOnError(errMsg)}       
      /> 
    </div>
  );
}

export default App;
```

## Props

- **onFileAdded (Function)**: Callback fired when a file is added. Ensure you update the imageData state within the React App that is using the package. (REQUIRED)
- **onFileRemoved (Function)**: Callback fired when a file is removed. Ensure you update the imageData state within the React App that is using the package. (REQUIRED)
- **imageData (string)**: The data URL of the image. This is managed in the parent component's state. (REQUIRED)
- **acceptedFileTypes (string)**: MIME types allowed for the upload. (OPTIONAL)
- **maxFileSize (number)**: Maximum file size allowed in bytes. (OPTIONAL)
- **style (CSSProperties)**: Styles for the uploader container. (OPTIONAL)
- **btnWrapperStyle (CSSProperties)**: Styles for the delete button container.(OPTIONAL)
- **onError (Function)**: Callback fired when validation fails.(OPTIONAL)


## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

This project is licensed under the MIT License - see [MIT License](https://opensource.org/licenses/MIT) for details.

<div align="center">

### 𝚂𝚑𝚘𝚠 𝚜𝚘𝚖𝚎 ❤️ 𝚋𝚢 𝚜𝚝𝚊𝚛𝚛𝚒𝚗𝚐 this repository!

</div>
