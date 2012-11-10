correios_soap
=============

Correios WebServices via SOAP.

### Usage example:

    <?php
    include_once 'Correios/SOAP.php';

    $service = array( '40010', '40045', '40215', '40290', '41106' );
    $zipOrigin = '04346000';
    $zipDestination = '543-7117';
    $height = 20;
    $width = 20;
    $diameter = 0;
    $length = 30;
    $weight = 2;

    $correios = new Correios_SOAP($service, $zipOrigin, $zipDestination, $height, $width, $diameter, $length, $weight);

    print_r($correios->calculateShipping());
    ?>

correios_simplexml
==================

Correios WebServices via SimpleXML.

### Usage example:

    <?php
    include_once 'Correios/SOAP.php';
    include_once 'Correios/SimpleXML.php';

    $service = array( '40010', '40045', '40215', '40290', '41106' );
    $zipOrigin = '04346000';
    $zipDestination = '543-7117';
    $height = 20;
    $width = 20;
    $diameter = 0;
    $length = 30;
    $weight = 2;

    $correios = new Correios_SimpleXML($service, $zipOrigin, $zipDestination, $height, $width, $diameter, $length, $weight);

    print_r($correios->calculateShipping());
    ?>

cubagem
=======

Estimated cubic volume for multiple products in a package.

### Usage example:

    <?php
    include_once 'Correios/Cubage.php';

    $heights = array( '20', '40', '80 );
    $widths = array( '5', '10', '5 );
    $lengths = array( '30', '20', '40 );

    $cubage = new Correios_Cubage( $heights, $widths, $lengths );
    print_r($cubage->cubage())
    ?>
