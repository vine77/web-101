### Welcome to Web 101

This mini-course will help you get started learning HTML and CSS to create webpages and JavaScript and Ember to create web applications.

### Get started with the command line

To get started, you should learn the basics of running commands with Terminal, which will be used for everything from installing apps to running a local server to saving code in a repository.
* Article: [Introduction to the Mac OS X Command Line (Treehouse)](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)
* Note: In this document, commands to be run in Terminal will be formatted like this:

    ```
    echo "Hello world"
    ```

* Make sure to learn basic commands like `cd` (change directory), `ls` (list directory contents), `pwd` (print working directory), and `man` (display manual)
* Learn the difference between absolute vs. relative paths
* Get comfortable with directory shorthands `~` (home directory), `/` (root directory), `..` (one directory up), and `.` (current directory)

### Prerequisites on Mac OS X

1. Install programs from the command line:
    1. Install homebrew:

        ```
        ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
        ```

    2. Install Node.js:

        ```
        brew install node
        ```

    3. Install git:

        ```
        brew install git
        ```

    4. Install Ember CLI:

        ```
        npm install -g ember-cli
        ```

    5. Enable color:

        ```
        git config --global color.ui true; echo "export CLICOLOR=1; export LSCOLORS=GxFxCxDxBxegedabagaced;" >> ~/.bash_profile && source ~/.bash_profile
        ```

2. Get started with Github, where we will be storing the code for your projects
    1. [Create a GitHub account](https://github.com)
    2. Tell git your name and email:

        ```
        git config --global user.name "YOUR NAME"
        ```

        ```
        git config --global user.email "YOUR EMAIL ADDRESS"
        ```

3. Install a text editor
    1. [Install Sublime Text](http://www.sublimetext.com/3)
    2. [Install Package Control for Sublime Text](https://packagecontrol.io/installation)
    3. [Install the Handlebars package for Sublime Text](https://github.com/daaain/Handlebars#installation)
    4. Set up the `subl` shortcut by running the following command in Terminal (which will allow you to open or create files with commands like `subl README` or open the current directory with `subl .`):

        ```
        ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
        ```

**Pro Tip**: Install [Ember Inspector](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi) for Google Chrome or [Ember Inspector](https://addons.mozilla.org/en-us/firefox/addon/ember-inspector/) for Mozilla Firefox.

### Your first app

1. Open Terminal and create a directory for your repositories:

    ```
    mkdir ~/repos
    ```

2. Go into your new repositories directory:

    ```
    cd ~/repos
    ```

3. Generate an Ember app called _hello-world_:

    ```
    ember new hello-world
    ```

    * **Note**: This will generate all the basic files necessary in a new `hello-world` directory and initialize it as a git repository

4. Go to your new project directory:

    ```
    cd ~/repos/hello-world
    ```

    * **Note**: Subsequent `ember` and `git` commands need to be run here, inside your project directory

5. Open your project in Sublime Text to see the files and folders generated for you:

    ```
    subl .
    ```

    * **Note**: The main files for your application are inside the `app` directory

6. Start a local web server:

    ```
    ember serve
    ```

    * **Note**: the server will only keep running as long as that Terminal window is open or until you press `control-c`

7. Open `http://localhost:4200` in web browser to see the Ember app live
8. Open the application template in Sublime Text, located at `app/templates/application.hbs`
9. Replace "Welcome to Ember.js" with something like "Hello world!" and save the file
10. Go back to your web browser and notice that the page has been automatically reloaded with your changes since the Ember server noticed that you saved the file
11. Open the CSS file located at `app/styles/app.css` and add something like `* { color: green; }` to change all color green
12. Congratulations on creating your first web application! Feel free to play around with putting more HTML in `app/templates/application.hbs` and more CSS in `app/styles/app.css`
13. To double check what files you modified, run:

    ```
    git status
    ```

14. To see the modified lines of code, run:

    ```
    git diff
    ```

15. Tell git which files you want to save (we'll save any changes in the app directory):

    ```
    git add app
    ```

    * **Note**: People often phrase this step as "staging" files, as in adding them to a staging area where they are on deck to be committed to the repository.

16. Save these files by committing them to the repository, with a message:

    ```
    git commit -m "Modified application"
    ```

17. Check the log of commits in your repository:

    ```
    git log
    ```

### Assignment 1

Objective: Create a web application with Ember and publish it to GitHub

Extra Credit: Add a photo to your GitHub profile

1. Follow the steps from [Your first app](#your-first-app), which creates a local repository on your computer for your project. You might want to call it something like "assignment-1" instead of "hello-world".
2. Create a new repository on GitHub (with the "+" icon in the upper-right), ideally using the same name as your Ember app.
3. Publish your local repository to GitHub's remote repository by following GitHub's instructions that pop up to "push an _existing_ repository from the command line".
4. Refresh your web browser to see the updates. This is your project's homepage on GitHub and you should be able to see your code online!
5. Send me the link to your project's homepage.
