# Introduction

This is the official repository for the documentation of 3PL Dynamics. It's really important to follow the guidelines.
If you have questions don't hesitate to contact one of the owners of the documentations.

## Guidelines

1. Don't spend much time on lay-out, this is handled by the pipeline.
2. Use # to mark an header
3. Use ## to mark an sub-header, ### sub-sub etc
4. Tip: Use a double space to get one enter
5. To create a link to a different file, you can use the following syntax: [Copy Item](CopyItem.md)
6. To include an file use the following syntax: [!INCLUDE[prod_short](includes/prod_short.md)]
7. Do not use spaces in your file-name, otherwise links don't work. Instead of a space use a dash, or an underscore.
8. For filenames don't use plural entity-names, eg CustomerItem instead of CustomerItems
9. The Table of Content (TOC) is managed by the toc.yml for the main page, each sub folder has is own toc.md
10. If you use Media (pictures etc) consider the size, please use *.png. and shrink the size via: <https://tinypng.com/>
11. Please be aware that every commit result in an update of <https://learn.boltrics.com> (after 10 minutes). Please Test before commit.
12. Please don't describe all the fields of a table, therefore use Tooltips in AL. Only use help if you have additional information.
13. Please add the ContextSensitiveHelpPage property to the list or a card page. *Example: (ContextSensitiveHelpPage = 'appWMS/CustomerItem');*

## Testing before commit

1. Please run the PowerShell script `RunCheck.ps1` -> You can run '5 = Documentation' via the Launch Script (RDP)
2. Make sure there are no error or warning messages and you have downloaded <https://aka.ms/dotnet/download>

> [!TIP]
> **Preview your documentation before publishing:**
> 1. Open Terminal in Visual Studio Code
> 2. Navigate to the Documentation folder: (Ctrl-P, search for docfx.json)
> 3. In the Terminal, run the command: `docfx --serve`
> 4. Open your browser and go to the URL shown (usually `http://localhost:8080`)
> 5. Review any of the warnings in the terminal
> 5. Review your changes in the test site. 
> 6. Press `Ctrl+C` in the terminal to stop the preview

## Sources

If you want to read more about MarkDown language please see the links below:

1. <https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/user-assistance>
2. <https://www.markdownguide.org/cheat-sheet/>
3. Be creative and get your examples from the already existing files
4. <https://www.deepl.com/nl/translator>
5. Read <https://www.markdownguide.org/basic-syntax/> for basic syntax documentation
