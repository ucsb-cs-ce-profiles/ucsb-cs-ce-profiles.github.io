
# 7 Gate ML Cohort Synopsis

This repository is storing the progress the 7 Gate Machine Learning Cohort students made through their program. The content is served as a webpage.

### [Access it here](https://7-gate-academy-ml-program.github.io/Synopsis/)

## Add yourself as a student

1. Fork the repo
2. Add an .md file for your profile under `_students`, following the naming convention (`lastname_firstname.md`) 
3. Add the "front matter", i.e. the part that looks like below.  Be sure it starts and ends exactly with the three hyphens `---`, and that the rest is key value pairs with the appropriate syntax. 
   ```
   ---
   name: Example Student
   resume: true
   ---
   ```
   Set the resume to `true` or `false` depending on wether you want to have a resume shown or not.
4. Add a subdirectory that has the same name as your .md file (i.e. `lastname_firstname`).  In that subdirectory, put your profile picture **exactly** as `profile.jpg` (note the lower-case and the jpg extension). Try to keep the image size less than a MB.

5. If you have set `resume: true` put your resume in the same place as `resume.pdf`.

6. Do a pull request to incorporate your bio into the site.

## Submit your first homework

When you submit your homeworks to Synopsis, people who visit your profile can see them.

1. Pull the latest changes.
2. Inside your own folder, make a new folder named `homework1`. For subsequent homeworks, name the folder accordingly `homework2`, `homework3`, ...
3. Inside the folder put an `index.pdf` (or `index.html` if the homework asks for it). This is the presentations of your homework, it can be an export of your python notebook for example.
4. Feel free to add any supplementary material such as the `.ipynb` file (**must be** `index.ipynb`). Be mindful of the size of the files (no ML models or data etc.)
5. Submit a pull request.
