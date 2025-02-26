# ![](https://avatars1.githubusercontent.com/u/8237355?v=2&s=50) Grav Skeleton T2B5

This is the Grav T2B5 Skeleton. It includes a copy of the Grav, configured to use the [T2B5 theme](https://github.com/stom66/grav-theme-t2b5) and is provided with sample pages, images, and relevant config files.

Using this Skeleton is the recommended way to use the theme. For downloads, see the [Latest Releases](https://github.com/stom66/grav-skeleton-t2b5/releases/latest).

## Features

-   Mobile-first, responsive Layout via Bootstrap 5.3
-   25 selectable Bootswatch themes
-   Icon packs: FontAwesome
-   Numerous customizable options through admin interface
-   A load of SEO meta tags, including OpenGraph, TwitterCard

#### Included Plugins

-   [Google Analytics](https://github.com/escopecz/grav-ganalytics)
-   [Color Tools](https://github.com/trilbymedia/grav-plugin-color-tools/)

## Installation

-   Download the `grav-skeleton-*.zip` file from the [Latest Releases](https://github.com/stom66/grav-skeleton-t2b5/releases/latest) section.
    -   Using the version with the Admin panel makes it much easier to configure the theme.
-   Unzip it somewhere accessible
-   Run the following in a terminal:

    ```bash
    bin/gpm selfupgrade -f
    bin/gpm update
    ```

Test the site works as expected, and you can browse the default content.

-   Run a local dev server with:

    ```bash
    bin/grav server
    ```

## Post-install steps

Some additional steps you can take after installing the theme to get the most from it:

-   Update `/user/config/site.yaml`, via _Admin -> Configuration -> Site_
    -   Set the `Site Title`
    -   Set the default `Author`, `Email`
    -   Update the Metadata `description` property
    -   Update the Metadata `keywords` property
-   Customise `/user/config/themes/t2b5.yaml` via _Admin -> Themes -> T2B5_
-   Choose an optional Bootswatch theme in the settings
-   Add `Sitemap: https://example.com/sitemap.xml` to your `robots.txt` file
-   Upload your [favicons](#favicons)
-   Configure the Plugin: Google Analytics
    -   Set your Tracking ID
    -   Enable the plugin

## Documentation

The full Grav documentation can be found from [learn.getgrav.org](https://learn.getgrav.org).

Theme documentation can be found in the [grav-theme-t2b5](https://github.com/stom66/grav-theme-t2b5) repository.

```

```
