# about-me
This should be my personal site, assuming I have the will to complete it :D

# Notes to myself

## Hugo
1. Use this [example site](https://github.com/luizdepra/hugo-coder/tree/main/exampleSite) as a reference
2. I can also use a containerised [Hugo](https://hub.docker.com/r/klakegg/hugo)
3. An interesting [blogpost](https://levelup.gitconnected.com/build-a-personal-website-with-github-pages-and-hugo-6c68592204c7) is here

### Some commands
- Create site content structure: `hugo new site <path>`
- Attach a theme to the structure: `cd <path> ; git submodule add https://github.com/luizdepra/hugo-coder.git themes/hugo-coder`
- Serve the site locally at `localhost:1313`: `hugo server`

## CV from YAML data
1. use `gomplate`
    - prepare a template with `go` template syntax
    - run `gomplate -f <htmlTemplateFile> -o <htmlOutputFile> -d <key>=<yamlDataFile>`
2. use `wkhtmltopdf <htmlFile> <pdfFile>`
3. CI/CD to integrate gomplate and wkhtmltopdf
