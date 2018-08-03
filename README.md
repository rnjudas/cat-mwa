# Project Title

A simple Mediawiki Assessment.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to install the software and how to install them

```
Any operating system that supports:
Git
Vagrant
Virtual Box
```

### Installing

If you have the prerequisites all setup simply follow the steps below:

Clone the git repo.
```
git clone https://github.com/rnjudas/cat-mwa
```

Navigate to the local repo folder
```
cd ./cat-mwa
```

(Optional):
Edit the Vagrantfile if you would like to set your own private IP by changing the line as you see below.
```
vi Vagrantfile

[...]
config.vm.network "private_network", ip: "192.168.34.8"
[...]
```

## Deployment

Once you are satisfied that nothing needs to change, bring up the server:

```
vagrant up
```

Now just sit back and watch the screen.

Finally navigate to http://IP/mediawiki/index.php/Main_Page which would default to the below if you have not changed it:

```
http://192.168.34.8/mediawiki/index.php/Main_Page
```

## Built With

* [Ansible](https://www.ansible.com/) - The automation tool used
* [Vagrant](https://www.ansible.com/) - Portable virtual software maintainer
* [Virtualbox](https://www.virtualbox.org/wiki/VirtualBox) -  General-purpose full virtualizer for x86 hardware

## Contributing

Please read [CONTRIBUTING.md](https://github.com/rnjudas) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

* **Renaldo Maclons** - *Initial work* - [RNJudas](https://github.com/rnjudas)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Anyone who ever used ansible/vagrant/Linux
* Danie
* Google / Stackoverflow / Servervault
