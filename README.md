# Documentation Theme for Jekyll
This is a fork of the [Documentation Theme Jekyll](https://github.com/tomjoht/documentation-theme-jekyll) repo, with a few modifications to make it accessible as a remote_theme in GitHub Pages, such as moving the `images`, `css` and `js` directories to the `assets` directory so they are packaged with the theme

## Usage
add the following line to your _config.yml

```yaml
remote_theme: read-automation/documentation-theme-jekyll
```

To add a `copy` button to a code snippet, add the following line above the code section

```
{% include code_header.html %}
```

To modify the sidebar, the following config shows how to add links, folders and subfolders
```yaml
entries:
  - product: Vehicles
    folders:
      - title: Cars
        folderitems:
          - title: Car Overview
            url: car_overview.html
          - subfolder:
              title: Luxury
              subfolderitems:
                - title: Lexus
                  url: /lexus.html
                - title: Tesla
                  url: /tesla.html
          - subfolder:
              title: Sports
              subfolderitems:
                - title: Ferarri
                  url: /ferarri.html
      - title: Trucks
        folderitems:
          - title: Utility
            url: /utility_trucks.html
          - title: Semi
            url: /semitrucks.html
```

See [upstream](https://github.com/tomjoht/documentation-theme-jekyll) for additional usage instructions

## Changes from the fork
Added ability to show copy button with code snippets (see above)

Refactored how to declare the sidebar (see above)
