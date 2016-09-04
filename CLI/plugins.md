## `plugins`
Print registered plugin summaries

### Optional arguments
| argument | description |
| --- | --- |
| `--table-type {plain,porcelain,github,single,double}` | Select output table style |
| `--porcelain` | Make the output parseable. Similar to using `--table-type porcelain` |
| `--group GROUP` | Show plugins belonging to this group |
| `--phase PHASE` | Show plugins that act on this phase |
| `--builtins` | Show just builtin plugins |

### Examples
```bash
#shows all builtin plugins
flexget plugins --builtins
```

### Related articles
* [CUI / Command line interface overview](/CLI)