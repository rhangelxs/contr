# Contributing to HMI course
:+1::tada: First off, thanks for taking the time to contribute! :tada::+1:

The following is a set of guidelines for contributing to my course, which are hosted on GitHub. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

#### Table Of Contents

[Code of Conduct](#code-of-conduct)

<!--[I don't want to read this whole thing, I just have a question!!!](#i-dont-want-to-read-this-whole-thing-i-just-have-a-question)-->

[Project Conventions](#project-conventions)
  * [File structure](#file-structure)
  * [Suggesting Enhancements](#suggesting-enhancements)
  * [Your First Code Contribution](#your-first-code-contribution)
  * [Pull Requests](#pull-requests)

[Styleguides](#styleguides)
  * [Git Commit Messages](#git-commit-messages)
  * [JavaScript Styleguide](#javascript-styleguide)
  * [CoffeeScript Styleguide](#coffeescript-styleguide)
  * [Specs Styleguide](#specs-styleguide)
  * [Documentation Styleguide](#documentation-styleguide)

[Additional Notes](#additional-notes)
  * [Issue and Pull Request Labels](#issue-and-pull-request-labels)

## Code of Conduct

To be ...

## Project Conventions
There are a few conventions that have developed over time.

As of 2017 projects consists up to four parts, called: `report`, `dataset`, `script` and `presentation`.
Content of this parts will be described below.

Suggested file structure provided in special section - file structure.

* **Report** file are typically describe experimental design and details of realization of the research project.
	* Basically it is text file, but you can include any support materials if it is needed.
	* Try not to add too much though, but stay clear and add all needed explanations here.
* **Dataset** that include all original data
	* Check that you reporting your data in raw format (not in aggregated form)
	* Check column names
	* Fit to your variables
	* Units for every variable is clear
	* Often numerical data should be machine readable
* **Script** file contains analysis and results of checking you assumptions.
	* Script can be published in two types: *original code* and *compiled one*. Compiled version is human readable and published in exchangeable formats like HTML, Markdown or others.

	  > **Note.** Jypyther Notebook contains both code and output, so it might be upload as is.
	
	* Please, always include **compiled version of your script**. Compiled or human readable means any output of your script (even in txt). Because nobody have have the same libraries as yours on they machines.
	* You can include both versions (included the original one), if prefer.

* **Presentation** is essential results that you get.
	* Printable version of you presentation is the best option to publish.

### File structure

File structure is important.

We will document it in this file. If you have a question around how to do things, check to see if it is documented here. If it is not documented there, please ask your question.

You should make a significant decision how you will publish and maintain the project files, what you should or shouldn't publish.

First, please be noted that your project root folder will be locatet under [github.com/rhangelxs/hmi_class/projects/year/](github.com/rhangelxs/hmi_class/projects/)

#### Project root folder name

Please name your root folder using comma separated surnames of the author's. So it will looks `Petrov, Sidirov`.

> **Note**. Please don't use short name of project. It can be usend in filenames (see Filenames option 2, described below).

#### File names

The two main variants are available:

1. Using same common name for all parts of project.
   
   It could be description of project in short form. 
   Please don't specify year  (like `42design`).
   
   In this case filenames will looks like:
   
   * For report – `42design.docx`.
   * Presentation – `42design.pdf`.
   * `42design.csv` for dataset.

2. Using unique file names for specific part of your project. In this case special requirement applied.
  
  * Report should be started with short form project name like `42design_description`.
  * Dataset: `dataset` or `data`.
  * Presentation should named literally `presentation`.
  * All script formats (original one and output or compiled one) should have the same name like  `script.Rmd`, `script.html`, etc.
  
  Of course, all files should have a valid extension according to the filetypes.

Suggesting Enhancements
This section guides you through submitting an enhancement suggestion for Atom, including completely new features and minor improvements to existing functionality. Following these guidelines helps maintainers and the community understand your suggestion :pencil: and find related suggestions :mag_right:.

Before creating enhancement suggestions, please check this list as you might find out that you don't need to create one. When you are creating an enhancement suggestion, please include as many details as possible. Fill in the template, including the steps that you imagine you would take if the feature you're requesting existed.

Before Submitting An Enhancement Suggestion

* *Check the debugging guide* for tips — you might discover that the enhancement is already available. Most importantly, check if you're using the latest version of Atom and if you can get the desired behavior by changing Atom's or packages' config settings.
* *Check if there's already a package which provides that enhancement.*
* *Determine which repository the enhancement should be suggested in.*
* *Perform a cursory search* to see if the enhancement has already been suggested. If it has, add a comment to the existing issue instead of opening a new one.

How Do I Submit A (Good) Enhancement Suggestion?
Enhancement suggestions are tracked as GitHub issues. After you've determined which repository your enhancement suggestion is related to, create an issue on that repository and provide the following information:

* Use a clear and descriptive title for the issue to identify the suggestion.
* Provide a step-by-step description of the suggested enhancement in as many details as possible.
* Provide specific examples to demonstrate the steps. Include copy/pasteable snippets which you use in those examples, as Markdown code blocks.
* Describe the current behavior and explain which behavior you expected to see instead and why.
* Include screenshots and animated GIFs which help you demonstrate the steps or point out the part of Atom which the suggestion is related to. You can use this tool to record GIFs on macOS and Windows, and this tool or this tool on Linux.
* Explain why this enhancement would be useful to most Atom users and isn't something that can or should be implemented as a community package.
* List some other text editors or applications where this enhancement exists.
* Specify which version of Atom you're using. You can get the exact version by running atom -v in your terminal, or by starting Atom and running the Application: About command from the Command Palette.
* Specify the name and version of the OS you're using.

Your First Code Contribution
Unsure where to begin contributing to Atom? You can start by looking through these beginner and help-wanted issues:

* Beginner issues - issues which should only require a few lines of code, and a test or two.
* Help wanted issues - issues which should be a bit more involved than beginner issues.

Both issue lists are sorted by total number of comments. While not perfect, number of comments is a reasonable proxy for impact a given change will have.

If you want to read about using Atom or developing packages in Atom, the Atom Flight Manual is free and available online. You can find the source to the manual in atom/flight-manual.atom.io.

Pull Requests

* Fill in the required template
* Do not include issue numbers in the PR title
* Include screenshots and animated GIFs in your pull request whenever possible.
* Follow the JavaScript and CoffeeScript styleguides.
* Include thoughtfully-worded, well-structured Jasmine specs in the ./spec folder. Run them using atom --test spec. See the Specs Styleguide below.
* Document new code based on the Documentation Styleguide
* End all files with a newline
* Avoid platform-dependent code
* Place requires in the following order:
	* Built in Node Modules (such as path)
	* Built in Atom and Electron Modules (such as atom, remote)
	* Local Modules (using relative paths)
* Place class properties in the following order:
	* Class methods and properties (methods starting with a @ in CoffeeScript or static in JavaScript)
	* Instance methods and properties

Styleguides

Git Commit Messages

* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or less
* Reference issues and pull requests liberally after the first line
* When only changing documentation, include [ci skip] in the commit description
* Consider starting the commit message with an applicable emoji:
	* :art: :art: when improving the format/structure of the code
	* :racehorse: :racehorse: when improving performance
	* :non-potable_water: :non-potable_water: when plugging memory leaks
	* :memo: :memo: when writing docs
	* :penguin: :penguin: when fixing something on Linux
	* :apple: :apple: when fixing something on macOS
	* :checkered_flag: :checkered_flag: when fixing something on Windows
	* :bug: :bug: when fixing a bug
	* :fire: :fire: when removing code or files
	* :green_heart: :green_heart: when fixing the CI build
	* :white_check_mark: :white_check_mark: when adding tests
	* :lock: :lock: when dealing with security
	* :arrow_up: :arrow_up: when upgrading dependencies
	* :arrow_down: :arrow_down: when downgrading dependencies
	* :shirt: :shirt: when removing linter warnings

JavaScript Styleguide
All JavaScript must adhere to JavaScript Standard Style.

* Prefer the object spread operator ({...anotherObj}) to Object.assign()
* Inline exports with expressions whenever possible`js
 Use this:
export default class ClassName {



}

// Instead of:
class ClassName {

}
export default ClassName


CoffeeScript Styleguide

* Set parameter defaults without spaces around the equal sign
  * clear = (count=1) -> instead of clear = (count = 1) ->
* Use spaces around operators
  * count + 1 instead of count+1
* Use spaces after commas (unless separated by newlines)
* Use parentheses if it improves code clarity.
* Prefer alphabetic keywords to symbolic keywords:
  * a is b instead of a == b
* Avoid spaces inside the curly-braces of hash literals:
  * {a: 1, b: 2} instead of { a: 1, b: 2 }
* Include a single line of whitespace between methods.
* Capitalize initialisms and acronyms in names, except for the first word, which
should be lower-case:
* getURI instead of getUri
* uriToOpen instead of URIToOpen
* Use slice() to copy an array
* Add an explicit return when your function ends with a for/while loop and
you don't want it to return a collected array.
* Use this instead of a standalone @
* return this instead of return @

Specs Styleguide

- Include thoughtfully-worded, well-structured Jasmine specs in the ./spec folder.
- Treat describe as a noun or situation.
- Treat it as a statement about state or how an operation changes state.

Example


describe 'a dog', ->
it 'barks', ->
# spec here
describe 'when the dog is happy', ->
it 'wags its tail', ->
# spec here


Documentation Styleguide

* Use AtomDoc.
* Use Markdown.
* Reference methods and classes in markdown with the custom {} notation:
	* Reference classes with {ClassName}
	* Reference instance methods with {ClassName::methodName}
	* Reference class methods with {ClassName.methodName}

Example


# Public: Disable the package with the given name.
#
# * `name`    The {String} name of the package to disable.
# * `options` (optional) The {Object} with disable options (default: {}):
#   * `trackTime`     A {Boolean}, `true` to track the amount of time taken.
#   * `ignoreErrors`  A {Boolean}, `true` to catch and ignore errors thrown.
# * `callback` The {Function} to call after the package has been disabled.
#
# Returns `undefined`.
disablePackage: (name, options, callback) ->


Additional Notes

Issue and Pull Request Labels
This section lists the labels we use to help us track and manage issues and pull requests. Most labels are used across all Atom repositories, but some are specific to atom/atom.

GitHub search makes it easy to use labels for finding groups of issues or pull requests you're interested in. For example, you might be interested in open issues across atom/atom and all Atom-owned packages which are labeled as bugs, but still need to be reliably reproduced or perhaps open pull requests in atom/atom which haven't been reviewed yet. To help you find issues and pull requests, each label is listed with search links for finding open items with that label in atom/atom only and also across all Atom repositories. We  encourage you to read about other search filters which will help you write more focused queries.

The labels are loosely grouped by their purpose, but it's not required that every issue have a label from every group or that an issue can't have more than one label from the same group.

Please open an issue on atom/atom if you have suggestions for new labels, and if you notice some labels are missing on some repositories, then please open an issue on that repository.

Type of Issue and Issue State
| Label name | atom/atom :mag_right: | atom‑org :mag_right: | Description |
| - | - | - | - |
| enhancement | search | search | Feature requests. |
| bug | search | search | Confirmed bugs or reports that are very likely to be bugs. |
| question | search | search | Questions more than bug reports or feature requests (e.g. how do I do X). |
| feedback | search | search | General feedback more than bug reports or feature requests. |
| help-wanted | search | search | The Atom core team would appreciate help from the community in resolving these issues. |
| beginner | search | search | Less complex issues which would be good first issues to work on for users who want to contribute to Atom. |
| more-information-needed | search | search | More information needs to be collected about these problems or feature requests (e.g. steps to reproduce). |
| needs-reproduction | search | search | Likely bugs, but haven't been reliably reproduced. |
| blocked | search | search | Issues blocked on other issues. |
| duplicate | search | search | Issues which are duplicates of other issues, i.e. they have been reported before. |
| wontfix | search | search | The Atom core team has decided not to fix these issues for now, either because they're working as intended or for some other reason. |
| invalid | search | search | Issues which aren't valid (e.g. user errors). |
| package-idea | search | search | Feature request which might be good candidates for new packages, instead of extending Atom or core Atom packages. |
| wrong-repo | search | search | Issues reported on the wrong repository (e.g. a bug related to the Settings View package was reported on Atom core). |

Topic Categories
| Label name | atom/atom :mag_right: | atom‑org :mag_right: | Description |
| - | - | - | - |
| windows | search | search | Related to Atom running on Windows. |
| linux | search | search | Related to Atom running on Linux. |
| mac | search | search | Related to Atom running on macOS. |
| documentation | search | search | Related to any type of documentation (e.g. API documentation and the flight manual). |
| performance | search | search | Related to performance. |
| security | search | search | Related to security. |
| ui | search | search | Related to visual design. |
| api | search | search | Related to Atom's public APIs. |
| uncaught-exception | search | search | Issues about uncaught exceptions, normally created from the Notifications package. |
| crash | search | search | Reports of Atom completely crashing. |
| auto-indent | search | search | Related to auto-indenting text. |
| encoding | search | search | Related to character encoding. |
| network | search | search | Related to network problems or working with remote files (e.g. on network drives). |
| git | search | search | Related to Git functionality (e.g. problems with gitignore files or with showing the correct file status). |

atom/atom Topic Categories
| Label name | atom/atom :mag_right: | atom‑org :mag_right: | Description |
| - | - | - | - |
| editor-rendering | search | search | Related to language-independent aspects of rendering text (e.g. scrolling, soft wrap, and font rendering). |
| build-error | search | search | Related to problems with building Atom from source. |
| error-from-pathwatcher | search | search | Related to errors thrown by the pathwatcher library. |
| error-from-save | search | search | Related to errors thrown when saving files. |
| error-from-open | search | search | Related to errors thrown when opening files. |
| installer | search | search | Related to the Atom installers for different OSes. |
| auto-updater | search | search | Related to the auto-updater for different OSes. |
| deprecation-help | search | search | Issues for helping package authors remove usage of deprecated APIs in packages. |
| electron | search | search | Issues that require changes to Electron to fix or implement. |

Pull Request Labels
| Label name | atom/atom :mag_right: | atom‑org :mag_right: | Description
| - | - | - | - |
| work-in-progress | search | search | Pull requests which are still being worked on, more changes will follow. |
| needs-review | search | search | Pull requests which need code review, and approval from maintainers or Atom core team. |
| under-review | search | search | Pull requests being reviewed by maintainers or Atom core team. |
| requires-changes | search | search | Pull requests which need to be updated based on review comments and then reviewed again. |
| needs-testing | search | search | Pull requests which need manual testing. |
