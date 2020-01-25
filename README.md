# Tech Talent Factory - DevOps Class 2020

This is the "archetype repository" for the students of Tech Talent Factory - DevOps Class 2020.

Into this repository will be saved the exercises done by the students during the class. The final assessment partially depends by the content and the usage of this repository.

## Usage

Students will have to fork this repository on our GitHub account, insert their data into the STUDENTS.md file and finally make a pull request of the updated STUDENTS.md file.

After that, the students will use this repository, their own fork, as a single repository for all their exercises. The teacher considers the students repository as **the only source of truth**, therefore no other file, exercise or implementation will be taken into consideration for the final assessment.

## Getting Started

- fork on GitHub
- clone the forked repository
- fill the STUDENTS.md file with their data
- commit the STUDENTS.md file
- push the STUDENTS.md file on remote repository
- make a new pull request to the "base repository"
- start working and enjoy

## vs-code usefull plugins

- Docker
- Vagrant (optional)

## Working Agreements

- libertà di lavorare da soli o in coppia (preferibilmente in coppia)
- le coppie sono durature e invariabili nel tempo
- la branch master contiene solo codice funzionante
- ogni esercizio deve essere in una cartella separata
- la branch master _può_ contenere il "work in progress"
- commit piccoli che permettano di ricostruire la storia
- uso libero delle branch per il "work in progress"
- messaggi di commit concisi, chiari ed esatti

> Put it before them briefly so they will read it, clearly so they will appreciate it, picturesquely so they will remember it and, above all, accurately so they will be guided by its light. Joseph Pulitzer

## Esercizi e Valutazione

Nella directory ```esercizi``` sono presenti i file necessari allo svolgimento degli stessi e per la precisione:
- _README.md_ file contenente il testo dell'esercizio
- _acceptance_test.sh_ file contenente i test di accettazione
- eventuali altri file utili all'esercizio specifico

I criteri di valutazione tengono conto del:
- contenuto della branch master
  - correttezza dello svolgimento dell'esercizio, cioè i test di accettazione dovrebber essere "verdi"
  - qualità del codice scritto e.g. rispetto delle buone pratiche e leggibilità
- l'uso delle branch e dei commit
  - commit piccoli che permettano di ricostruire la storia
  - messaggi di commit concisi, chiari ed esatti

## Vagrant
HashiCorp Vagrant provides the same, easy workflow regardless of your role as a developer, operator, or designer. It leverages a declarative configuration file which describes all your software requirements, packages, operating system configuration, users, and more.

More info at this [link](https://www.vagrantup.com/intro/index.html).

### Vagrant - Overview
in the _vagrant_ folder there is a file called ```Vagrantfile```. Inside, the configuration of the virtual machine (VM) that can be used to perform the exercises is described. In addition, there is a _bash_ file called ```provisioner.sh``` that is automatically executed during the creation of the VM and which has the purpose of installing the necessary software packages and making some configurations inside the newly created VM.

> :warning: WARNING: please change the values of ```user.name``` and ```user.email``` in ```provisioner.sh``` file and un-comment that lines!!!


### Vagrant - Usage
To use vagrant you need to open a terminal in the ```vagrant``` folder and type one of the commands below, the one that's right fo you :-)

| Name | Vagrant Command |
| ---- | --------------- |
| Up | vagrant up |
| Provision | vagrant provision |
| Suspend | vagrant suspend |
| Halt | vagrant halt |
| Reload | vagrant reload |
| Destroy | vagrant destroy |
| Status | vagrant status |
| Connect | vagrant ssh |

### Vagrant - Example of usage
In this example I show the commands to start and connect to the VM using _Vagrant_. Once connected to the VM you are in a fully functional, albeit minimal, GNU/Linux distribution. At the end of the work, remember to logout from the VM and turn it off.

Start VM and connect to it:
```bash
# you are on your pc
gianni@nolok ~/workspace/projects/ttf $ cd vagrant
gianni@nolok ~/workspace/projects/ttf/vagrant $ vagrant up
gianni@nolok ~/workspace/projects/ttf/vagrant $ vagrant ssh
# now you are connected to the VM and the next commands will be execute inside VM
alpine38:~$ 
```

At the end, you need to logout and shutdown the VM:
```bash
# remenber to logout from the VM
alpine38:~$ logout
# you are back on your pc
gianni@nolok ~/workspace/projects/ttf/vagrant $ vagrant halt
```

## License
This project is licensed under the GPL-v3 License - see the LICENSE.md file for details
