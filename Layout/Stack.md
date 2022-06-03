### Mui Stack

Stack component is used to manage layout in 1 Dimension. either along vertical or horizontal.

Continue with MUILayout

Flex direction column is the default Stack style.

```javascript
import React from "react";
import { Box, Stack, Divider } from "@mui/material";

const MuiLayout = () => {
  return (
    <Stack
      sx={{ border: "1px solid" }}
      direction="row"
      spacing={2}
      //divider={<Divider orientation="vertical" flexItems />}
    >
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
    </Stack>
  );
};

export default MuiLayout;
```
