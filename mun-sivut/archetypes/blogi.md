+++
date = '{{ .Date }}'
draft = true
{{ $title := strings.SliceString .File.ContentBaseName 11 -}}
{{ $title = strings.Replace $title "-" " " -}}
{{ $title = strings.FirstUpper $title -}}
title = '{{ $title }}'
{{ $slug := strings.SliceString .File.ContentBaseName 11 -}}
{{ $slug = strings.ToLower $slug -}}
{{ $slug = strings.Replace $slug "ä" "a" -}}
{{ $slug = strings.Replace $slug "ö" "o" -}}
{{ $slug = strings.Replace $slug "å" "a" -}}
slug = '{{ $slug }}'
+++
