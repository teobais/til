> Today I Learned

_Things I learn/forget over time._

### Java
- Project with lots of modules - No matter [how hard you try to make an import work](https://stackoverflow.com/questions/26952078/intellij-cannot-resolve-symbol-on-import), if the module where you trying to import from is not defined as a dependency of your module (in your pom.xml), the import will not work.

### GitHub
- [GitHub doesn't support files larger than 100MB by default](https://toubou91.github.io/how-to-push-large-files-to-github/)

### Git
- You can force push directly to master from a detached head. Then, once on master, you have to pull.

### Unix
- You cannot use `(` or `)` as part of a filename, unless you surround that filename with quotes. The follwing will not work: `touch hello(asd)`, but this one will work: `touch "hello(asd)"`
- If a script put on cron gives an error like "cannot identify file or directory", it is probably because the crontab does not cd to the offending directory.
- cron can take up to 7 arguments: `minute hour dom month dow user cmd`.
Example: `H/5 * * * *` : The H will take a numeric hash of the Job name and use this to ensure that different jobs with the same cron settings do not all trigger at the same time.
H/5 in the first field means Every five minutes starting at some time between 0 and 4 minutes past the hour.
More details [here](http://www.unixgeeks.org/security/newbie/unix/cron-1.html) and [here](https://itisatechiesworld.wordpress.com/jenkins-related-articles/jenkins-configuration/jenkins-scheduling-jenkins-jobs-for-a-specific-time/). 

### Jekyll
- Jekyll does not include a post in the compiled version of your blog, unless `given timestamp <= current timestamp`
- One should always define the `url` value in the `_config.yml`. Eventhough it might work locally with an empty value for it, when deployed on Github Pages, it will cause assets like images to not be loaded.
