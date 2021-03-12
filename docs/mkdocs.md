# Mkdocs Explanation

Fast static site generator

## Installation

1. Install with pip:

    ```
    pip install mkdocs
    ```

2. Create file mkdocs.yml in your project:

    ```
    site_name: <your_site_name>
    ```

3. Try to see your site: 

    run with -v to present errors if occure
    ```
    mkdocs -v serve
    ```
    Run: http://127.0.0.1:8000
&nbsp;

## Plugins 
&nbsp;
- search plugin should call once. It is a default plugin and if you declare plugins you should declare search.

### Create Table
&nbsp;

In your MarkDown file, create a table as:

| First Column  | Second Column  | Third Column  |
|---------------|:--------------:|---------------|
| Ex1           | Ex2            | Ex3           |



- In order to center the content, use :---: as shown in Second Column

Install the plugin:
```
pip install mkdocs-bootstrap-tables-plugin
```

Add the plugin to mkdocs.yml file:
```
plugins:
    - search
    - bootstrap-tables
```
&nbsp;
### Create Mermaid Graphs
&nbsp;

In your MarkDown file, create an example graph:

```mermaid

graph LR
    Hello --> MermaidPlugin
```

Install the plugin:
```
pip install mkdocs-mermaid2-plugin
```

Enter to https://www.cdnpkg.com/mermaid/file/mermaid.min.js/ and download the file mermaid.min.js (version 8.6.3)

Save the file on project/docs folder.

- Add the plugin to mkdocs.yml file:
```
plugins:
    - search
    - mermaid2
```

- Add the Mermaid library declaration to mkdocs.yml file:
```
extra_javascript:
    - mermaid.min.js
```

- Download from vscode MarketPlace the `Markdown Preview Mermaid Support` in order to see mermaid graphs on markdown file.


### Code Reference

Install the plugin:
```
pip install mkdocstrings
```

- Add the plugin to mkdocs.yml file:
```
plugins:
    - search
    - mkdocstrings
```

- Add a reference in your MarkDown file:
```
::: <folder>.<file_name>.<class/function>
```
For example:

::: src.main.func

