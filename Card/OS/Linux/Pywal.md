up:: [[Linux]]

# Polybar
source:: [[Polybar]]
url:: [Customization · dylanaraps/pywal Wiki · GitHub](https://github.com/dylanaraps/pywal/wiki/Customization#polybar)


```json
[colors]
background = ${xrdb:color0:#222}
foreground = ${xrdb:color7:#222}
foreground-alt = ${xrdb:color7:#222}
primary = ${xrdb:color1:#222}
secondary = ${xrdb:color2:#222}
alert = ${xrdb:color3:#222}

[bar/bar]
; ...
background = ${colors.background}
foreground = ${colors.foreground}

; ...
```

:heavy