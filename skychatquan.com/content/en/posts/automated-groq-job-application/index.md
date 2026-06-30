---
title: Automated Groq Job Application
date: 2025-02-22
author: Sky Quan
description: Description of Automated Groq Job Application project
tags:
  - project
---

This post details my work on my automated groq job application project. The code can be found on my github here: 
* https://github.com/Ctrl-Sky/automated-groq-job-application.git

# Project Overview
This project automates the job application process using Python and Groq. The model takes a job description, your resume, and your CV, and then the model provides suggestions for points to add to your resume based on your CV that best match the job description.

With these suggestions, the model then helps in generating ideas and key content for a cover letter. The resulting resume and cover letter drafts are then saved as a .docx file for editing and personalization.

Furthermore, the generated resume, cover letter, and job description is stored in the hidden outputs directory organized by the date the application was made and the company's name. This allows for revisiting and tracking your job applications over time. Additionally, the system logs each interaction in a CSV file, providing a record of the jobs you've applied to with this automation.

# Tools Used
* Python
* Groq
* Bash
* Powershell

# The Purpose for Creation
Back in my second year when I was applying for jobs, I felt the application process to be very tedious. I was applying to many different jobs and which each job I was personalizing my resume, this would result in many different variation of my resume being all over the place. On top of that, when I landed an interview, because I was applying to so many jobs, I was unable to identify which resume I used in the application or even what the job description was. This, of course, created many problems for me when the interview came along. So, because of those reasons, I decided to create this project to remove the tediousness of each application and better organize my different resumes and files. Leading to smoother more efficient application process.