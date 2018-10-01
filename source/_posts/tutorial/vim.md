---
title: vim cheatsheet
date: 2018-08-03 09:00:00
comments: true
tags:
     - linux
categories: 
    - tutorial
---
personal memo table of vim shortkey.  
command                   | meaning             
------------              | -------------
```u```               | Ctr + Z  undo       
```.```               | repeat    
```i```               | insert     
```k j h l```               | UP DOWN LEFT RIGHT                
```w b```               |  next previous word
```0 $```   | head tail of setence                
```{ }```   | next previous paragrah                
```gg G```     | first last line of doc     
```yy y$ yw```     | copy the line, copy current to end of the line, copy current to end of the word        
```dd o```     | delete the line, open new line        
```p```     | paste
``` /keyword n N```     | find keyword next previous


Additionally.
command                   | meaning             
------------              | -------------
```UP DOWN```               | history command  
```:o file```               | open another file      
```saveas: file```               | save as file     
```%s/old/new/g[c]```               | replace keyword without/ with confirm   