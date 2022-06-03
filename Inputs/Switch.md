### Mui Switch

Switches toggle the state of a single setting on or off and are the preferred way to adjust settings on a mobile.

```javascript
import React from "react";
import { Box, FormControlLabel, Switch } from "@mui/material";

const MuiSwitch = () => {
  return (
    <Box>
      <FormControlLabel label="Dark mode" control={<Switch />} />
    </Box>
  );
};

export default MuiSwitch;
```
---

Tracking the state of checked.

```javascript
import React, { useState } from "react";
import { Box, FormControlLabel, Switch } from "@mui/material";

const MuiSwitch = () => {
  const [checked, setChecked] = useState(false);
  console.log({ checked });

  const handleChange = (event: React.ChangeEvent<HTMLInputElement>) => {
    setChecked(event.target.checked);
  };

  return (
    <Box>
      <FormControlLabel
        label="Dark mode"
        control={
          <Switch
            checked={checked}
            onChange={handleChange}
            color="success"
            size="small"
          />
        }
      />
    </Box>
  );
};

export default MuiSwitch;
```
