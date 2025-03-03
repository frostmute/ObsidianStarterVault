---
tags:
  - Obsidian
  - jupyter
  - data-science
cssclasses:
  - page-grid
  - pen-purple
  - daily
  - saturday
category:
  - "[[Clippings]]"
source: '"[](https://medium.com/@biscotty666/obsidian-and-jupyter-notebooks-5d90ab3eab4c)"'
---
# Personal Knowledge Management for Data Science
[Brian Carey](https://medium.com/@biscotty666)[Follow](https://medium.com/@biscotty666)

androidstudio·March 21, 2024 (Updated: March 22, 2024)·Free: No

### Motivation

Jupyter notebooks, or more properly iPython notebooks, are fantastic tools for data exploration and modeling. You can run bits of code, interspersed with blocks of markdown, allowing you to easily work with data and present analyses and forecasts in a visual and interactive format. Notebooks can be easily shared via GitHub, or run on-line with Colab.

The problem with iPython notebooks, from a Personal Knowledge Management perspective, is they end up being "books on the shelf". For Obsidian users and PKM practitioners, the whole point is to get away from keeping information in notebooks, with all the uselessness that that implies. One could, as you will see, just do data exploration directly in Obsidian instead of in a standard iPython notebook. But Obsidian is not an IDE. The ecosystem around the interactive Python notebook IDEs, be it Jupyter Lab itself, or VS Code, etc, is so useful, that working in Obsidian while exploring data and creating models would be unacceptably tedious. Using fit-for-purpose tools is very important for efficiency.

We need a painless way to capture all this information in our vault, making **notes** out of the notebooks. How can we easily make this information future-useful, without repeating/duplicating our efforts or doing a ton of copy/paste? In this article, I'll explain the solution that works well for me, ensuring Obsidian-speed access to any bits of information I have in my notebooks, as well as making review and study activities so much more pleasant. And, of course, my canvases have all gotten richer as well.

### Setting up Obsidian

The community plugin needed to accomplish this is called [Execute Code](https://github.com/twibiral/obsidian-execute-code), written by Tim Wibiral, together with Jupyter itself and a Python library called "nbconvert". The latter will convert the notebooks to markdown, and the plugin allows you to execute the code directly within a note. To get started, create a virtual environment for Obsidian to use. If you aren't using virtual environments, please start now! It's simple, and you will avoid future problems. From the command line, do:

Copy`mkdir -p $HOME/.config/venvs && cd "$_" python -m venv obsidian_venv source obsidian_venv/bin/activate pip install --upgrade pip pip install jupyterlab nbconvert` 

You can also install other libraries like Pandas and Matplotlib as well into the virtual environment with pip install. Jupyter lab and nbconvert will be necessary to convert the notebooks to markdown. At this point, you could launch jupyter lab, but there is no need to. After installing packages, you can exit the virtual environment with "deactivate". Should you need to install more packages later, you can type "source $HOME/.config/venvs/obsidian_venv/bin/activate" to re-enter the virtual environment and `pip install` other packages.

In Obsidian, install the Execute Code plugin. After installing the plugin you must point it to the version of Python you want to use, in this case the one we made in the virtual environment above. In the settings for the plugin, under the language-specific settings, choose Python from the drop down list. For _Python Path_, enter "/home/directory/.config/venvs/obsidian_venv/bin/python".

With that done, any code block with the keyword "python", added directly after the opening back ticks of the block, can be run in the note. In Read View, a _Run_ button will appear by each code block, allowing you to execute the code in the block. After execution, there will be a _Clear_ button to clear up output that you want removed from the note. Code can also be executed from Edit View by using the keyword "run-python" rather than simply "python". The plugin offers a command to run all the code in the note, as well as a command to view and kill any active runtimes.

### Processing a notebook

Jupyter Lab can export an ipynb file directly to markdown! As of writing, VS Code can only export to py, pdf or html. From the file menu of Jupyter Lab, select _Export_ and choose _Markdown_. This will generate a zipped archive containing a markdown page, along with any image files in the notebook. The markdown file can be placed where-ever you want in the vault, and the images can be placed in your attachments directory. The problem with this approach. however, is that all of the image files get named "output" something, and so, after exporting a few notebooks, there will be name conflicts in your vault.

Using the command line avoids this problem, and is in any case much more efficient. You will need to activate your virtual environment with the "source" command as described above. Then type:

Copy`jupyter nbconvert --to Markdown your_notebook.ipynb`

This will generate a markdown file which can be copied into your vault. If there are images generated by the output, like graphs and other visuals, these will be put in a new directory created by the above command. If you copy this directory, with all the image files into the vault directory that you use for attachments, the new note will find them. (It is important to copy the directory itself and not just the files, since the new note will expect to find them there.)

Once in Obsidian you can process your Notebooks as you would any other file, breaking them into bite-size chunks of atomic goodness. I rely heavily on "Extract this heading" for this purpose, available with a right-click on any heading/section in a note. This replaces the section with a link to a newly-created note containing the section's content. I find it useful to apply a template that loads frequently used libraries, since they will need to be added them at the top of all the new files created in this manner.

When converting your notebooks to notes, be aware that different notes do not share the same runtime. Be sure to include all the variables/calculations necessary for the part of the code you extracted in the new file, as this will not be available from another file's state. Also, any images that you link to in the markdown sections of the original notebook will need to be manually copied into the vault, as only images generated from code in the file will be exported.

### Closing Thoughts

I first started using Obsidian for the specific purpose of studying data science. My use of Obsidian broadened considerably and quickly once I first began with it. However, after some time I realized that, because of the nature of iPython notebooks, and the necessity, or really the pleasure, of using them, I found myself many months later in the very position I was trying to avoid vis-a-vis my notes: information I needed was somewhere in my piles of notebooks, and I turned to Google more often than searching through my notebooks.

Now I can immerse myself in the Python project or study I am focusing on, knowing that after I'm finished, generating proper atomic notes from the work I'm doing will be a breeze. I hope that you may find this information useful. Happy coding!

***

[#pkm](https://medium.com/tag/pkm "Pkm")[#obsidian](https://medium.com/tag/obsidian "Obsidian")[#data-science](https://medium.com/tag/data-science "Data Science")[#python](https://medium.com/tag/python "Python")