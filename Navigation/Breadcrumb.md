### Breadcrumbs

Breadcrumbs Component.

Breadcrumbs is a type of secondary navigation scheme that reveals the users location in a website.

```javascript
import React from "react";
import { Box, Breadcrumbs, Link, Typography } from "@mui/material";

const MuiBreadcrumbs = () => {
  return (
    <Box m={2}>
      <Breadcrumbs aria-label="breadcrumb">
        <Link underline="hover" href="#">
          Home
        </Link>
        <Link underline="hover" href="#">
          Catalog
        </Link>
        <Link underline="hover" href="#">
          Accessories
        </Link>
        <Typography color="text.pri">Shoes</Typography>
      </Breadcrumbs>
    </Box>
  );
};

export default MuiBreadcrumbs;
```

---

```javascript
import React from "react";
import { Box, Breadcrumbs, Link, Typography } from "@mui/material";
import NavigationNextIcon from "@mui/icons-material/NavigateNext";

const MuiBreadcrumbs = () => {
  return (
    <Box m={2}>
      <Breadcrumbs
        aria-label="breadcrumb"
        separator={<NavigationNextIcon fontSize="small" />}
        maxItems={3}
        itemsAfterCollapse={2}
        //itemsBeforeCollapse={2}
      >
        <Link underline="hover" href="#">
          Home
        </Link>
        <Link underline="hover" href="#">
          Catalog
        </Link>
        <Link underline="hover" href="#">
          Accessories
        </Link>
        <Typography color="text.pri">Shoes</Typography>
      </Breadcrumbs>
    </Box>
  );
};

export default MuiBreadcrumbs;
```
