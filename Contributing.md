# Contributing to Haystack Tutorials

A contribution to Haystack tutorials may be anything from a suggestion for edits or a new tutorial request to adding a new tutorial or editing an existing one yourself.

To make a request for a new tutorial or to suggest edits and fixes, submit an issue and choose the appropriate type:

- **Bug  report:** For any edit suggestions or bug reports.

- **New Tutorial Request 📓:** To suggest that we create a new tutorial.

## Contributing Edits or New Tutorials

All of the Haystack tutorials live in the `tutorials` folder in this repo. Each tutorial is an interactive `.ipynb` file that you can run on Google Colab, too. For each `.ipynb` file, we also generate a Markdown file to accompany it.

Here's what you need to do to add or edit tutorials 👇:

1. If you're creating a new tutorial, follow the [naming convention](#naming-convention-for-file-names) for file names.
2. Edit an existing tutorial or create a new one in the `/tutorials` folder by editing or creating `.ipynb` files.
3. Update the `markdowns` folder to reflect the changes:
    - Install requirements with `pip install -r scripts/requirements.txt`.
    - Run `python scripts/generate_markdowns.py`. This generates or updates the relevant markdown file in `/markdowns`.
4. Create a pull request.
5. Wait for the [CI](#ci-continuous-integration) checks to pass.
   These checks pass if the relevant markdown files are created.
6. Update the [README](./README.md), if necessary.
6. Wait for a review and merge 🎉. Thank you for contributing 💙.



# Continuous Integration (CI)

We use a GitHub action for our Continuous Integration tasks. This means that as soon as you open a PR, GitHub starts executing some workflows on your code. Here, the workflow checks that you've generated the required `.md` files for the tutorials you've edited or created.

If all goes well, at the bottom of your PR page, you should see something like this, where all checks are green.

![](https://raw.githubusercontent.com/deepset-ai/haystack/main/docs/img/ci-success.png)

If you see some red checks, then something didn't work and you need to take some action. The most likely reason is that the `.md` file accompanying the `.ipynb` tutorial hasn't been updated or created. You can try to run repeat step 3 in [Contributing to Haystack Tutorials](#contributing-to-haystack-tutorials).

# Naming Convention for File Names

- Each tutorial name starts with a number. If you create a new tutorial, its name should start with the number following the last tutorial. 
- Separate words in the title with an `_` underscore.
- Use a short descriptive name for the filename, for example: *22_creating_a_summarizer_pipeline*.
- Generated markdown files only have the number of the tutorial (use the `scripts/generate_markdowns.py` script for this).