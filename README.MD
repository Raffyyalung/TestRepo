README format
Drupal recommends the following README formatting:

Headings capitalized with an initial capital, following standard English sentence rules
Headings prefixed with #/##/### to indicate level of heading (h1/h2/h3) followed by a blank line
Project name is the first line of the document, and only level one heading (#)
Two lines prior to ##/### headings
No leading or trailing spaces
Bulleted lists denoted by dashes (-)
Nested lists indented with 4 spaces
Links should have a meaningful link text, for example:
[Drupal](https://www.drupal.org/) (i.e. not just the URL)
Text manually word-wrapped within around 80 cols
README sections
Drupal recommends the following README sections:

Project name and introduction (required)
Table of contents (optional)
Requirements (required)
Recommended modules (optional)
Installation (required, unless a separate INSTALL.md is provided)
Configuration (required)
Troubleshooting & FAQ (optional)
Maintainers (optional)
Project name and introduction
Start the README.md with the project name, and an introduction to the project. The project name is the only level one heading in the document. This must be the first line of the document and must be followed by one blank line.

The introduction summarizes the purpose and function of the project, and should be concise (a brief paragraph or two). This introduction may be the same as the first paragraph on the project page.

This section should include a link to the project page and issue queue. If the project is a sandbox, these links should go to the sandbox until promotion.

# Administration Menu

The Administration Menu module displays the entire administrative menu tree
(and most local tasks) in a drop-down menu, providing administrators one- or
two-click access to most pages.

For a full description of the module, visit the
[project page](https://www.drupal.org/project/admin_menu).

Submit bug reports and feature suggestions, or track changes in the
[issue queue](https://www.drupal.org/project/issues/admin_menu).
Table of contents (TOC)
TOCs are optional but appreciated for lengthy README files.

## Table of contents

- Requirements
- Recommended modules
- Installation
- Configuration
- Troubleshooting
- FAQ
- Maintainers
Requirements
The requirements section describes whether this project requires anything outside of Drupal core to work (modules, libraries, etc). List all requirements here, including those that follow indirectly from another module, etc. The idea is to inform the users about what is required, so that everything they need can be procured and included in advance of attempting to install the module. If there are no requirements, write "No special requirements".

## Requirements

This module requires the following modules:

- [Views](https://www.drupal.org/project/views)
- [Panels](https://www.drupal.org/project/panels)
## Requirements

This module requires no modules outside of Drupal core.
Recommended modules
The recommended modules section lists modules that are not required, but that may enhance the usefulness or user experience of your project. Make sure to describe the benefits of enabling these modules.

## Recommended modules

[Markdown filter](https://www.drupal.org/project/markdown): When enabled,
display of the project's README.md help will be rendered with markdown.
Installation
The installation section describes how to install the module. However, if the steps to install the module follow the standard instructions for Drupal 9, Drupal 7, Drupal 6/5, or a theme, don't reinvent the wheel — simply provide a link and explain in detail any steps that may diverge from these steps. Take special note of Drush integrations. In a case where many Drush commands are added, consider adding a section for Drush.

Consider replacing this section with a standalone INSTALL.md file if your installation instructions are especially complex.

## Installation

Install as you would normally install a contributed Drupal module. For further
information, see
[Installing Drupal Modules](https://www.drupal.org/docs/extending-drupal/installing-drupal-modules).
Configuration
The configuration section describes how to configure the module – including, but not limited to, permissions. This section is particularly important if the module requires additional configuration outside of the Drupal UI.

If the module has little or no configuration, you should use this space to explain how enabling/disabling the module will affect the site.

## Configuration

1. Enable the module at Administration > Extend.
1. When creating a new field on a content type or custom entity type, choose
   "Double Field" from the drop-down menu.
1. On the Field Settings form for the Double Field, define the two subfields
   as you would with any other field.
1. Optionally, on the "Edit" form for the Double Field, you may choose
   options for whether or not the subfields are "required".
## Configuration

The module has no menu or modifiable settings. There is no configuration. When
enabled, the module will prevent the links from appearing. To get the links
back, disable the module and clear caches.
Troubleshooting & FAQ
The Troubleshooting and FAQ sections address questions that are asked frequently in the issue queue. Outline common problems that people encounter along with solutions.

External links are acceptable if the steps are complex. However, maintainers should provide a summary since external links can become inactive.

## Troubleshooting

If the menu does not display, check the following:

- Are the "Access administration menu" and "Use the administration pages and
  help" permissions enabled for the appropriate roles?
- Does html.tpl.php of your theme output the `$page_bottom` variable?


## FAQ

**Q: I want to prevent robots from indexing my custom error pages by
setting the robots meta tag in the HTML head to "noindex".**

**A:** There is no need to. **Customerror** returns the correct HTTP
status codes (403 and 404). This will prevent robots from indexing the
error pages.



**Q: I want to customize the custom error template output.**

**A:** In your theme template folder for your site, copy the template
provided by the **Customerror** module
(i.e. `templates/customerror.html.twig`) and then make your
modifications there..

**Q: I want to have a different template for my 404 and 403 pages.**

**A:** Copy `customerror.html.twig` to
`customerror--404.html.twig` and `customerror--403.html.twig`. You
do not need a `customerror.html.twig` for this to work.
Maintainers
The maintainer section lists current project maintainers. The section can also list historical maintainers.

This section replaces any legacy, standalone MAINTAINERS.md file.

## Maintainers

- Daniel F. Kudwien - [sun](https://www.drupal.org/u/sun)
- Peter Wolanin - [pwolanin](https://www.drupal.org/u/pwolanin)
- Stefan M. Kudwien - [smk-ka](https://www.drupal.org/u/smk-ka)
- Dave Reid - [Dave Reid](https://www.drupal.org/u/dave-reid)
Changes from README.txt
Historically, the Drupal community used README.txt formatting. The Drupal project migrated README documentation to Markdown (#3192842: Make our README more welcoming by converting it into an "entrypoint" into the Drupal ecosystem).

Modules upgrading to Markdown formatting should adjust their README files to match Markdown features.

Headers in README.txt-files were all upper-cased to make them stand out, because the txt-format didn't have any other formatting tools. Markdown automatically transforms for example ## into h2, so it is recommended to use that method, for a more easily readable formatting. Headers should be capitalized with an initial capital, and not all upper-cased, using for example "Metatag", not "METATAG". The same for "CONTENTS OF THIS FILE", "INTRODUCTION", etc.

Advanced help module
Drupal site owners can install Advanced help to view README files.

Sample README
See the following modules for recommended README.md examples:

Gin Admin Theme README.md
Views GeoJSON README.md
Search API README.md
Project Browser README.md