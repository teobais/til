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

### Jekyll
- Jekyll does not include a post in the compiled version of your blog, unless `given timestamp <= current timestamp`
