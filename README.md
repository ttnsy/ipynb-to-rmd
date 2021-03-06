*Disclaimer:

The script is developed from RStudio Team's `convert_ipynb` [code](https://rmarkdown.rstudio.com/docs/reference/convert_ipynb.html). This simple app is developed for my personal purpose to ease the process of converting multiple `ipynb` into a tidy pdf.

## How to Use

### Step 1: Convert .ipynb to .Rmd file

1. Open the R project

2. In your R console, run `to_Rmd()` function from `R/converter.R` script. You can define your prefered input/output directory but the **default location** is in `/documents/` folder of this repository (input & output).
 
```r
source('R/converter.R')
to_Rmd()
```

### Step 2. Compile your pdf

1. Make sure all files (including images attached, related script, etc.) related to the notebook are included in `/documents`  (or, if you change the input/output directory, make sure it's in the same location of your Rmd).
2. Open `parent.Rmd`
3. Adjust YAML options & chunk titles
4. Knit it to pdf

Note: Please make sure the formatting of your notebook has followed the formatting rules below:


## Markdown Formatting

Please follow the formatting below:

1. Heading
  - `#`: Indicates the **Title** of the document. DO NOT use this heading for sectioning.
  - `##`, `###`, ...: Marks the section heading

![](img/heading.png)

2. Bullets
  - Please add breaks after paragraph and before bullet! Example:

![](img/bullets.png)

3. Others:
  - Do **NOT** use `%matplotlib inline`
  - Do **NOT** use space(` `) before and after `$` when creating latex equation:
  ```
  # WRONG:
  $ f(x) = x^2 $
  
  # CORRECT:
  $f(x) = x^2$
  ```
  

