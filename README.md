# Zqjs
A simple CLI for creating your projects

## Getting Started

### Install

```shell
npm add zqjs -g
```
### Usage

```
  Usage: zqjs <command>


  Commands:

    add|a      Add a new template
    list|l     List all the templates
    init|i     Generate a new project
    delete|d   Delete a template

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```

### Commands
#### add | a
This command would help you to add a new template to the `templates.json`, which will be used by `Zqjs` to generate projects.
```
$ zqjs add

? Set the custom name of the template: react
? Owner/name of the template: BooheeFE/react-template
? Branch of the template: master
┌───────────────┬─────────────────────────┬────────┐
│ Template Name │ Owner/Name              │ Branch │
├───────────────┼─────────────────────────┼────────┤
│ react         │ BooheeFE/react-template │ master │
└───────────────┴─────────────────────────┴────────┘
✔ New template has been added successfully!
```
`Zqjs` use [download-git-repo](https://github.com/flipxfx/download-git-repo) to down load git repos. After answering 3 questions, you'll add a new template to `Zqjs`.

### list | l
It shows you the templates list.
```
$ zqjs list

┌───────────────┬─────────────────────────┬────────┐
│ Template Name │ Owner/Name              │ Branch │
├───────────────┼─────────────────────────┼────────┤
│ react         │ BooheeFE/react-template │ master │
├───────────────┼─────────────────────────┼────────┤
│ vue           │ BooheeFE/vue-template   │ master │
└───────────────┴─────────────────────────┴────────┘
```

### init | i
After adding new templates, you could use this command to generate your own project by choosing template.
```
$ zqjs init

? Template name: react
? Project name: boohee
? Where to init the project? ./
⠹ Downloading template...

New project has been initialized successfully!
```

### delete | d
To delete a template, you could use this command:
```
$ zqjs delete

? Which template you want to delete? vue
┌───────────────┬─────────────────────────┬────────┐
│ Template Name │ Owner/Name              │ Branch │
├───────────────┼─────────────────────────┼────────┤
│ react         │ BooheeFE/react-template │ master │
└───────────────┴─────────────────────────┴────────┘
✔ Template has been deleted successfully
```
## Template
The most important part of Zqjs is `template`. All templates' infomation were list in the `templates.json`.
A template means a project sample, which has a simple or complex file structure.

You can create your own templates repository, and push your templates in different branches. All you need to do then is to add the templates into Zqjs's `templates.json`.

## License

[**The MIT License**](LICENSE).

