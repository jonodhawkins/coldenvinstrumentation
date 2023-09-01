# CryoSkills README
This README file outlines how to modify text content for the various pages on this site.
It does not describe the HTML layout of each page.

**Todo** Add description of HTML pages in separate document.

### Key Files to Edit Site Content


## Navigation Menu
The navigation menu is configured with a YAML file in `_data/nav.yml`.

Each item of the YAML tree is made up of the following structure:

```YAML
- name: [page name]
  link: path/from/root.md
```

Adding new items to `_data/nav.yml` will modify the navigation bar at the top of each page accordingly.
The order of the items is determined by the order in which they are written in the YAML file.

## About Page
**To modify content in the About page, you will need to edit the Markdown file located in** `_includes/about/about.md`. 

The file is formatted using [Markdown](https://www.markdownguide.org/basic-syntax/).
It is possible to embed HTML within the Markdown file if more control over the content is required.

### Key Dates Table
The table containing information of the key dates is generated from the `_data/key_dates.yml` YAML file.
Formatting of the table is controlled by `_includes/about/key_dates_table.html`.

**To modify the key dates table, you will need to edit** `_data/key_dates.yml`

Each key date is listed with a `short_date` (used when viewed on a narrow screen), `long_date` (used when viewed on a wide screen) and `event` field.  For example

```YAML
- short_date: MM/DD/YYYY
  long_date: Day Month Year
  event: My new test event
```

## Apply Page
**To modify content in the Apply page, you will need to edit the Markdown files located in** `_includes/apply/` and the configuration file in `_data/apply_subpages.yml`

To update the title of one of the application sub-pages, edit the `title` parameter of an item in `_data/apply_subpages.yml`, i.e.

```YAML
- url: apply_subpage_file.md
  link: newpage
  title: My new apply subpage title!
```

The `url` parameter in `_data/apply_subpages.md` is relative to the `_includes/apply` folder.
In order to use the page `_includes/apply/my_new_subpage.md` as a new subpage, the `url` parameter would be set to

```YAML
- url: my_new_subpage.md
  link: newpage
  title: My new subpage!
```

The `link` parameter sets the HTML anchor (i.e. `#eligibility` or `#data`) that can be used to link to each subpage externally. 
For example, to link to the `#eligibility` page externally, one could use the URL [cryoskills.com/apply.html#eligiblity](cryoskills.com/apply.html#eligiblity).

Each subpage is formatted using [Markdown](https://www.markdownguide.org/basic-syntax/).