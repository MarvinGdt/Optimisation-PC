# Optimiser son PC et Windows 10 sans risque

Dans ce github, j'ai compilé plusieurs tutos, guides de différentes personnes. Les trouvailles, tutos appartiennent aux personnes qui ont passés du temps à faire toutes ces recherches.
 
![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`CAPETLEVRAI`](https://www.twitter.com/capetlevrai)

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`PIWI`](https://www.twitter.com/piwielle) + [`GUIDE`](https://piwielle.github.io/oui)

A noter qu'il y a probablement du copier/coller venant des sources, c'est normal car c'est si bien expliqué que j'ai préféré laisser tel quel.

# DISCLAIMER

Avant de commencer ce guide, je tiens à faire quelques “disclaimer” sur ce qui sera expliqué dans ce manuel d’optimisation : 

Tous les fichiers nécessaires, pour le suivi de ce guide, seront disponibles directement via ce dernier au fur et à mesure des chapitres. 

Je ne parlerai pas d’overclocking processeur et RAM durant ce guide. Mais je vous redirigerai vers une playlist de tuto qui explique les bases et quoi faire, si vous voulez vous y lancer.

Pour finir, je ne serai en aucun cas responsable de tout dommage, défaut ou mauvaise manipulation de votre part. Ce guide est rédigé par mes soins après plusieurs tests de ce que j’en ai tiré dans mes recherches et les tutos que j’ai suivis. 

NE FAITES PAS CES MANIPULATIONS SUR PC PORTABLE !!! 

JE NE FOURNIRAI PAS DE SUPPORT TECHNIQUE, VOUS ÊTES SEUL MAÎTRE DE VOS RESPONSABILITÉS ! LISEZ ATTENTIVEMENT LE GUIDE PAR CHAPITRE ET PRENEZ VOTRE TEMPS ! 

J’espère que ce guide vous sera utile, j’y ai mis du temps, des recherches, j’essaie de tout centraliser dans ce guide en français et j’essaie de simplifier au maximum les étapes afin que tous ces réglages vous soient accessibles ! 

## Optimisation du BIOS

Avant d’entamer l’optimisation de Windows, il est préférable que vous ayez un bios bien réglé afin de pouvoir profiter du plein potentiel de votre ordinateur. 
Ces optimisations sont utiles, nous ne rentrerons pas dans les détails pour l’overclocking, il existe beaucoup de site qui peuvent vous y guider de manière très explicite et complète. Je vous laisse faire vos recherches à ce sujet. 
Ci-dessous, je mets les guides vidéos des cartes mères pour AMD et Intel en brutes avec toutes les explications pour effectuer les réglages. S’il vous manque une option qui n’est pas disponible dans votre bios, passez à la suivante, faites le plus de réglage que vous pouvez en suivant le guide. 

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`OPTIMISER SON BIOS AMD - CAPET`](https://www.youtube.com/watch?v=BXpEE3Qz4X4&t)

-> Dans l'idéal, pour la partie AMD, laissez le SMT en "Auto", quelques personnes ont eu des soucis de stabilité en ayant désactiver le SMT (HyperThreading pour AMD). 

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`OPTIMISER SON BIOS INTEL - CAPET`](https://www.youtube.com/watch?v=xSjLnO5VZEY)

-> Laissez également l'HyperThreading sur les CPU Intel. En effet, la majorité des jeux vont bien gérer l'HT et, pour certains jeux, cela fait gagner des performences. Donc laissez activé.

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`OVERCLOCKING CPU/RAM - CAPET`](https://www.youtube.com/playlist?list=PL96Ozk0v-00PNjvTPTvpMlT0sMGZvAXLg)

-> Cette étape est OPTIONNELLE. Vous n'êtes pas obligé de faire cette partie si vous n'êtes pas serein. Je la mets pour les plus téméraires.

## Installation de Windows et de vos Drivers

**Note :** Je préconise de partir sur un formatage complet de votre PC afin que tout ce guide se passe sans problème.

Pour ce faire, je vous redirige vers ce tuto très simple de TopAchat afin de pouvoir préparer votre clé USB bootable, installer Windows. 

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`[TUTO] Installer Windows 10 & Tes Drivers - TopAchat [FR]`](https://www.youtube.com/watch?v=uHOP4UbEGug)

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`DRIVER NVIDIA`](https://www.nvidia.com/Download/Find.aspx?lang=fr)

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`DRIVER AMD`](https://www.amd.com/fr/graphics/radeon-rx-graphics)

## Désactivation des drivers automatiques & Tweaks Regedit

Une fois que Windows sera installé, on se retrouve sur le bureau (avec une résolution très faible, ce qui est normal, la résolution normale viendra quand on aura installé les drivers de la carte graphique). La première chose qu’on va faire, c’est désactiver l’installation automatique des drivers de Windows. Pour ce faire, je vous propose de suivre la vidéo suivante :

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`Désactiver l'installation automatique des drivers de Windows Update`](https://www.youtube.com/watch?v=IMmNS6yAK4g)

Les commandes (à lancer dans CMD en administrateur) : 

`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\DriverSearching" /v SearchOrderConfig /t REG_DWORD /d 00000000 /f`

Une fois les drivers de Windows désactivés, vous devez impérativement redémarrer le PC. Une fois que c’est fait, vous pouvez rebrancher internet
Reboot le PC maintenant vous permettra d’avoir accès à internet, et donc de copier/coller les commandes CMD suivantes (si vous les avez pas sauvegardé avant l’install sur un fichier texte dans une clé USB)
Tant qu’on est à faire des changements dans regedit, je vous propose quelques petits tweaks basiques, qui vont légèrement améliorer les performances de votre PC, mais sans aucun problème de compatibilité, ou risque pour votre PC. La vidéo qui vous donnera des explications et du contexte est la suivante (recommandée).

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`Quelques tweaks regedit (basiques)`](https://www.youtube.com/watch?v=X4AVdnHFn_E)

Et la liste des tweaks proposés par Piwi dans sa vidéo (à rentrer dans CMD en admin, encore une fois) : 

**=> Désactiver Cortana :** 

`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v AllowCortana /t REG_DWORD /d 00000000 /f`

**=> Désactiver la sortie d'hibernation :** 

`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Power" /v HiberbootEnabled /t REG_DWORD /d 00000000 /f`

**=> Désactiver la combinaison de touche Win+Tab :** 

`REG ADD "HKCU\Keyboard Layout\toggle" /v "Language Hotkey" /t REG_SZ /d 3 /f`

**=> Désactiver Aero Shake :** 

`REG ADD "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v DisallowShaking /t REG_DWORD /d 00000001 /f`

**=> SUPPRIMER l'hibernation :** (à faire si vous avez désactivé la sortie d'hibernation)

`powercfg -h off`

**=> Vérifier le trim du SSD :** 

`fsutil behavior set DisableDeleteNotify 0`

**=> Garanti 90% des ressources aux tâches principales :** 

`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v SystemResponsiveness /t REG_DWORD /d 00000010 /f`

>QUELQUES COMMANDES BONUS : 
>
>Supprimer 3D Object de l'explorateur de fichier
>
>`REG DELETE "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\MyComputer\NameSpace\{0DB7E03F-FC29-4DC6-9020-FF41B59E513A}"`
>
>`REG DELETE "HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Explorer\MyComputer\NameSpace\{0DB7E03F-FC29-4DC6-9020-FF41B59E513A}"`


>Désactiver "Applications récemments ajoutés" du menu Démarrer
>
>`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Explorer" /v HideRecentlyAddedApps /t REG_DWORD /d 00000001 /f`
>
>`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer" /v HideRecentlyAddedApps /t REG_DWORD /d 00000001 /f`


>Screen snip sur la touche "impr écran"
>
>`REG ADD "HKEY_CURRENT_USER\Control Panel\Keyboard" /v PrintScreenKeyForSnippingEnabled /t REG_DWORD /d 00000001 /f`


>Ouvrir l'explorateur windows vous dirige à "Ce PC"
>
>`REG ADD "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v LaunchTo /t REG_DWORD /d 00000001 /f`


>Afficher les extensions des fichiers connus
>
>`REG ADD "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v HideFileExt /t REG_DWORD /d 00000000 /f`


>Désactiver la précision de la souris
>
>`REG ADD "HKEY_CURRENT_USER\Control Panel\Mouse" /v MouseSpeed /t REG_SZ /d 0 /f`
>
>`REG ADD "HKEY_CURRENT_USER\Control Panel\Mouse" /v MouseThreshold1 /t REG_SZ /d 0 /f`
>
>`REG ADD "HKEY_CURRENT_USER\Control Panel\Mouse" /v MouseThreshold2 /t REG_SZ /d 0 /f`


>Désactiver le mode veille
>
>`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FlyoutMenuSettings" /v ShowSleepOption /t REG_DWORD /d 00000000 /f`


>Désactiver le verrouillage de session
>
>`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FlyoutMenuSettings" /v ShowLockOption /t REG_DWORD /d 00000000 /f`


>Qualité du fond d'écran à 100%
>
>`REG ADD "HKEY_CURRENT_USER\Control Panel\Desktop" /v JPEGImportQuality /t REG_DWORD /d 00000100 /f`


>Délai du menu
>
>`REG ADD "HKEY_CURRENT_USER\Control Panel\Desktop" /v MenuShowDelay /t REG_SZ /d 0 /f`


>Désactiver le Power Throttling
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerThrottling" /v PowerThrottlingOff /t REG_DWORD /d 00000001 /f`


>Changer la taille des miniatures de la barre des tâches (très gros)
>
>`REG ADD "HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Taskband" /v MaxThumbSizePx /t REG_DWORD /d 000001f4 /f`


>Désactiver le texte " - raccourci"
>
>`REG ADD "HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer" /v link /t REG_BINARY /d 00000000 /f`


>Afficher les secondes sur l'horloge de la barre des tâches
>
>`REG ADD "HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v ShowSecondsInSystemClock /t REG_DWORD /d 00000001 /f`


> Services Google Chrome (désactive les mises à jour automatiques)
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\GoogleChromeElevationService" /v Start /t REG_DWORD /d 00000004 /f`
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\gupdate" /v Start /t REG_DWORD /d 00000004 /f`
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\gupdatem" /v Start /t REG_DWORD /d 00000003 /f`


>Services Microsoft Edge (désactive les mises à jour automatiques)
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\MicrosoftEdgeElevationService" /v Start /t REG_DWORD /d 00000004 /f`
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\edgeupdate" /v Start /t REG_DWORD /d 00000004 /f`
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\edgeupdatem" /v Start /t REG_DWORD /d 00000003 /f`

>Services Brave Browser (désactive les mises à jour automatiques)
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\brave" /v Start /t REG_DWORD /d 00000004 /f`
>
>`REG ADD "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\bravem" /v Start /t REG_DWORD /d 00000003 /f`

## Mises à jour de Windows

Une fois tous nos drivers à jour, et avant d’entamer la suite des réglages de Windows, on va vérifier les éventuelles mises à jour. 
On le fait maintenant, parce que certaines grosses mises à jour peuvent réinitialiser certains paramètres de windows, ça nous évitera de faire les réglages 2 fois. 
Il suffit d’aller dans les options de windows, cliquer sur windows update, et faire une recherche de mises à jour. Une fois qu’elles ont été téléchargées et installées, redémarrer le PC. 
Une fois le PC redémarré, refaites une vérification de mise à jour. Des fois, le fait d’avoir fait une màj va débloquer l’installation d’autres màj, d’ou le fait de devoir faire la vérification deux fois de suite. 
Si il y a de nouvelles mises à jour, répéter l’opération, jusqu’à avoir windows à jour.

## Paramètres de Windows

Il suffit simplement de se promener dans les paramètres de Windows et de désactiver ce qui ne vous est pas nécessaire. 

Si vous avez besoin d'aide, voici une vidéo qui explique l'ensemble des paramètres : 

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`Paramètres Windows`](https://www.youtube.com/watch?v=DP0e0xTk0Ck)

## W10Privacy

J'utilise ce logiciel pour automatiser les réglages des paramètres Windows. Simple et clair, il suffit de lire les options avant de cocher. 
Si vous rencontrez un soucis, vous pourrez décocher l'option qui vous pose problème.

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`W10Privacy (et d'autres logiciels de "vie privée"`](https://www.youtube.com/watch?v=oPUJThkVmXI)

## Mode MSI

Explication et utilité du mode MSI se trouvent dans la vidéo suivante :

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`MSI Mode`](https://youtu.be/eydeMfLlIsA)

[`Si vous voulez plus d'information sur ce qu'est le mode MSI`](https://forum.malekal.com/viewtopic.php?t=62058) et [`télécharger MSI Utility`]( https://forums.guru3d.com/threads/windows-line-based-vs-message-signaled-based-interrupts-msi-tool.378044/)

## Mode de gestion d'alimentation

Un réglage important que vous pouvez faire sur votre PC est de changer le mode d'alimentation.
Pour installer le mode "Performances Optimales" de Windows, lancez le CMD en administrateur et coller cette ligne : `powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61`.

Ensuite, allez l'appliquer dans les réglages de gestion d'alimentation.

Voici une vidéo explicative sur le mode d'alimentation : 

![#f03c15](http://placehold.it/15/f03c15/000000?text=+) [`Mode de gestion d'alimentation`](https://youtu.be/SAlqNxr1eVY)

## Installer le Visual C++ Package et DirectX

DirectX à télécharger ici : [`DirectX`](https://www.microsoft.com/fr-FR/download/details.aspx?id=35) 

Visual C++ à télécharger ici : [`Visual C++ Package AiO`](https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/)

- Allez sur le lien ci dessus, puis cliquer sur le bouton bleu à gauche de la page marqué "DOWNLOAD"
- Sur la page qui s'ouvre, cliquez sur n'importe quel drapeau pour lancer le téléchargement.
- Vous avez téléchargé une archive. Utilisez winRAR, ou 7-zip, ou le gestionnaire d'archive de windows pour extraire cette archive (clic droit -> extraire).
- Une fois l'archive extraite, ouvrez le dossier de l'archive extraite, faites un clic droit sur le fichier "**install_all**", et cliquez sur "**Lancer en tant qu'administrateur**".
- Attendre la fin des installations, puis redémarrer le PC.


## Réduire encore plus la latence

Simplement, un logiciel qui réduira la latence de votre Windows mais aussi, cela permet de purger la RAM. 
Aucune bidouille nécessaire. 

Pour cela, il vous faut [`Intelligent Standby List Cleaner`](https://www.wagnardsoft.com/forums/viewtopic.php?f=5&t=1256)

En bas à gauche du logiciel vous aurez 2 lignes : 

- The list size is at least
- Free Memory is lower than

Sur la 1ère ligne, vous laissez 1024 MB.

Sur la 2nd ligne, vous appliquez au MINIMUM la moitié du nombre total de votre RAM. Personnellement, pour 16 Go de RAM, j'applique 8192 MB. 

N'allouez pas tout, laissez au moins 4 Go de RAM de dispo afin que la purge de RAM se fasse régulièrement.

N'oubliez pas de cocher les 2 cases en dessous de ses lignes afin que ISLC démarre au démarrage et en mode réduit.

## Réactiver les mises à jour automatiques des drivers

Il est utile de laisser cette fonction active une fois que tout le guide a été fait. 

Lorsque vous mettez une nouveau périphérique à brancher en USB sur votre PC, il est parfois pénible de trouver le bon fichier ".cab" afin d'installer manuellement le certificat qui peut ne pas être trouvé du tout ou pas compatible.

Réactiver les mises à jour automatiques des drivers permet d'éviter de chercher des heures ce qui peut être fait en 2 secondes (lancer CMD en administrateur) : 

`REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\DriverSearching" /v SearchOrderConfig /t REG_DWORD /d 00000001 /f`


## (BONUS) Liste des logiciels utiles à installer sur votre PC

- [`7Zip`](https://www.7-zip.org/download.html) : gratuit et open-source, plus léger et meilleur (à mon sens) que WinRar.

- [`NVCleanstall`](https://www.techpowerup.com/download/techpowerup-nvcleanstall/) : alternative à GeForce Experience, plus léger, permet d’installer que le driver vidéo. Vous pouvez donc ne pas installer GeForce Experience, Ansel, ShadowPlay etc. si vous ne les utilisez pas. Vous pouvez aussi les installer si nécessaire. A vous de voir, cela ne joue pas sur les performences en jeu si vous installez toutes les features de Nvidia ou pas.

- [`LibreOffice`](https://fr.libreoffice.org/download/telecharger-libreoffice/) : Bon remplaçant de la suite Office de Microsoft, prend en charge l’exportation “.docx”, gratuit, interface qui se rapproche beaucoup de Word.

- [`Office 2007`](https://mega.nz/file/lgAjlKab#5JHXgCCO1n9EwRzauOOl_n__bQN1d3C2mGINKf3iH2E) : si vous souhaitez garder la suite Office de Microsoft, alors je vous recommande cette version. Pas de nécessité de se connecter à internet, gère les formats “.docx” sur les documents récents. Outre l’interface qui change un petit peu, vous ne vous perdrez pas car les menus sont identiques aux versions récentes (2013/2016/2019/2021). Aussi, nous pouvons supprimer le service “Office Source Engine” pour ne pas que les mises à jour de Office 2007 se fassent avec Windows Update.

- [`VLC Player`](https://www.videolan.org/vlc/index.fr.html) : bonne alternative au lecteur de base de Windows 10 qui est une infamie ou au Lecteur Windows Media. Plus polyvalent, une meilleure compatibilité des fichiers. Encore une fois, open-source. 

- [`Epic Disk Cleanup`](https://drive.google.com/open?id=1ORb7otD5bvITT5eBgsMvOz60BWkRp2Wd) : pour ajouter cette fonctionnalité embarquée dans Windows faites windows+r et tapez : cleanmgr.exe /sageset:50 et faites Enter. 
Permet de nettoyer plus en profondeur votre PC. Pas besoin de logiciel tier, le cleanup embarqué dans Windows est le mieux.
Cochez tout sauf Corbeille (conseillé de le cocher) et Téléchargement (conseillé de ne pas le cocher afin de garder ce que vous avez besoin). 
Une fois réglé, téléchargez le raccourci de Epic Disk Cleanup et lancez le. Il fera le travail que vous lui aurez demandé de faire. 

- [`OpenShell`](https://github.com/Open-Shell/Open-Shell-Menu/releases/) : Remplace le menu démarrer natif de Windows 10 par un style Windows 7. Fork de StartMenu 7.















