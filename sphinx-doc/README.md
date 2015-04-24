# Sphinx Doc Container

Sphinx Doc for drop in usage. Comes with following contribs:

* seqdiag
* blockdiag
* httpdomain

## Example Usage
Initialize you project with:

```
 docker run -i -v $(pwd)/src:/src/ -v $(pwd)/doc:/doc -w /doc -t kfinteractive/sphinx-doc:latest sphinx-quickstart
```

Then build your docs like so:

```
 docker run --rm -i -v $(pwd)/src:/src/ -v $(pwd)/doc:/doc -w /doc -t kfinteractive/sphinx-doc:latest make html
```

By mounting folders to the container with as Volumes (-v) you are able to build files on your host form the container without hassle. Wrap the make command with a shell script or a task runner like thor, rake, phake, etc. for less typing.
