---
title: Expense Sheet Combiner
date: 2024-12-21
author:  Sky Quan
description: Description of Expense Sheet Combiner project
tags:
  - project
---

This post details my work on my expense sheet combiner project. The code can be found on my github here: 
* https://github.com/Ctrl-Sky/expense-sheet-combiner.git

# Project Overview
This is a personal expense tracker automation tool. This is something I created to help keep track of my expenses across multiple different cards. It takes account activity of each card as a csv format, standardizes all of them to fit my specific format, and then combines them all into one master excel file. Filtering each purchase into a new sheet respective to the month the expense was made in.

# Tools Used
* Python
* Shell 
* PowerShell
* Excel
* Pandas
* NumPy

# The Purpose for Creation
I'm really big on managing my money and after getting my second credit card, I found it much harder to keep track of everything since I had to jump from one banking page to another. What I wanted was a centralized place to view all my finances month by month. So, I created this python script that combines them all into one place and splits them depending on the month.