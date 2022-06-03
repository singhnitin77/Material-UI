### MUI-TextField

Basic Text Field

```javascript
import { Stack, TextField } from "@mui/material";
export const MuiTextField = () => {
  return (
    <Stack spacing={4}>
      <Stack direction="row" spacing={2}>
        <TextField label="Name" />I
      </Stack>
    </Stack>
  );
};
```

Outline is the default variant

```javascript
import { Stack, TextField } from "@mui/material";
export const MuiTextField = () => {
  return (
    <Stack spacing={4}>
      <Stack direction="row" spacing={2}>
        <TextField label="Outlined" variant="outlined" />
        <TextField label="Filled" variant="filled" />
        <TextField label="Standard" variant="standard" />
      </Stack>
    </Stack>
  );
};
```

Adornments acts like prefixes and suffixes, input adornment does not have to be just text we can even use icons.

```javascript
import { useState } from "react";
import { Stack, TextField, InputAdornment } from "@mui/material";

export const MuiTextField = () => {
  const [value, setValue] = useState("");

  const handleChange = (event: React.ChangeEvent<HTMLInputElement>) => {
    setValue(event.target.value);
  };
  return (
    <Stack spacing={4}>
      <Stack spacing={2} direction="row">
        <TextField label="Outlined" variant="outlined" />
        <TextField label="Filled" variant="filled" />
        <TextField label="Standard" variant="standard" />
      </Stack>
      <Stack spacing={2} direction="row">
        <TextField label="Small secondary" size="small" color="secondary" />
      </Stack>
      <Stack spacing={2} direction="row">
        <TextField
          label="Form Input"
          required
          value={value}
          onChange={(e) => setValue(e.target.value)}
          error={!value}
          helperText={
            !value ? "Required" : "Do not share your password with anyone"
          }
        />
        <TextField
          label="Form Input"
          required
          helperText="Do not share your password with anyone"
          type="password"
        />
      </Stack>
      <Stack spacing={2} direction="row">
        <TextField
          label="Amount"
          InputProps={{
            startAdornment: <InputAdornment position="start">$</InputAdornment>,
          }}
        />
        <TextField
          label="Weight"
          InputProps={{
            endAdornment: <InputAdornment position="end">kg</InputAdornment>,
          }}
        />
      </Stack>
    </Stack>
  );
};
```









