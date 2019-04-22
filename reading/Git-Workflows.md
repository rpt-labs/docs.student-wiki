## Git Workflows

### Beginning of a new sprint for **ONSITE** students

At the beginning of each sprint, you'll get access to a a new git repository that will contain the code you'll be working with.

- Go to the Learn app and navigate to the assignment
- Find the repo on github. In this case, `https://github.com/hackreactor/{cohort-prefix}-recursion-review`
- Find yourself a nice spot on the pair stations with your partner.
- Fork the school repo to your account on GitHub.
- Make sure your Pair forks the Hack Reactor repo on GitHub as well.
- Clone **YOUR FORK** of the Hack Reactor repo `git clone https://github.com/<YOUR_GITHUB_HANDLE>/{cohort-prefix}-recursion-review.git`
- Add **YOUR PAIR'S FORK** as a remote of your local repo, I'm naming the remote my pair's GitHub handle so I remember which one is which `git remote add svnh https://github.com/svnh/{cohort-prefix}-recursion-review.git`
- Add the original HR repo as an upstream remote `git remote add upstream https://github.com/hackreactor/{cohort-prefix}-recursion-review.git`
- Do some work ... don't forget to commit frequently!
- **\*harp noise*** Time to start wrapping up, time to push up to both of our GitHub accounts.
- Make sure you push to BOTH of your forks.
 - Push your work to your branch `git push origin master`
 - Push your work to your pair's branch `git push <REMOTE_NAME> master`, so for me it'll be `git push svnh master`
- Done. All your work is now on your GitHub account.

### Beginning of a new sprint for **REMOTE** students

At the beginning of each sprint, you'll get access to a new git repository that will contain the code you'll be working with.

- Go to the Learn app and navigate to the assignment
- Find the repo on github. In this case, `https://github.com/hackreactor/{cohort-prefix}-recursion-review`
- Fork the school repo to your account on GitHub.
- Make sure your Pair forks the Hack Reactor repo on GitHub as well.
- Clone **YOUR FORK** of the Hack Reactor repo `git clone https://github.com/<YOUR_GITHUB_HANDLE>/{cohort-prefix}-recursion-review.git`
- Add the original HR repo as an upstream remote `git remote add upstream https://github.com/hackreactor/{cohort-prefix}-recursion-review.git`

At this point, one person should tell their pair, "I will start the Floobits setup." The next steps depend on whether you're doing the setup or joining someone else's setup.

#### Floobits -- If you're doing the setup:

* Open the entire project directory in Sublime Text (eg, `subl .` from your terminal if you're `cd`ed into your project directory)
* If you get an error in the next steps, please reach out to your staff so they can delete unused Floobits workspaces at https://floobits.com/HackReactor. (Hint: You can delete your old workspaces to expedite this process.)
* Right-click on the folder name in the sidebar, then select `Floobits` -> `Share This (Private)`.  Select `HackReactor` as the owner. (Selecting `HackReactor` is crucial to allow staff to see your code.)
* In the input box at the bottom of Sublime Text, you will be provided with a workspace name that matches the name of your repo. To prevent name collisions with other workspaces, add your name and your pairs name to the end of the workspace. Example: `https://floobits.com/HackReactor/{cohort-prefix}-recursion-review-aragorn-boromir`
* An alert box will pop up with your workspace URL. Copy the link and send it to your pair. If you accidentally closed that box, or misplaced the URL, you can find it in the `.floo` file in the top level of your project directory.
* If your partner receives a permissions error trying to join the Floobits workspace, make a help request!

#### Floobits -- If you're joining someone else's setup:

* Join the Floobits project by either:
  * Open the `Tools` menu, then select `Floobits` -> `Join Workspace`
  * Or `CTRL + SHIFT + J`
* Sublime Text asks you at the very bottom of the window where you want to save a local copy of the Floobits workspace. The default is `/user/floobits/workspace-name`, but you must save it to the same directory path as your cloned repo. Use the command `pwd` in the terminal to get the specific path of your clone.
* When prompted, always select "Overwrite Local Changes", DO NOT overwrite remote changes.

#### Floobits -- Rejoin a workspace to resume a coding session:

* Open the `Tools` menu, then select `Floobits` -> `Join Recent Workspace`
* Or `CTRL + OPTION + SHIFT + J`
* General rule of thumb is to overwrite all local files (especially if your partner has been working in the Floobits session while you were disconnected) instead of overwriting all remote files.

#### Git -- Save and upload your work

Once you're done closing your git repo, setting up Floobits, and verifying that both pairs have joined the Floobits sessions, do the following:

- Do some work ... don't forget to commit frequently!
- **\*harp noise*** Time to start wrapping up, time to push up to both of our GitHub accounts.
- Make sure EACH of you push to your forks via `git push origin master`
- Done. All your work is now on your GitHub account. Verify by opening your repo at `https://github.com/<YOUR_GITHUB_HANDLE>/{cohort-prefix}-recursion-review.git`.
