# blogs
This is Blog site for Panta Rhei.

## Initial local server
This site is built with [hugo](https://github.com/gohugoio/hugo), follow this [website](https://gohugo.io/installation/) to install hugo at first. Then, please initial or update the PaperMod theme, run the command `hugo server` to start the local server (at `http://localhost:1313/` by default). 

## Add content
Run the command to add a new post according to the `archetypes/default.md`
```bash
hugo new content content/docs/my-post.md
```

Add some content to the `my-post.md` file. Save the file, then start Hugo’s development server to view the site, which will contain draft posts.
```bash
hugo server --buildDrafts
# or
hugo server -D
```

Change the `draft: true` to `draft: false` if the drafts are ready to publish. Run the command to start Hugo server.
```bash
hugo server
```


## hugo-PaperMod theme
The [PaperMode](https://github.com/adityatelange/hugo-PaperMod) theme is imported with git submodule. To import it, run the following commands:
```bash
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
```

To update the theme to the latest version, run the following command:
```bash
git submodule update --init themes/PaperMod
# or
git submodule update --remote --merge
```