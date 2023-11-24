# Setting up modules and adding dependencies

* Create a new repository
* Create a new main.go file
* Create a mod file by running `git mod init <name>`
* In another repository, run `go get github.com/<username>/<repositoryname>@latest` to get the repository to be imported and its latest commits
* The go.mod file will be updated with a reference to the new repository as an indirect dependency
* In a go file, import the repository using its address:
  `import "github.com/<username>/<repositoryname>`
  Now it is possible to use public methods from that repository, even though it is a different repository.
* Run `go mod tidy` to update the go.mod file. The dependency is now set as direct.
