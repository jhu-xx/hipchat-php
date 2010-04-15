hipchat-php
===========

A PHP library for interacting with the [HipChat][hc] REST API.

Testing
-------
You can test this library (and your API key) using the example.php script as follows. It should print a list of your rooms and users.

    ./example.php <your api token>

To test the library itself, run the PHPUnit tests:

    phpunit tests/

Usage
-----
    require 'HipChat.php';

    $token = '<your api token>';
    $hc = new HipChat($token);

    foreach ($hc->get_rooms() as $room) {
      echo " - $room->id = $room->name\n";
    }


[hc]: http://www.hipchat.com
