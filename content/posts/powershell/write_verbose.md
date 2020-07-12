---
title: "How to use Write-Verbose in PowerShell functions"
date: 2020-04-14T20:21:48+06:00
hero: /images/headshot.jpg
id: docker-multi-stage
author:
    name: Chris Blackden
    image: /images/headshot.jpg
categories:
    - powershell
---

# How to use Write-Verbose in PowerShell functions

## Summary
Have you ever been running a new PowerShell cmdlet, but you wish you could see how it works under the hood? Has some function you were writing been just slightly off, and you need a way to determine what it's doing without going line-by-line trying to see where the code is broken? Using a debugger can help, but in situations where you prefer a little extra logging instead, you can use the `-Verbose` parameter.

## Setting the scene
Here's an example

```
# PowerShell

function Add-Numbers {
  param (
    [int]$num1,
    [int]$num2
  )

  $answer = $num1 + $num2
  return $answer
}
```

