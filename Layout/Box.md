### Mui Box

Box component serves as a wrapper component for the most of our css utility needs.

Box component accepts a prop called sx which can be used to define a custom style that has access to teh theme.

As a css utility component, box component supports material ui system properties. which means we can use lot of the css properties as a prop directly on a component.

```javascript
import React from "react";
import { Box } from "@mui/material";

const MuiLayout = () => {
  return (
    <>
      <Box
        //component="span"
        sx={{
          backgroundColor: "primary.main",
          color: "white",
          height: "100px",
          width: "100px",
          padding: "16px",
          "&:hover": {
            backgroundColor: "primary.light",
          },
        }}
      >
        MuiLayout
      </Box>
      <Box
        display="flex"
        height="100px"
        width="100px"
        bgcolor="success.light"
        p={2}
      ></Box>
    </>
  );
};

export default MuiLayout;
```
