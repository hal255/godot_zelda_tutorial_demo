# godot_zelda_tutorial_demo
https://www.youtube.com/watch?v=4CLvL05Av6g&amp;list=PLv0bAfkzWSiY4d_FJlQTlFOZh34nrlJZY&amp;index=1

## Steps to host Godot project on GitHub
Test Bed:
* OS: Windows 10
* Git Bash 2.23
* Godot 3.2 Alpha1

Steps to host on GitHub (there's probably an easier way, but... this is my way):
* On Godot 3.2:
  * Open project, and click Project tab > Export...
  * In Export window, click Add...
    * Select HTML5
    * Under Export Path, select your destination folder and name the file as "index" (which results to index.html). 
      * Ex: export_html
    * For vram compression, I just selected Desktop
    * Everything else, I left as default
    * When trying to open index.html, you'll get an error "Failed to open index.wasm". 
      * You will need to host this application.
        * Example: python http-server or github pages
* On GitHub:
  * Follow these steps to create new repo on GitHub: https://help.github.com/en/articles/create-a-repo
  * Copy url of new repo
* Open Git Bash to destination folder
  * $ git clone <paste repo_url here>
* Go to <godot_export_html> folder and copy all the contents of that folder
* Paste contents to the GitHub repo folder
* On Git Bash (from the repo folder), enter:
  * $ git add -A
  * $ git commit -m "some message"
  * $ git push
  * may need to enter credentials here
* On GitHub again:
  * Go to the repo of your html project
  * Click Settings tab
  * In Options Menu, scroll down to GitHub Pages section
    * Under Source, in first drop down menu, select master branch
    * Wait a few minutes and there will be a message in green "your site is published at..." under the this section

  
