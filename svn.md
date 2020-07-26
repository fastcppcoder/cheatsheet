
# use vimdiff for svn diffs

    # bashrc
    alias svnvimdiff="svn diff --diff-cmd ~/bin/svnvimdiff.sh"
    alias svnvimdiffwhite="svn diff --diff-cmd ~/bin/svnvimdiff.sh"
    alias svndiff="svn diff --diff-cmd /usr/bin/diff --extensions 'unified -show-c-function' "


    # svnvimdiff.sh
    #!/bin/sh
    /usr/bin/vimdiff ${6} ${7}
    
    # svnvimdiffwhite.sh
    #!/bin/sh
    /usr/bin/vimdiff ${6} ${7} -c 'set diffopt+=iwhite'
