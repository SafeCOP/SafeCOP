# SafeCOP
SafeCOP main repository

### Repository organization
This repository is organized as follows:
- For each WP and UC, there is a _submodule_ that tracks the status of the _release_ branch of the corrispondent sub-repository
- All the contribution to a WP/UC is done in the corrispondent sub-repository (the branch _master_ is the development branch). When WP/UC contribuitors want to release a new version, they should merge the _master_ branch into the _release_ branch, so that the main repository (this one) and its sub-modules can be updated

### Additional information on Git
[Quick Git tutorial (video)](https://youtu.be/IHaTbJPdB-s)
[Interactive tutorial on Git](https://learngitbranching.js.org/)

### Example worflow
Example: a partner wants to contribute to the WP1 repository. He/She first clone the sub-repository to his/hers local machine:
```
git clone https://github.com/SafeCOP/WP1.git
```
Then he/she ensureis to work in the _master_ branch:
```
git checkout master
```
Now, he/she can edit the repository content with the standard Git workflow:
(for example):
```
echo test > test.txt
git add test.txt
git commit -m "example commit"
git push origin master
```
Once the WP1 reaches a new release, developers can merge _master_ into _release_:
```
git checkout release
git merge master
git checkout master
```
