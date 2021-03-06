Documentation Documentation
===========================

Doc Doc - Goose?
----------------

Here is some documentation about how this documentation is written. Feel free to pitch-in and improve things.

  1. Markdown - Much of this site is written in the [Markdown format](http://daringfireball.net/projects/markdown/syntax).

    Markdown source files are located in: [src/site/markdown](https://github.com/bhamail/pinexus/tree/master/src/site/markdown).
    
  2. Asciidoc - Some of this site is also written in the [Asciidoc format](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)
  
    Ascidoc source files are located in: [src/site/asciidoc](https://github.com/bhamail/pinexus/tree/master/src/site/asciidoc)
  
  3. You may also find some `README.md` files scattered around the source tree as well.


Doc Publishing
--------------

To deploy these docs to GH Pages, see: http://stephenc.github.io/wagon-gitsite/

 1. One time - create an empty `gh-pages` branch and push to github.
    
        $ git push
    
    or

        $ git push --set-upstream origin master
    
    then
    
        $ git pull
        $ git symbolic-ref HEAD refs/heads/gh-pages
        $ rm .git/index
        $ git clean -fdx
        $ echo "My GitHub Page" > index.html
        $ git add .
        $ git commit -a -m "First pages commit"
        $ git push origin gh-pages
        $ git checkout master
        
 2. Deploy site to github gh-pages.
  
        $ git checkout master
        $ mvn clean site-deploy

