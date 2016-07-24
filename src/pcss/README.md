# PCSS

## PureCSS

PureCSS Task for generate custom grid.

Features:
- ```visible/hidden``` classes
- ```wrapper``` class for main wrapper
- ```offset``` classes
- media variables | *example:* ```--screen-xs```

Config ```tasks.json```

    {
      "purecss": {
        "prefix": "grid",
        "columnHasPrefix": true,
        "columns": 12,
        "gutterWidth" : "0.9375rem",
        "columnPrefix": "col",
        "wrapperBreakpoints": ["md", "lg"],
        "breakpoints": {
          "xs": "30em",
          "sm": "48em",
          "md": "62em",
          "lg": "75em"
        },
        "files": {
          "dest": "./generated/pcss/",
          "src": ["base", "grids-core"]
        }
      }
    }

#### prefix

Type: ```String```

Sets prefix for all generated classes.

#### columnHasPrefix

Type: ```Boolean```

Indicates whether the column get a prefix.

#### columns

Type: ```Number```

Sets the number of columns.

#### gutterWidth *(optional)*

Type: ```String```

Sets the width of grid-gutter. Example: 0.9375rem

*Required one Prefix.*

#### columnPrefix

Type: ```String```

Sets the prefix of columns.

#### wrapperBreakpoints

Type: ```Array```

Sets the breakpoints for the wrapper.

#### breakpoints

Type: ```Object```

Sets the breakpoints that are required to generate the grid classes and media querys vars.

    {
      "xs": "30em",
      "sm": "48em",
      "md": "62em",
      "lg": "75em"
    }

#### files

Type: ```Object```

Sets PureCSS files and destination path for generated files.

    {
      "dest": "./generated/pcss/",
      "src": ["base", "grids-core"]
    }


##### dest

Type: ```String```

Destination for generated files.

##### src

Type: ```Array```


Gives the files to prefix.
Files comes from ```purecss``` *node_modules*.
