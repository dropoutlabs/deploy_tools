# deploy_tools

How to publish open source changes to GitHub

merge (some?) changes

    $ gco upstream
    $ git merge master

or

    $ git cherry-pick ...

then

    $ git push -u upstream upstream:master

## buildbots.yml

Buildbot deployment

Install dopy system wide to localhost

    $ sudo -H pip3.6 install -e git+https://github.com/ysz/dopy.git@42a3170f01841ebaa2a11fd96f2ffe2d2e50a49e#egg=dopy

In virtualenv `foo` run the playbook, like this:

    (foo) deploy_tools $ ansible-playbook -i hosts buildbots.yml

