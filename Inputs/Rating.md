### MUI Rating

```javascript
import React from "react";
import { Stack, Rating } from "@mui/material";

const MuiRating = () => {
  return (
    <Stack spacing={2}>
      <Rating />
    </Stack>
  );
};

export default MuiRating;
```
---

```javascript
import React, { useState } from "react";
import { Stack, Rating } from "@mui/material";

const MuiRating = () => {
  const [value, setValue] = useState<number | null>(null);
  console.log({ value });

  const handleChange = (
    event: React.ChangeEvent<{}>,
    newValue: number | null
  ) => {
    setValue(newValue);
  };

  return (
    <Stack spacing={2}>
      <Rating value={value} onChange={handleChange} />
    </Stack>
  );
};

export default MuiRating;
```
---

Props

```javascript
import React, { useState } from "react";
import { Stack, Rating } from "@mui/material";
import FavoriteIcon from "@mui/icons-material/Favorite";
import FavoriteBorderIcon from "@mui/icons-material/FavoriteBorder";

const MuiRating = () => {
  const [value, setValue] = useState<number | null>(null);
  console.log({ value });

  const handleChange = (
    event: React.ChangeEvent<{}>,
    newValue: number | null
  ) => {
    setValue(newValue);
  };

  return (
    <Stack spacing={2}>
      <Rating
        value={value}
        onChange={handleChange}
        precision={0.5}
        size="large"
        icon={<FavoriteIcon fontSize="inherit" />}
        emptyIcon={<FavoriteBorderIcon fontSize="inherit" />}
        //readOnly
        highlightSelectedOnly
      />
    </Stack>
  );
};

export default MuiRating;
```


