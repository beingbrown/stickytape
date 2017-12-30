# Contributing

## Working on a Local Copy

1. [fork and clone the repo](https://help.github.com/articles/fork-a-repo/).
2. setup the working environment:

```sh
make bootstrap && make setup && make test 
```

This should setup a virtual environment and run the test suite. Eventually this step may be simplified.

## Using the Local Copy

Stickytape's executable can be found by running the scripts file of the same name:

```sh
scripts/stickytape
```

However, this script depends on stickytape being imported. To do this, you'll need to link the 'stickytape' directory from the parent directory into the scripts directory.

```sh
mv scripts/stickytape scripts/stickytape.py
ln -s ./stickytape scripts/stickytape
```

A build step will eventually be used to remove this requirement.

Now, you can run the application by targetting the new python file, and it will include your new local changes:

```sh
scripts/stickytape.py
```

Please note that, for the time being, you'll need to manually undo these changes. **Changes to the scripts folder should not be delivered**.

## Submitting Pull Requests

Currently, this project follows the 'upstream first' model. This means you can make your commits on master and submit a PR from your master to this one.

Happy Coding!