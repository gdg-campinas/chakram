# Contributing to Frisbee

We'd love for you to contribute to our source code and to make Frisbee even better than it is
today! Here are the guidelines we'd like you to follow:

 - [Code of Conduct](#coc)
 - [Question or Problem?](#question)
 - [Issues and Bugs](#issue)
 - [Feature Requests](#feature)
 - [Submission Guidelines](#submit)
 - [Coding Rules](#rules)
 - [Commit Message Guidelines](#commit)
 - [Signing the CLA](#cla)
 - [Further Info](#info)

## <a name="coc"></a> Code of Conduct
Help us keep Frisbee open and inclusive. Please read and follow our [Code of Conduct][coc].

## <a name="question"></a> Got a Question or Problem?

If you have questions about how to use Frisbee, please direct these to 
the [Google Plus Community][gplus-com].

## <a name="issue"></a> Found an Issue?
If you find a bug in the source code or a mistake in the documentation, you can help us by
submitting an issue to our [GitHub Repository][github]. Even better you can submit a Pull Request
with a fix.

***Localization Issue:*** *Frisbee uses the standard Android resource files for localizations. You should
submit a pull request with your translations here at github.*

**Please see the Submission Guidelines below**.

## <a name="feature"></a> Want a Feature?
You can request a new feature by submitting an issue to our [GitHub Repository][github].  If you
would like to implement a new feature then consider what kind of change it is:

* **Major Changes** that you wish to contribute to the project should be discussed first on 
the [Google Plus Community][gplus-com] so that we can 
better coordinate our efforts, prevent duplication of work, and help you to craft the change so that it is successfully accepted into the
project.
* **Small Changes** can be crafted and submitted to the [GitHub Repository][github] as a Pull Request.


## <a name="submit"></a> Submission Guidelines

### Submitting an Issue
Before you submit your issue search the archive, maybe your question was already answered.

If your issue appears to be a bug, and hasn't been reported, open a new issue.
Help us to maximize the effort we can spend fixing issues and adding new
features, by not reporting duplicate issues.  Providing the following information will increase the
chances of your issue being dealt with quickly:

* **Overview of the issue** - if an error is being thrown a non-minified stack trace helps
* **Motivation for or Use Case** - explain why this is a bug for you
* **Frisbee Version(s)** - is it a regression?
* **Reproduce the error** - provide an unambiguous set of steps.
* **Related issues** - has a similar issue been reported before?
* **Suggest a Fix** - if you can't fix the bug yourself, perhaps you can point to what might be
  causing the problem (line of code or commit)

**If you get help, help others. Good karma rulez!**

### Submitting a Pull Request
Before you submit your pull request consider the following guidelines:

* Search [GitHub](https://github.com/gdg-x/frisbee/pulls) for an open or closed Pull Request
  that relates to your submission. You don't want to duplicate effort.
* Please sign our [Contributor License Agreement (CLA)](#cla) before sending pull
  requests. Otherwise, it is assumed the contributor agrees to the CLA without signing.
* Make your changes in a new git branch. Please be aware that we are following the [git flow branching model](http://nvie.com/posts/a-successful-git-branching-model/) with `develop` as the branch for the next version:

     ```shell
     git checkout -b feature/my-shiny-contribution develop
     ```

* Create your patch, **including appropriate test cases**.
* Follow our [Coding Rules](#rules).
* Run the full Frisbee test suite, as described in the [developer documentation][dev-doc],
  and ensure that all tests pass.
* Commit your changes using a descriptive commit message that follows our
  [commit message conventions](#commit-message-format). 
  Adherence to the [commit message conventions](#commit-message-format)
  is required because release notes are automatically generated from these messages.

     ```shell
     git commit -a
     ```
  Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

* Build your changes locally to ensure all the tests pass

    ```shell
    ./gradlew test
    ```

* Push your branch to GitHub:

    ```shell
    git push origin feature/my-shiny-contribution
    ```

* In GitHub, send a pull request to `frisbee:develop`.
* If we suggest changes then 
  * Make the required updates.
  * Re-run the Frisbee test suite to ensure tests are still passing.
  * Rebase your branch and force push to your GitHub repository (this will update your Pull Request):

    ```shell
    git rebase develop -i
    git push -f
    ```

That's it! Thank you for your contribution!

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete feature/my-shiny-contribution
    ```

* Check out the develop branch:

    ```shell
    git checkout develop -f
    ```

* Delete the local branch:

    ```shell
    git branch -D feature/my-shiny-contribution
    ```

* Update your develop with the latest upstream version:

    ```shell
    git pull --ff upstream develop
    ```

## <a name="rules"></a> Coding Rules
To ensure consistency throughout the source code, keep these rules in mind as you are working:

* All features or bug fixes **must be tested** by one or more unit or integration test.
* With the exceptions listed below, we follow the rules contained in
  [Google's Android Style Guide][android-code]:
    * Wrap all code at **150 characters**.
    * Instead of complex inheritance hierarchies, we **prefer simple objects**. We use prototypical
      inheritance only when absolutely necessary.

## <a name="commit"></a> Git Commit Guidelines

We have very precise rules over how our git commit messages can be formatted.  This leads to **more
readable messages** that are easy to follow when looking through the **project history**.  But also,
we use the git commit messages to **generate the Frisbee change log**.

### Commit Message Format
Each commit message consists of a **header**, a **body** and a **footer**.  The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>: <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier
to read on github as well as in various git tools.

### Type
Must be one of the following:

* **feat**: A new feature
* **fix**: A bug fix
* **docs**: Documentation only changes
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing
  semi-colons, etc)
* **refactor**: A code change that neither fixes a bug or adds a feature
* **perf**: A code change that improves performance
* **test**: Adding missing tests
* **chore**: Changes to the build process or auxiliary tools and libraries such as documentation
  generation


### Subject
The subject contains succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* no dot (.) at the end

### Body
Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes"
The body should include the motivation for the change and contrast this with previous behavior.

### Footer
The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.


A detailed explanation can be found in this [document][commit-message-format].

## <a name="cla"></a> Signing the CLA 

Please sign our Contributor License Agreement (CLA) before sending pull requests. For any code
changes to be accepted, the CLA must be signed. It's a quick process, we promise!

* For individuals we have a [simple document][individual-cla].
* For corporations we have a [simple document][corporate-cla].

## <a name="info"></a> Further Information

[hub-api]: https://hub.gdgx.io/developers/api
[gplus-com]: https://plus.google.com/communities/100423211916386801761
[github]: https://github.com/gdg-x/frisbee
[dev-doc]: https://github.com/gdg-x/frisbee/wiki/Developer-Documentation 
[coc]: https://github.com/gdg-x/frisbee/blob/master/CODE_OF_CONDUCT.md
[corporate-cla]: https://github.com/gdg-x/frisbee/blob/master/misc/Frisbee-Individual.pdf?raw=true
[individual-cla]: https://github.com/gdg-x/frisbee/blob/master/misc/Frisbee-Entity.pdf?raw=true
[android-code]: http://source.android.com/source/code-style.html
[git flow]: http://nvie.com/posts/a-successful-git-branching-model/
