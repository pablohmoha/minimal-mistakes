---
title: "The Right way to using jupyter notebook in git bash"
categories:
  - Tutorials
tags:
  - jupyter
  - notebook
  - git bash
  - windows
---

Are you running "jupyter notebook" on windows cmd and it works fine, but on running the same on git bash (on windows) it doesn't work. This is the solution.

- Add Anaconda Scripts path for git bash to see, by first opening the bashrc file using vim as follows.

{% highlight bash %}
vim ~/.bashrc
{% endhighlight %}

![Opening vim]({{ "/assets/images/vim.png" | absolute_url }})

- Vim editor will open and you need to press 'I' in your keyboard to Insert/edit the file.
Add the path to Anaconda3 Script files on the open vim editor as follows.

{% highlight bash %}
PATH=$PATH:/c/Users/username/Anaconda3/Scripts
{% endhighlight %}

NB: In place of username replace with your username in my case it is Muhia. You can see this name from your git bash

![Editing vim]({{ "/assets/images/vimeditor.png" | absolute_url }})

- Once you have added the PATH to Anaconda3 scripts press 'Esc' key to exit editing. 
Enter ':' followed by 'x' and finally 'Enter' key to exit Vim editor.

- Now chek if the path was set well

{% highlight bash %}
which jupyter
{% endhighlight %}

- If no error shows up, now you are good to go. Run 

{% highlight bash %}
jupyter notebook
{% endhighlight %}

![Jupyter notebook]({{ "/assets/images/jupyternotebook.png" | absolute_url }})

Hope that helps and especially those starting out in data science and have been following tutorials which advices on using jupyter notebook on git bash for windows users.
