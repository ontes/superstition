# The Most Dangerous Superstition
Archive of the legendary book The Most Dangerous Superstition by Larken Rose and home of a Czech translation made using DeepL with a tonne of manual corrections.

`superstition-orig.md` - original text in Markdown format  
`superstition.md` - improved text in Markdown format (some excessive quotes removed)  
`latex/superstition.tex` - improved text in LaTex format  
`superstition-cz.md` - Czech translation in Markdown format  
`latex/superstition-cz.tex` - Czech translation in LaTex format  

Pull requests with fixes and improvements are welcome.

## Generating LaTex from Markdown

For the English version:
```
sed -e 's/"\([^"]*\)"/\\enquote{\1}/g' -e 's/\*\*\([^*]*\)\*\*/\\textbf{\1}/g' -e 's/\*\([^*]*\)\*/\\emph{\1}/g' -e 's/^# Part.*: \(.*\)/\\chapter{\1}/' -e 's/^## \(.*\)/\\section{\1}/' -e 's/ \- /---/g' -e 's/\- /-- /g' -e 's/\$/\\$/g' -e 's/%/\\%/g' superstition.md
```

For the Czech version:
```
sed -e 's/"\([^"]*\)"/\\enquote{\1}/g' -e 's/\*\*\([^*]*\)\*\*/\\textbf{\1}/g' -e 's/\*\([^*]*\)\*/\\emph{\1}/g' -e 's/^# Část.*: \(.*\)/\\chapter{\1}/' -e 's/^## \(.*\)/\\section{\1}/' -e 's/\- /-- /g' -e 's/\$/\\$/g' -e 's/%/\\%/g' superstition-cz.md
```

Only works for the main body, the beginning of the file was written manually.
