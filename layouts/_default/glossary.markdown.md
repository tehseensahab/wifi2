# {{ .Title }}

> {{ .Description }}

- URL: {{ .Permalink }}
- Publisher: {{ site.Title }} ({{ site.BaseURL }})
{{ range site.Data.glossary }}
## {{ .section }}
{{ range .terms }}
**{{ .term }}**: {{ replaceRE `\]\(/` (printf "](%s/" (strings.TrimSuffix "/" site.BaseURL)) .def }} ({{ $.Permalink }}#{{ printf "term-%s" (replace .term "." "-" | anchorize) }})
{{ end }}
{{- end }}
