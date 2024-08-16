## latexmk options

Located at `XDG_CONFIG_HOME/latexmk/latexmkrc`, example:
```
$pdflatex = "pdflatex -file-line-error -halt-on-error -interaction=nonstopmode -synctex=1";
```

## Default Mappings

Many of the mappings utilize the maplocalleader.
The right-hand sides are provided as plug mappings.
For any given <plug> map, the default mapping will only be created if it does not already exist.
This means that if a user defines a custom mapping, e.g. with
```
  nmap <space>li <plug>(vimtex-info)
```

then the corresponding default left-hand side will not be mapped.

If one prefers, one may disable all default mappings through the option
`g:vimtex_mappings_enabled`.
One must then define custom mappings for all desired features through the
listed RHS `<plug>` maps or by mapping the available commands.

In the below list of mappings, LHS is the default mapping, RHS is the
corresponding <plug> maps, and MODE indicates in which vim mode the mappings
are valid.

| LHS   | RHS   | MODE  |
| ----- | ----- | ----- |
| `<localleader>li` 	| `<plug>(vimtex-info)` 	                | n 	|
| `<localleader>lI` 	| `<plug>(vimtex-info-full)` 	            | n 	|
| `<localleader>lt` 	| `<plug>(vimtex-toc-open)` 	            | n 	|
| `<localleader>lT` 	| `<plug>(vimtex-toc-toggle)` 	            | n 	|
| `<localleader>lv` 	| `<plug>(vimtex-view)` 	                | n 	|
| `<localleader>lr` 	| `<plug>(vimtex-reverse-search)` 	        | n 	|
| `<localleader>ll` 	| `<plug>(vimtex-compile)` 	                | n 	|
| `<localleader>lk` 	| `<plug>(vimtex-stop)` 	                | n 	|
| `<localleader>lK` 	| `<plug>(vimtex-stop-all)` 	            | n 	|
| `<localleader>le` 	| `<plug>(vimtex-errors)` 	                | n 	|
| `<localleader>lo` 	| `<plug>(vimtex-compile-output)` 	        | n 	|
| `<localleader>lg` 	| `<plug>(vimtex-status)` 	                | n 	|
| `<localleader>lG` 	| `<plug>(vimtex-status-all)` 	            | n 	|
| `<localleader>lc` 	| `<plug>(vimtex-clean)` 	                | n 	|
| `<localleader>lC` 	| `<plug>(vimtex-clean-full)` 	            | n 	|
| `<localleader>lm` 	| `<plug>(vimtex-imaps-list)` 	            | n 	|
| `<localleader>lx` 	| `<plug>(vimtex-reload)` 	                | n 	|
| `<localleader>ls` 	| `<plug>(vimtex-toggle-main)` 	            | n 	|
| `dse` 	            | `<plug>(vimtex-env-delete)` 	            | n 	|
| `dsc` 	            | `<plug>(vimtex-cmd-delete)` 	            | n 	|
| `ds$` 	            | `<plug>(vimtex-env-delete-math)` 	        | n 	|
| `cse` 	            | `<plug>(vimtex-env-change)` 	            | n 	|
| `csc` 	            | `<plug>(vimtex-cmd-change)` 	            | n 	|
| `cs$` 	            | `<plug>(vimtex-cmd-change-math)` 	        | n 	|
| `tse` 	            | `<plug>(vimtex-env-toggle-star)` 	        | n 	|
| `tsd` 	            | `<plug>(vimtex-delim-toggle-modifier)` 	| nx 	|
| `<F7>` 	            | `<plug>(vimtex-cmd-create)` 	            | ni 	|
| `]]` 	                | `<plug>(vimtex-delim-close)` 	            | i 	|
| `ac` 	                | `<plug>(vimtex-ac)` 	                    | nxo 	|
| `ic` 	                | `<plug>(vimtex-ic)` 	                    | nxo 	|
| `ad` 	                | `<plug>(vimtex-ad)` 	                    | nxo 	|
| `id` 	                | `<plug>(vimtex-id)` 	                    | nxo 	|
| `ae` 	                | `<plug>(vimtex-ae)` 	                    | nxo 	|
| `ie` 	                | `<plug>(vimtex-ie)` 	                    | nxo 	|
| `a$` 	                | `<plug>(vimtex-a$)` 	                    | nxo 	|
| `i$` 	                | `<plug>(vimtex-i$)` 	                    | nxo 	|
| `%` 	                | `<plug>(vimtex-%)` 	                    | nxo 	|
| `]]` 	                | `<plug>(vimtex-]])` 	                    | nxo 	|
| `][` 	                | `<plug>(vimtex-][)` 	                    | nxo 	|
| `[]` 	                | `<plug>(vimtex-[])` 	                    | nxo 	|
| `[[` 	                | `<plug>(vimtex-[[)` 	                    | nxo 	|
