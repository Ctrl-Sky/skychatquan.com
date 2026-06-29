---
title: Automatic Photo Transfer
date: 2025-08-17
author: Sky Quan
description: Description for Automatic Photo Transfer Project
tags:
  - project
---

This post details my work on my automated groq job application project. The code can be found on my github here: 
* https://github.com/Ctrl-Sky/automatic-photo-transfer-2.0.git

# Project Overview
This project is an automated standardization pipeline for transfering photos from one folder to another, keeping track of which photos have already been uploaded and organizing them based on date.

This project automates the process of moving photos from my SD card/Iphone into my external hard drive and organizing them. To run the script, plug in the destination and source and it will copy every photo from the source directory into the destination directory, organizing each into folders based on the date they were taken. Out of all the photos, it will note down the photo that was taken the most recently and write that date into the csv file (the migration table). This will act as a save point. Now if the script is run again, it will pull that date from the save point in the migration table and only upload the photos that were taken after said date.

The current supported file types are:
* JPEG
* JPG
* PNG
* HEIC
* MP4
* MOV
Any unknown files encountered are transferred into an a directory for manual sorting.

# Tools Used
* Python
* Shell 
* PIL (Python Imaging Library)
* Excel

# The Purpose for Creation
For me, I really enjoy taking photos. Mainly, I use my phone camera and my own DSLR camera for taking photos. However, I never really had a central area to save all my photos until I bought my first external hard drive. There, I would save all my photos from my phone and my camera, however I would have to organize them all by myself manually. This was a very tedious process so, I began thinking of ways of automating it. Organizing and copying the photos on to the hard drive was simple, but I was struggling to think of a way to allow me to keep the photos on the source everytime and have my script remember which photos have already been transfered. Now, this was during the time I worked as a DevOps Engineer Intern at OTPP. During that exact time, I was also working on a ticket to fix an issue with the logs Flyway was producing. Because of that ticket, I ended up learning the ins and outs of Flyway and discovering its Migration Table. To simplifiy it, Flyway uses a migration table as source control for databases, tracking every SQL query made to a database and recording it to the table. For every SQL query made, Flyway would look back on the migration table and if a similar SQL query was already made and the new one would have no new effects, it would deny that query. That idea of referencing back to the table made a lot of sense to me as a way to remember which photos have already been moved. This would result in the creation of my migration table that tracks the date of the newest added photo and only adding the ones past that date, allowing me to keep the photos on my camera/phone while already transferring them to my hardrive.