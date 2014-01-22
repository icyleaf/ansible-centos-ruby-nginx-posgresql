# Ansbile deploy Centos with Ruby + Nginx + Postgresql

ansible directory layout based on [Ansible Best
Practices](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&ved=0CCwQFjAA&url=%68%74%74%70%3a%2f%2f%64%6f%63%73%2e%61%6e%73%69%62%6c%65%2e%63%6f%6d%2f%70%6c%61%79%62%6f%6f%6b%73%5f%62%65%73%74%5f%70%72%61%63%74%69%63%65%73%2e%68%74%6d%6c&ei=R2vfUpfhNoiciAe-z4CIAg&usg=AFQjCNEmMvyxmIayrLUjWJa4HFebs03QOg&sig2=cK5iNlmyCJujnZ7KyAErFQ).

## Available Envs

* stage ([vagrant](http://www.vagrantup.com/) + [CentOS
  box](https://github.com/2creatives/vagrant-centos/releases))
* production (any server)

## Available Playbooks(roles)

* centos (common)
* vim + vundle + bundles
* zsh + oh-my-zsh
* nginx
* ruby 2.1
* postgresql 9.3

## Configure

### stage

Enable debug mode, change `Vagrantfile`:

    ansible.verbose = 'vvvv'

### production

Replace your server ip address (or domain) in `ansible/production`

    [production]
    10.10.10.10

## Deploy it!

    $ ansible-playbook -i production site.yml
