NoCommitGitHook
===============

This is a git hook that will prevent commits if it finds //NOCOMMIT: anywhere in the staged code.

========================================================

Example:

  <pre>
  <?php
    $var = "Here is some random code and stuff";
    // NOCOMMIT: Don't commit this debug!!!
    var_dump("testing".$var);
  ?></pre>

When you try to commit this file, the commit will fail and show you the message "Don't commit this debug!!!"

========================================================

Installation:

To install this hook, copy the pre-commit file into your git templates/hooks directory.  On windows this is probably in "C:\Program Files (x86)\Git\share\git-core\templates\hooks".

Any new repositories will have use this hook.  To have this work on existing repositories you will need to run "git init" in the repository directory.  If you already have a pre-commit hook installed in that repo, it will not add it.  You will need to add it yourself
