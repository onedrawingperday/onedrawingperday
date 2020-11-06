+++
{{ $dir := split .File.Dir "/" -}}
{{- $value :=  index $dir 2 -}}
title = "{{ $value | title }}"
date = "{{ dateFormat "Monday, Jan 2, 2006, 15:04:05 EEST" .Date }}"
year = "{{ dateFormat "2006" .Date }}"
month = "{{ dateFormat "2006/01" .Date }}"
+++