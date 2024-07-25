# [SEED Platform Documentation Website](https://seed-platform.org/)

Documentation website for the SEED Platform.

This site was generated and deployed using mkdocs.

## Updating Documention

* Install Python and PIP
* Install mkdocs `pip install -r requirements.txt`
* Create a new branch and update documentation
* Serve mkdocs website locally by calling `mkdocs serve`

## Updating Documentation via GitHub interface

* Create a new branch by clicking the dropdown to change branches on the repository's main page and entering a new branch name in the input box.
* Ensure that new branch is active using the same dropdown, and make documentation changes as desired by following the next steps below.

Note: Each page on the [website](https://seed-platform.org/) corresponds to a file within the `docs` subdirectory.

* Use `mkdocs.yml` as a guide for both identifying which file to update if updating existing documentation or to create new pages by adding new entries.
* If updating existing documentation, open the corresponding file in the GitHub interface and click on the pencil icon towards the top right of the file.
* If creating a new page, after you've created a new entry within `mkdocs.yml`, navigate to the appropriate directory within the `docs` subdirectory, click "Add file" at the top right to "Create new file".
* Whether you're creating a new file or editing an existing one, the current page should allow you to edit the file contents and preview your changes.
* Once changes are made as desired, add a commit message and optional description, choose "Commit directly to `<your-branch-name>` branch", and click "Commit changes".
* Repeat this for desired files. Reminder that adding new pages will likely require that the `mkdocs.yml` is updated to include a new entry pointing to a newly created `.md` file in the `docs` directory.
* Once you've modified all the desired files, open a Pull Request (PR) by navigating back to the repository's main page, ensuring your new branch is currently active, and clicking "Pull request" or "Compare & pull request".
* On the next page, add relevant information, tag appropriate reviewers, modify as otherwise needed, and finally, click "Create pull request".
* After the updated content has been reviewed, a site administrator will build and release the website at which point your changes will be live.
For any issues, please reach out to Katherine Fleming.

## Releasing New Documentation
* Create a pull request into the `main` branch
* The PR will automatically deploy when merging to `main`. 
    * If a manual deploy is needed then run `mkdocs gh-deploy`

## Markdown Examples

### Collapsible Sections
To make a section collapsible, you have to remove the `#`s before the section name and replace them with three `?`s. Additionally, you have to add the word `note` and put quotation marks around the section title. For example, change `### Collapsible Sections` to `??? note "Collapsible Sections"`. Finally, the remaining content in that section needs to be indented. See below for an example block of markdown.

```markdown
??? note "Collapsible Sections"
    This is the content that is inside the collapsible section.
```

### Image Optimization
Install [pngquant](https://lib.rs/install/pngquant). Once installed run the following commands (these were tested on MacOS):

```BASH
pngquant docs/images/*.png --ext=.png --force
```

```BASH
pngquant docs/images/new/*.png --ext=.png --force
```

```BASH
pngquant docs/images/release_notes/*.png --ext=.png --force
```
