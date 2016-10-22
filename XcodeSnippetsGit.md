## Sharing of Xcode code snippets
#### 0. Create new git repo on disk
- `mkdir ~/XcodeSnippets/`  
- `cd XcodeSnippets/; git init`  
- `git remote add origin https://github.com/[you]/my_snippets.git`  
- `cp -a ~/Library/Developer/Xcode/UserData/CodeSnippets/*.codesnippet ~/XcodeSnippets/`  

Push to your repo to fill it with snippets

#### *1. Checkout snippets repo somewhere on disk*
- `git clone git@some-repo.org:me/my_snippets.git ~/MyRepos/`

#### *2. Create Symlink of snippets directory to repo*
⚠️ We should have a backup, otherwise make one. No backup? sad smiley face
- `cd ~/Library/Developer/Xcode/UserData`  
- `rm -R CodeSnippets` - All is removed  
- `ln -s ~/XcodeSnippets/ CodeSnippets` - Create a symlink from repo to CodeSnippets folder

#### *3. Set up cron to pull repo every XX time*
- `crontab -e`
- `0 * * * * git -C ~/XcodeSnippets/ pull`
