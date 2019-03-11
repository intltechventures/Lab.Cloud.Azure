
Azure Git Resources
====


### Azure Git References
* https://docs.microsoft.com/en-us/azure/devops/repos/git/

* https://docs.microsoft.com/en-us/azure/devops/repos/git/limits
  * "Repositories should generally be no larger than 10GB."
  * "In uncommon circumstances, repositories may be larger than 10GB. For instance, the Windows repository is at least 300GB. For that reason, we do not have a hard block in place"
  * "If your repository grows beyond 10GB, consider using Git-LFS, GVFS, or Azure Artifacts to refactor your development artifacts."
  * "pushes are limited to 5GB at a time."
  * "If the repository is more than 5GB, then you must use the web to Import the repository instead of the command line."

* https://docs.microsoft.com/en-us/azure/devops/integrate/concepts/rate-limits?view=azure-devops
  * "Uploading a large number of files to Team Foundation version control ```or Git``` typically creates a large amount of load on both an Azure SQL Database and an Azure Storage account."
  * "We take a similar approach to rate limiting in Azure Pipelines. Since pipelines are not associated to a single user like other activities, each pipeline is treated as an individual entity with its own resource consumption tracked. Just like the global consumption limit for users, we apply a 200 TSTU limit for an individual pipeline in a sliding 5-minute window. Even if build agents are self-hosted, there could be load on Azure DevOps Services resources for operations such as ```git clone.```"

* https://docs.microsoft.com/en-us/azure/devops/learn/git/git-at-scale   

* [Git Virtual File System Architecture](https://docs.microsoft.com/en-us/azure/devops/learn/git/gvfs-architecture)
  * https://docs.microsoft.com/en-us/azure/devops/learn/git/gvfs-design-history



### Large File Support
* [Manage and store large files in Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/manage-large-files?view=azure-devops)
  * "Don't commit large, frequently updated binary assets"
  * "Strategies for working with large binary source files"
    * "Don't commit large, frequently updated binary assets"
    * "Don't commit compressed archives of data. It's better to uncompress the files and commit the diffable sources, letting Git handle compressing the data in your repo."
    * "Avoid committing compiled code and other binary dependencies. Commit the source and build the dependencies, or use a package management solution to version and supply these files to your system."
  * "Use Git Large File Storage (LFS)"
    * "When you have source files with large differences between versions and frequent updates, you can use Git LFS to manage these file types. Git LFS is an extension to Git which commits data describing the large files in a commit to your repo, and stores the binary file contents into separate remote storage. When you clone and switch branches in your repo, Git LFS downloads the correct version from that remote storage. Your local development tools will transparently work with the files as if they were committed directly to your repo."
    * "The benefit of Git LFS is that your team can use the familiar end to end Git workflow no matter what files your team creates. LFS files can be as big as you need them to be. Additionally, as of version 2.0, Git LFS supports file locking to help your team work on large, undiffable assets like videos, sounds, and game maps."
    * "Git LFS is is fully supported and free in Azure DevOps Services. To use LFS with Visual Studio, you need at least Visual Studio 2015 Update 2. Just follow the instructions to install the client, set up LFS tracking for files on your local repo, and then push your changes to Azure Repos."
  * "Limitations: Git LFS has some drawbacks that you should consider before adopting:"
    * ```"Every Git client used by your team must install the Git LFS client and understand its tracking configuration."```
    * ```"If the Git LFS client is not installed and configured correctly, you will not see the binary files committed through Git LFS when you clone your repo. Git will download the data describing the large file (which is what Git LFS commits to the repo) and not the actual binary file itself. Committing large binaries without the Git LFS client installed will push the binary to your repo."```
    * "Git cannot merge the changes from two different versions of a binary file even if both versions have a common parent. If two people are working on the same file at the same time, they must work together to reconcile their changes to avoid overwriting the other's work. Git LFS provides file locking to help. Users must still take care to always pull the latest copy of a binary asset before beginning work."
    * ```"Azure Repos currently does not support using SSH in repos with Git LFS tracked files."```
    * "If a user drags and drops a binary file via the web interface into a repo which is configured for Git LFS, the binary will be committed to the repo and not the pointers that would be committed via the Git LFS client."
  * "The GitHub URL included for the version value only defines the LFS pointer file type, and is not a link to your binary file."
    * "The file written into your repo for a Git LFS tracked file will have a few lines with a key and value pair on each line:"
      * ```version https://git-lfs.github.com/spec/v1"```
      * ```oid a747cfbbef63fc0a3f5ffca332ae486ee7bf77c1d1b9b2de02e261ef97d085fe```
      * ```size 4923023```




### File Size Limit Issues:
* https://github.com/MicrosoftDocs/vsts-docs/issues/1400
  * chrisrpatterson commented on Sep 13, 2018
    * "Currently there is no hard limit set just like there is no hard limit set for repos."

* https://github.com/MicrosoftDocs/vsts-docs/issues/1520
  * "```I tested Git LFS for a site of 20G```, the first time I want to commit all the files with LFS it didn't working. There is ' adding files error' . I think it would be appreciable to mention the maximum size of the file to commit while using Git lfs"


