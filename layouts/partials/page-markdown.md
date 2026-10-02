{{- /* Clean Markdown version of a page, used by index.md and llms-full.txt. Context: a page. */ -}}
{{- $p := . -}}
{{- $isArticle := in (slice "reviews" "news" "guides" "deals") $p.Section -}}
{{- $t := partial "primary-topic.html" $p -}}
{{- $a := partial "author.html" $p -}}
{{- $base := strings.TrimSuffix "/" site.BaseURL -}}
# {{ $p.Title }}

{{ with $p.Description }}> {{ . }}
{{ end }}
- URL: {{ $p.Permalink }}
{{- if $isArticle }}
- Type: {{ $p.Section | singularize | title }}
- Topic: {{ $t.name }}
{{- with $a.name }}
- Author: {{ . }}
{{- end }}
- Published: {{ $p.Date.Format "2006-01-02" }}
- Last updated: {{ $p.Lastmod.Format "2006-01-02" }}
{{- with $p.Params.testedOn }}
- Tested: {{ dateFormat "2006-01-02" . }}
{{- end }}
{{- with $p.Params.score }}
- Score: {{ printf "%.1f" . }}/10
{{- end }}
{{- with $p.Params.bestFor }}
- Best for: {{ . }}
{{- end }}
{{- with $p.Params.price }}
- Price: ${{ lang.FormatNumber 0 . }} (US street price on the test date)
{{- end }}
{{- with $p.Params.dealPrice }}
- Deal price: ${{ lang.FormatNumber 0 . }}{{ with $p.Params.retailer }} at {{ . }}{{ end }}{{ with $p.Params.priceChecked }} (checked {{ dateFormat "2006-01-02" . }}){{ end }}
{{- end }}
{{- else }}{{ with $p.Params.updated }}
- Last updated: {{ dateFormat "2006-01-02" . }}
{{- end }}{{ end }}
- Publisher: {{ site.Title }} ({{ site.BaseURL }})
{{ with $p.Params.summary }}
## Short answer

{{ . }}
{{ end }}
{{- with $p.Params.takeaways }}
## Key takeaways

{{ range . }}- {{ . }}
{{ end }}
{{- end }}
{{- with $p.Params.specs }}
## Key specs

| Spec | Value |
|---|---|
{{ range . }}| {{ .k }} | {{ .v }} |
{{ end }}
{{- end }}
{{- if or $p.Params.pros $p.Params.cons }}
## Pros and cons

{{ range $p.Params.pros }}- Pro: {{ . }}
{{ end }}{{ range $p.Params.cons }}- Con: {{ . }}
{{ end }}
{{- end }}
{{- $body := $p.RenderShortcodes -}}
{{- $body = replaceRE `\]\(/` (printf "](%s/" $base) $body }}
{{- if $isArticle }}
---
{{ end }}
{{ $body }}
{{ with $p.Params.faq }}
## Frequently asked questions
{{ range . }}
### {{ .q }}

{{ .a }}
{{ end }}
{{- end }}
{{- with $p.Params.sources }}
## Sources

{{ range . }}- {{ .title }}{{ with .publisher }}, {{ . }}{{ end }}{{ with .url }}: {{ . }}{{ end }}
{{ end }}
{{- end }}
