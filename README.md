# Get your own gollom wiki onto OpenShift

This project is all about getting your own [gollum](https://github.com/github/gollum) wiki hosted on
Red Hat's [Openshift](https://openshift.redhat.com/app/). It's quite straight forward. Just sign up
for an OpenShift account and follow these instructions:

    $ git clone git://github.com/openshift/gollum-openshifted.git
    $ git remote rm origin
    $ rhc domain create -n <your-domain> -l <email>
    $ rhc app create -a <app> -t ruby-1.8 -l <email> --nogit
      <git-url>
    $ git remote add openshift <git-url>  
    $ git push -f openshift master
    
* \<your-domain\> - The domain name you want to use for your apps
* \<email\>       - The email you signed up with for OpenShift  
* \<password\>    - Your OpenShift password
* \<git-url\>     - The OpenShift git URL which you receive when creating the app	

Let me know if you have problems ...

Enjoy,

Hardy
