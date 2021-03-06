# 🌐 Recommended

External links I enjoy and would like share with others.

## 🤩 Popular repos

Lists of Github repos, sorted by various criteria.

- Repos I have [starred](https://github.com/MichaelCurrin?tab=stars) 
- [Most starred](https://github.com/search?q=stars%3A%3E100&s=stars&type=Repositories) on all Github.
- [Most forked](https://github.com/search?o=desc&q=stars:%3E1&s=forks&type=Repositories) on all Github.
- [Git most wanted](http://gitmostwanted.com/) - covers the most interesting repos on [GH Archive](https://www.gharchive.org/)

Some links above sourced from [here](https://stackoverflow.com/questions/19855552/how-to-find-out-the-most-popular-repositories-on-github).

## ⭐ My favorite websites and blogs

- [OpenSource.com](https://opensource.com)
- [Free Code Camp](http://freeCodeCamp.org)
- [dev.to](https://dev.to)
- [Medium.com](https://medium.com) topics
    - [Programming](https://medium.com/topic/programming)
    - [Software engineering](https://medium.com/topic/software-engineering)
    - [Data Science](https://medium.com/topic/data-science)
- [Towards Data Science](https://towardsdatascience.com/) (see topics like Data Science, AI, Python, Machine Learning)
- [Flowing Data](https://flowingdata.com)

## 🛠 Online tools

### Git Pod

- [GitPod.io](https://gitpod.io) 

A free cloud-based IDE that runs Github repos. Edit code with a VS Code editor, run in the terminal and save your changes to Github. Also includes a way to view and manager Pull Requests. Runs in a container environment and can be configured with a Git Pod file in your repo.

### Python Anywhere

- [PythonAnywhere.com](https://pythonanywhere.com)

Free Python hosting. Includes web server with easy configuration along with a MySQL database if you need. Run cron jobs, edit files editing and use consoles for Python, Bash and SQL.

### Github pages

- [pages.github.com](https://pages.github.com/)

Free hosting for static sites built with Jekyll or plain HTML

### StackEdit

- [StackEdit.io](https://stackedit.io/) site

Edit markdown files on Github using your browser. 

 - The editor makes it easy to apply formatting using buttons rather than typing it up. It includes a preview alongside the edit view, unlike Github's editor which switches between edit and preview modes. 
- Edit and sync files on the following platforms
	- Dropbox
	- Github - When you link these, you can choose to include or exclude private repo access.
	- Gitlab
	- Google Drive
- How to edit a repo:
	1. Go to [stackedit.io](https://stackedit.io/). You will start at a welcome page.
	2. Sign in with Github.
	3. From the menu on the right, select Workspaces.
	4. Select "Add a Github workspace".
	5. Enter a repo path. Optionally set folder path and branch.
	6. You will see your folder tree on the left. Note that files will give a data error initially while content is being pulled in.
	7. Edit files. You do not have to press save - changes will be saved and synced for you and these will appear as commits in Github.
	8. You may add more repos using steps above and then switch between then.

Usage notes:

- You can undo and redo and the keyboard shortcuts work for this.
- Indentation is done with tabs.
- The `.md` extension will be hidden.
- Files which are not markdown files will be hidden from the folder view.
- If a file is deleted, it goes to Trash (and in Github to a trash folder).
- If a file is renamed, StackEdit will actually delete the file and create a few file at the commit level, so you will lose history within a file.
- Although the Welcome file shows in the tree, it is not actually stored in the repo. You can delete it from the editor view, but it can be useful to keep open as a quick reference.
- For help, select Table of Contents from the menu on the right.
- You do not have save - it autosaves for you. Auto sync defaults to 90 seconds and the minimum is 60 seconds. Every sync which contains changes causes a commit, so you might want to make this less frequent like every 5 minutes. You can also click the sync button in the top right to force a sync, in case you need to view the results on Github.
- Click Settings in the right menu. You can override default settings.
- Use `CTRL+SHIFT+V` in the docs to paste *without* formatting - I found this necessary to avoid unnecessary open lines when copying code from an IDE into a markdown codeblock. When not using a codeblock, you may want to keep the pasted line breaks, as the double spacing is needed for line breaks to render in Markdown.

<!--stackedit_data:
eyJwcm9wZXJ0aWVzIjoiZXh0ZW5zaW9uczpcbiAgcHJlc2V0Oi
BnZm1cbiIsImhpc3RvcnkiOlstMjAyMjU5MDI5NV19
-->