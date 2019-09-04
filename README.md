
# Instructions

Use this repo. Copy your files from the previous homework into this repo, making any improvements you need. (Yes, I know this isn't the best way to do version control.) Make sure that you don't accidentally copy the `.git` folder over when moving files.

## Launch Docker
Using the Docker config files in this repo, launch Docker and view your new web site. Practice this, as we'll be doing it often.

## `.dockerignore` File
Read the following [explaition of the `.dockerignore` file](https://blog.codeship.com/leveraging-the-dockerignore-file-to-create-smaller-images/)
Create a `.dockerignore` file with at least the following. Be able to explain what each line does.

```
.*
docker-compose.yml
*.md
```

## Using Docker
When in this directory, use `docker-compose build` to build this docker image.

After building, use `docker-compose up` from the project directory to run the container.

After running this image container, the web page should be visible at http://localhost:8080/ (If you're using Docker Tools because you're on Windows 7, it may be slightly different.)

The file `docker-compose.yml` maps the container's port 80 (default web port) to
the host's (that's your machine's) port 8080 with the `ports` command.

The `volumes` command in `docker-compose.yml` maps the your folder `app` to the
container's `\srv\app\` folder. Changes made in one place will be made in the
 other.

 The key combo `ctrl-C` will kill the container.

## A simple Javascript
Add a script to your project to make the table sortable (on your page with the table).

You may use any table sort script on the web. Here are two to get your search started:

* http://tristen.ca/tablesort/demo/
* https://github.hubspot.com/sortable/docs/welcome/ (I think I like this one better.)

The ideal script "just works", perhaps with simply adding only a class to your table.
