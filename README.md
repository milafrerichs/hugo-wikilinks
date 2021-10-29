# hugo-wikilinks
A module for Hugo to include wikilinks style to your content


## Usage

### content-wikilinks
where you want to include wikilinks in content. for example in your `single.html` layout file

```
{{ partial "content-wikilinks" . }}
```

it will take the `.Content` and search for wikilinks `[[...]]` and then will use `relref` to find the page and add a link. 


### backlinks
Backlinks is a function partial. it will return a list of backlinks to a specific page. 

```
{{ $backlinks := partial "funcs/backlinks.html" . }}
{{ range $backlinks }}
{{ end }}
```
