# LaTeX environment for source code

> Listings with sane defaults

## Usage

## Features

### Autogobble
Automatically removes indentation (looks at first line of code to determine how much whitespace to gobble).

```LaTeX
    \begin{code}{python}
        def f():
            pass
    \end{code}
```

If you want to override the amount of whitespace to gobble (i.e. when the first line has more whitespace than others or when you want to preserve some whitespace) then you can do this:

```latex
    \begin{code}[gobble=4]{python}
        def f():
            pass
    \end{code}
```

### Embedded laTeX
You can embed laTeX code inside the code:

```latex
\begin{code}{python}
  def f()
      pass     // §O(1)§
\end{code}
```

The character for escaping into laTeX was chosen as `§` as Apple keyboards have a dedicated key for this and it isn't used for anything else. I appreciate that for non-osx users this may be a bit annoying. You can override it like so:

```latex
\begin{code}[escapechar=?]{python}
    def f():
        pass
\end{code}
```

### Minor tweaks
 - Tabs are displayed as 4 spaces rather than 8
 - spaces aren't underlined
