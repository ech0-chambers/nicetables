# `nicetables`

`nicetables` is a $\LaTeX{}$ package which provides a simple but flexible interface for stylising tables in $\LaTeX{}$. It relies on the `xcolor`, `longtable`, and `environ` packages, and uses LaTeX3 syntax.

## Examples

See the documentation for a full list of options and examples. Some examples are shown below.

## Example Styling

```latex
\begin{nicetable}[
    array stretch       = 1.5,
    header cell style   = \color{BackgroundColour}\scshape\bfseries,
    header row color    = Accent4,
    row colors          = {Surface5, BackgroundColour},
    every cell style    = \color{ForegroundColour},
    separator color     = ForegroundColour,
    row separator       = false,
    cell style          = {, \num, \ensuremath},
]{|llc|}
    Planet  & Mass (\unit{\kilo\gram})  & Number of Moons   \\
    Mercury & 3.30e23                   & 0                 \\
    Venus   & 4.87e24                   & 0                 \\
    Earth   & 5.97e24                   & 1                 \\
    Mars    & 6.42e23                   & 2                 \\
    Jupiter & 1.90e27                   & 92                \\
    Saturn  & 5.68e26                   & 83                \\
    Uranus  & 8.68e25                   & 27                \\
    Neptune & 1.02e26                   & 14                \\
    Pluto   & 1.31e22                   & 5 
\end{nicetable}
```

[![Styled table](/examples/example-1.png)](/examples/example-1.png)

### Default (no additional styling)

```latex
\begin{nicetable}{|l|c|l|}
Name           & Age & City           \\
John Smith     & 28  & New York       \\
Alice Johnson  & 35  & Los Angeles    \\
Bob Anderson   & 22  & Chicago        \\
Eva Williams   & 30  & San Francisco  \\
David Brown    & 25  & Miami  
\end{nicetable}
```

[![Default table](/examples/default-1.png)](/examples/default-1.png)

### Adding Some Colour

*The colours used here are defined by the `qoplots` Python package, which can be found here: [https://github.com/pbrookeschambers/qoplots](https://github.com/pbrookeschambers/qoplots)*


```latex
\begin{nicetable}[
    header row color = Blue,
    header row style = {\color{BackgroundColour}},
    row colors = {Surface5, BackgroundColour},
    separator color = ForegroundColour,
    cell style = \color{ForegroundColour}
]{|l|c|l|}
Name           & Age & City           \\
John Smith     & 28  & New York       \\
Alice Johnson  & 35  & Los Angeles    \\
Bob Anderson   & 22  & Chicago        \\
Eva Williams   & 30  & San Francisco  \\
David Brown    & 25  & Miami          
\end{nicetable}
```

[![Coloured table](/examples/with_colour-1.png)](/examples/with_colour-1.png)

### Easy Spacing Control

```latex
\begin{nicetable}[
    array stretch = 2,
    column separation = 1cm
]{|l|c|l|}
Name           & Age & City           \\
John Smith     & 28  & New York       \\
Alice Johnson  & 35  & Los Angeles    \\
Bob Anderson   & 22  & Chicago        \\
Eva Williams   & 30  & San Francisco  \\
David Brown    & 25  & Miami          
\end{nicetable}
```

[![Spaced table](/examples/spacing_control-1.png)](/examples/spacing_control-1.png)

### Column Formatting

```latex
\begin{nicetable}[
    header row style = {\scshape},
    cell style = {\color{red!50!black}, \ensuremath, \texttt}
]{|l|c|l|}
Name           & Age & City           \\
John Smith     & 28  & New York       \\
Alice Johnson  & 35  & Los Angeles    \\
Bob Anderson   & 22  & Chicago        \\
Eva Williams   & 30  & San Francisco  \\
David Brown    & 25  & Miami          
\end{nicetable}
```

[![Formatted table](/examples/column_formatting-1.png)](/examples/column_formatting-1.png)

### Removing Separators

```latex
\begin{nicetable}[
    row separator = false,
]{|lcl|}
Name           & Age & City           \\
John Smith     & 28  & New York       \\
Alice Johnson  & 35  & Los Angeles    \\
Bob Anderson   & 22  & Chicago        \\
Eva Williams   & 30  & San Francisco  \\
David Brown    & 25  & Miami          
\end{nicetable}
```

[![No separators table](/examples/without_separators-1.png)](/examples/without_separators-1.png)