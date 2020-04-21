# PHP Welcome Page

This is an example PHP application you can use to test your OSEv3 environment.

Here is an example:
```
user@host$ oc new-app openshift/php~https://github.com/RedHatWorkshops/welcome-php
```

Things to keep in mind:
* `ose new-app` Creates a new application on OSE3
* `openshift/php` This tells OSEv3 to use the PHP image stream provided by OSE
* Provide the git URL for the project
  * Syntax is "imagestream~souce"

Once you created the app, start your build

```
user@host$ oc start-build welcome-php
```

Once the build completes; create and add your route:
```
user@host$ oc expose svc welcome-php
```

Scale up as you wish
```
user@host$ oc scale --replicas=3 dc/welcome-php
```

If you'd like to add another route (aka "alias"); then you need to specify a new name for it

```
user@host$ oc expose svc welcome-php --name=hello-openshift --hostname=hello-openshift.cloudapps.example.com
```





Openshift Workshops 
====

Voici une liste non exaustive des laboratoires disponibles pour démarrer ou monter la connaissance dans la plateforme Openshift. 

Workshops / Laboratoires 
----

**Openshift Basic Tutorials** - *tutoriels de Red Hat qui expliquent la base de la plateforme Openshift*

[https://developers.redhat.com/openshift/#assembly-field-sections-13455][1]

**Laboratoire Openshift version 3.11** - *Forge Gouvernementale* 

[https://gitlab.forge.gouv.qc.ca/cqen/okd/workshopv3/openshiftv3-workshop][2]

**Laboratoire Openshift version 4.1** - *Forge Gouvernementale*

[https://gitlab.forge.gouv.qc.ca/cqen/okd/les-travaux-pratiques-openshift][3]


Resources
----

**Openshift online** - *pour avoir un cluster personnel. Il faut un compte chez RedHad, puis l'abbonement du cluster est valide pour 60 jours, rénouvellables.* 

[https://www.openshift.com/products/online][r1]




**Instalation de l'outil `oc`**

[https://mirror.openshift.com/pub/openshift-v4/clients/oc/4.2/][r2]


**Portail d'apprentissage iteractive d'Openshift**

[https://learn.openshift.com/][r3]


**Téléchargement et instalation d'un cluster Openshift v4 provisionné sur la machile locale.**

[https://cloud.redhat.com/openshift/install/crc/installer-provisioned][r4]


[1]: https://developers.redhat.com/openshift/#assembly-field-sections-13455 "Openshift tutorials RedHat"
[2]: https://gitlab.forge.gouv.qc.ca/cqen/okd/workshopv3/openshiftv3-workshop "Labo v3 forge gouv"
[3]: https://gitlab.forge.gouv.qc.ca/cqen/okd/les-travaux-pratiques-openshift "Labo v4 forge gouv"

[r1]: https://www.openshift.com/products/online/
[r2]: https://mirror.openshift.com/pub/openshift-v4/clients/oc/4.2/
[r3]: https://learn.openshift.com/
[r4]: https://cloud.redhat.com/openshift/install/crc/installer-provisioned

