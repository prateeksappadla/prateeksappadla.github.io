---
layout : post 
title: Guide to creating your own personal webiste using Jekyll and Bootstrap 
tags: [jekyll, bootstrap]
---

<p>
I used an existing Bootsrap theme adapted to Jekyll available at startbootstrap.com . 

Alternatively, you could create a new jekyll project and add the bootstrap files to the jekyll directory structure. 

</p>


<p>
	The liquid tag {% raw %}{% include file.ext %}{% endraw %} can be used to include the partial in _includes/file.ext.
</p>

<p>
YAML Front Matter
Is a directive for Jekyll to process the file as a special file. The YAML front matter is at the top of the page and is placed 
between triple dashed lines (---). 

Between the triple dashed lines, we can set predefined variables or create new variables. These variables can then be accessed in liquid tags.

ProTip: Don't repeat yourself
If you don't want to repeat your frequently used front matter variables over and over, just define defaults for them and only override them where necessary (or not at all). This works both for predefined and custom variables. 
</p>

<p>
	Creating Post Files

	Add a new file in the _posts/ directory. Jekyll requires that the files be named in the following format 
	"YYYY-MM-DD-title.md". eg. 2011-12-31-new-years-eve-is-awesome.md

	All Blog post files must begin with YAML front matter.
</p>

Highlighting code snippetsPermalink

Jekyll also has built-in support for syntax highlighting of code snippets using either Pygments or Rouge, and including a code snippet in any post is easy. Just use the dedicated Liquid tag as follows:

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}

Escaping liquid tags
if we wrap any thing in posts with {% raw %} and {% endraw %} tags, they will escape from formatting in Jekyll.