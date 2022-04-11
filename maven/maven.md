# maven cheat sheet

## Docker

### Run maven container with docker using a different user than root:

* First run the docker container:

  `docker run -v $(pwd):/app -v ~/.m2:/var/maven/.m2 -ti --rm -u $(id -u):$(id -g) -e MAVEN_CONFIG=/var/maven/.m2 maven sh`

* Then when running any maven command specify the maven home with the following switch:

  `-Duser.home=/var/maven`

## CLI

* [CLI Options](http://maven.apache.org/ref/3.1.0/maven-embedder/cli.html)
  * `-am, --also-make`: If project list is specified, also build projects required by the list
  * `-amd, --also-make-dependents`: If project list is specified, also build projects that depend on projects on the list
  * `-e, --errors`: Produce execution error messages
  * `-N, --non-recursive`: Do not recurse into sub-projects
  * `-T,--threads`: Thread count, for instance 2.0C where C is core multiplied
  * `-X, --debug`: Produce execution debug output

## POM

* [POM Reference](https://maven.apache.org/pom.html)

## Settings

* [Settings Reference](https://maven.apache.org/settings.html)
* [Security Settings](https://maven.apache.org/guides/mini/guide-encryption.html)

```bash
# Specify settings.xml file from mvn cli
mvn -s <path/to/settings.xml> <goals or phases>
mvn -s ~/.m2/settings-custom.xml clean install

# Specify local repository path/location
mvn -Dmaven.repo.local=<pat/to/local/repo>

```

## Useful Plugins

### Help Plugin

```bash
# Check which profiles are actives
mvn help:active-profiles

# Get effective pom
mvn help:effective-pom -Doutput=effective-pom.xml

# To get value of maven property
mvn help:evaluate -Dexpression=project.version -q -DforceStdout -N
```

### Dependency Plugin

```bash
# To view dependency tree
mvn dependency:tree
```

### Exec Plugin

```bash
# Get maven project version
mvn -q -Dexec.executable=echo -Dexec.args='${project.version}' --non-recursive exec:exec
```

## More Info

* https://blog.sonatype.com/2009/10/maven-tips-and-tricks-advanced-reactor-options/