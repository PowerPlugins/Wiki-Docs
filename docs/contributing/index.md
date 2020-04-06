[repo]: https://github.com/PowerPlugins/Plugins-Docs
[imgur]: https://imgur.com
[gfycat]: https://gfycat.com

# Contribute
Do you want to add a plugin, which doesn't has a documentation yet? Here's a small guide on how to add it.

## Styling
Before you start do we recommend to take a look at our [Styling Guide](contributing/styling-guide) to know all the details about what features we offer.

## Pages
Each plugin has its own folder under the `docs/plugins` directory to allow them to have separate pages.  
You can create as many pages for your plugin as you want, as long as you keep it within the same folder (`plugins/<your-plugin>`).  
To prevent any possible formatting issues will you need to follow these important parts:

1. Do **not** use any non-alphanummerical character in your folder or file name including spaces and underlines (`_`). Use dashes (`-`) as replacement for spaces (So `my plugin.md` becomes `my-plugin.md`)
2. Names of folders and files have to be all lowercase.
3. It's recommendet to create a `index.md` file which would be displayed first when connecting to the sub-page of the plugin (`/plugins/<your-plugin>`).
4. Put any images you want to use for your plugin under the `assets/img/plugins/` folder. Make sure to create a separate folder with the name of the plugin (while following point 1) to put all the images into.

## Adding pages to the mkdocs.yml
Now that you've created your files is it time to actually add them to the `mkdocs.yml` file, to tell MkDocs, where you can find those pages.

In the `mkdocs.yml` will you find a section called `nav` which acts as the navigation/list of MkDocs.  
To add your files, you first need to create a sub-directory under the `Plugins` one:

```yaml
nav:
  - Welcome: index.md
  - Contribute:
    - Contribute: contributing/index.md
    - Styling: contributing/styling-guide.md
  - Plugins:
    - Welcome: plugins/index.md
    # Imagine here to be any other plugins
    - Your Plugin:
```

!!! info "Note"
    We would appreciate it, if you could keep it ordered by alphabet (0-9 first, followed by A-Z).

Now that you have added it, is it time to add your pages.  
You can add them either by just providing the relative path (`- 'plugins/<your-plugin>/<page>.md'`) or by prefixing it with a name that would be displayed in the navigation on the left (`- The Page: plugins/<your-plugin>/<page>.md`).  
It's recommendet to name the pages, as you can use spaces and non-alphanummerical characters in it (Although last one isn't recommendet as it probably won't render well).

If you've done everything should the nav section look something similar to this:  

```yaml
nav:
  - Welcome: index.md
  - Contribute:
    - Contribute: contributing/index.md
    - Styling: contributing/styling-guide.md
  - Plugins:
    - Welcome: plugins/index.md
    # Imagine here to be any other plugins
    - Your Plugin:
      - Hello: plugins/your-plugin/index.md
      - About: plugins/your-plugin/about.md
```

## Create a Pull Request
You can now create a Pull Request towards the [Plugin-Docs repository][repo] to get it added (if everything is alright).

## Styling suggestions
Here are some styling suggestions for the files to keep them organized and simple

### Reference links
It's highly recommendet to use a reference link in your file.  
Reference links are links prefixed by a text within square brackets. (Example: `[text]: https://url.tld`)

These kind of links have some benefits:

- You only need to update a single instance of the URL and don't have to go through each one separately.
- You just need to provide `[text]` and Markdown will translate it to `text` containing the link.
- You can keep the links at a single place (i.e. on top of the page) for easier managing and updating.

### Image links
You can upload images to the repository, by creating a folder named after the plugin under the `assets/img/plugins/` directory.  
After you've uploaded your images can you reference them like this:  
```markdown
![image](/assets/img/plugins/<your-plugin>/<image>.<type>)
```

Please make sure to upload the images as either `.gif` or `.jpg` to save resources and storage space.  
You're allowed to use external sites for the images and use the respective URLs for them, but keep in mind that we might deny your PR if it uses a sketchy website for images.  
Below can you find a list of trusted sites for uploading and sharing images and gifs.

!!! info "Trusted sites"
    Note that this is by no means a complete list and that it might get updated from time to time.
    
    - [Imgur] - Supports images and gifs.
    - [GfyCat] - For gifs. Use the "gifs" share-option.

## Videos
MkDocs (And especially the Material Theme) allows us to directly implement Videos from sources like YouTube, which isn't possible for pages like GitHub Wikis.  
In order to display a video will you need to use the `<iframe>` option which most sites *should* provide.

!!! example "Video example"
    This is an example using the video "How to use SlimeWorldManager" found on YouTube.
	
	=== "Markdown/HTML"
	    ```html
		<iframe width="560" height="315" src="https://www.youtube.com/embed/FIA-oy-fx7A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
		```
	
	=== "Result"
	    <iframe width="560" height="315" src="https://www.youtube.com/embed/FIA-oy-fx7A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>