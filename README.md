# Github-cards for minimal mistakes and academic pages

This repo allows an easy github-cards integration, showing your repos or user information to your github page. 

## Usage
* Copy the full github-cards directory to your _assets_ folder (if you place it in other folder, make sure to change all text instances of _/assets/github-cards/_ to your desired path).
* Add to the __config.yml_ file the desired github repository names or users under github-repos like:
```yaml
github-repos:
  - name: pvjosue/LFMNet
  - name: pvjosue/pytorch_convNd
  - name: pvjosue/OpenCV-Spout
  - name: pvjosue
```
* Add the following code to the page under __pages_ where you would like to show your repos.
For example in _pages/cv.md
```javascript
{% if site.github-repos %}
  <h1>Repositories</h1>
  <div class="grid__wrapper">
    {% for repo in site.github-repos %}
      <div class="github-card" data-github="{{repo.name}}" data-width="300em" data-height="" data-theme="default"></div>
    {% endfor %}
  </div>
  <script src="/assets/github-cards/src/widget.js"></script>
{% endif %}
```
* Modify the variables `data-width`, `data-height` and `data-theme` (default or medium) from the previous script as it suits you.

## Result
You will see something similar to this in your page when using the _default_ theme:
![Grid of repos and user](output_example.png)

[Here](https://pvjosue.github.io) you can see it in action.

#### This repo was forked and modified from [github-cards](https://github.com/lepture/github-cards)
