mdGoogleMapDoctrinePlugin
=========================

INSTALACION

1- schema.yml

2- habilitar el modulo mdMap en el settings

3- En la pagina donde se vaya a utilizar incluir:

<meta name="viewport" content="initial-scale=1.0, user-scalable=no" /> <?php
use_javascript("http://maps.google.com/maps/api/js?sensor=true");
use_plugin_javascript('mdGoogleMapDoctrinePlugin', 'mdGoogleMapControlBackend.js', 'last');
use_plugin_javascript('mdGoogleMapDoctrinePlugin', 'mdGoogleMap.js', 'last'); ?>

4- incluir el partial _googleMap. Las opciones que recibe son:

  $object: Este objecto debe tener los metodos getObjectClass y getId
  $options un arreglo de opciones.
  Las opciones validas y soportadas al momento son:
   $width: ancho del contenedor del mapa
   $height: alto del contenedor del mapa
   $zoom: zoom en el mapa

<?php include_partial('mdMap/googleMap', array('object' => $md_restaurant, 'options' => array('latitude' => '-34.911414', 'longitude' => '-56.151552', 'width' => '550', 'height' => '250', 'zoom' => 13))); ?>
