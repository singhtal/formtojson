Lighest Form to JSON data plugin ⚡⚡
## Usage

<strong> Install the plugin </strong>

```Bash
npm i react-form2json
```

### Using plugin in react code

```javascript
import formtojson from "react-form2json";
```

#### Pass event as a parameter
formtojson takes submit event as a paramter, event is e in this case.

```javascript
    const data = formtojson(e);
    console.log(data);
```

#### React Example

```javascript
import React, { useState } from "react";
import formtojson from "react-form2json";
function Myform() {
  const [name, setName] = useState("Talvinder");
  const [age, setAge] = useState("20");
  const handleClick = (e) => {
    const data = formtojson(e);
    console.log(data);
  };
  const handleName = (e) => {
    setName(e.target.value);
  };
  const handleAge = (e) => {
    setAge(e.target.value);
  };
  return (
    <div>
      <form onSubmit={(e) => handleClick(e)}>
        <input
          name="name"
          type="text"
          value={name}
          onChange={(e) => handleName(e)}
        />
        <input
          name="age"
          type="text"
          value={age}
          onChange={(e) => handleAge(e)}
        />
        <button>Submit</button>
      </form>
    </div>
  );
}
export default Myform;

```

On Form Submit the output will be -

```bash
{"name":"Talvinder","age":"20"}
```

