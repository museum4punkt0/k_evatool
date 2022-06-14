# k:evatool

### Description
The "k:evatool" is designed as an application for the evaluation of diverse, digital offers and mediation formats. It is versatile and can be adapted to the format to be evaluated. An interface makes it possible to integrate the surveys into the museums' existing applications. Surveys can be easily created, tested and evaluated in a content management system. For the respondents, the surveys are more varied and entertaining.
<br>It was developed as part of the project "Labor digital: Vermittlungsformate in und außerhalb der Museen"

### Funding
This project is part of the project museum4punkt0 - Digital Strategies for the Museum of the Future, sub-project k:eva. Further information: https://www.museum4punkt0.de.

The project museum4punkt0 is funded by the Federal Government Commissioner for Culture and the Media in accordance with a resolution issued by the German Bundestag (Parliament of the Federal Republic of Germany).
 
![BKM-Logo](https://github.com/museum4punkt0/Object-by-Object/blob/77bba25aa5a7f9948d4fd6f0b59f5bfb56ae89e2/04%20Logos/BKM_Fz_2017_Web_de.gif)
![NeustartKultur](https://github.com/museum4punkt0/Object-by-Object/blob/22f4e86d4d213c87afdba45454bf62f4253cada1/04%20Logos/BKM_Neustart_Kultur_Wortmarke_pos_RGB_RZ_web.jpg)

### Skills required to implement
We recommend personnel with a good skill set in server administration and usage of Docker images.
Further development of the different parts of the system requires good skill in Laravel and VueJs.

### Recommended Server Setup 
#### Backend (Laravel)
- Ubuntu 20.04
- Apache 2.4.x
- PHP 8.0  (Several additional php modules are needed. Please see https://laravel.com/docs/8.x/deployment)
- MySQL 8.0
- Composer 2.x

#### Frontend (VueJS)
- Ubuntu 20.04
- Apache 2.4.x
- NodeJS 14.x

### Installation
The full installation of the k:evatool consists of four repositories
- k_evatool_laravel_container_app (Laravel app)
- k_evatool_laravel_package (Laravel package)
- k_evatool_admin_frontend (VueJS App)
- k_evatool_survey_player (VueJS App)

#### k_evatool_laravel_container_app
This part of the system functions as a wrapper for the k:evatool Laravel package. It is intended to provide a fully functional backend including user 
management and OAUTH Authentication.
https://github.com/museum4punkt0/k_evatool_laravel_container_app

####  k_evatool_laravel_package
This Laravel package is located within the container app and holds all components that are needed to provide the survey related API. Please see the package 
readme for installation instructions.
CAUTION: The package must be cloned into **/packages/twoavy** within the **k_evatool_laravel_container_app**. Otherwise installation won't complete.
https://github.com/museum4punkt0/k_evatool_laravel_package

#### k_evatool_survey_player
The survey player holds the user frontend needed to display a survey or single question. The player connects to the k:evatool backend through the RESTful 
API using a maximum of three endpoints to get the survey and post the result data and if applicable the audio file data of a voice recording.
https://github.com/museum4punkt0/k_evatool_survey_player

#### k_evatool_admin_frontend
This app provides the admin frontend for the k:evatool.
https://github.com/museum4punkt0/k_evatool_admin_frontend

### Development
There are 4 build systems included. 

### Usage
All three services can be run on the same server. For environments expecting high loads it is recommended to host each service on a dedicated machine. As 
all three units are intended to communicate directly with each other they must either be able to access the same network or need to be made available over 
the internet. 

### Contributing
If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcome.

### About
The Klassik Stiftung Weimar (KSW), like an increasing number of museums, is sending online education offers into the digital space. The Corona pandemic of recent years in particular has accelerated this process. However, relatively little is known in the intuitions about the online audience that perceives such offers. In order to explore the conditions for success of digital offerings, the KSW developed a new tool that goes beyond the approaches of previous questionnaires and data analysis tools. Together with an agency, a digital evaluation tool was developed in an iterative procedure in order to find out more about the digital audience and their interests and needs using quantitative, but above all qualitative research approaches. This was tested using the format of the Digital Workshop as an example. In the development process, the central concern was to make the surveys more entertaining and varied and to adapt the evaluation tool to the diverse offers of the KSW. The integration into the daily work of museums and other cultural institutions should be promoted through simple operation. The k:evatool makes it possible to carry out small, short surveys on a wide range of offers without great effort and to evaluate them quickly, thus integrating evaluation processes into day-to-day business.

#### Team 2av
- Katrin Jedon (Project coordination and methodology)
- Martin Schmitt (Technical project lead and backend development)
- Manuel Herr (Software developer)
- Miroslav Milev (Software developer)
- Thomas Geißl (Software developer)

#### museum4punkt0 Teilprojekt M16
- Sophia Gröschke (Teilprojektleitung / Referentin Kulturelle Bildung)
- Felix Zühlsdorf (Stellvertretende Teilprojektleitung / Referent Kulturelle Bildung)
- Nicolas Dittgen (Projektkoordination: Evaluierung Digitale Werkstatt)
- Florentine Holte (Projektkoordination: Augmentierte Raumerfahrungen App)

### License
GNU GENERAL PUBLIC LICENSE <br>
Copyright © 2022, 2av GmbH <br>
Please also see the LICENSE file provided within this repository
