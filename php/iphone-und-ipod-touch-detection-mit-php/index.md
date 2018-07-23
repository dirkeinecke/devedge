---
title: iPhone und iPod touch Detection mit PHP
---

## iPhone und iPod touch Detection mit PHP

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
    <title>iPhone and iPod touch detection with PHP</title>
    <style type="text/css">
      * {
        font-size: 30px;
      }
    </style>
  </head>
  <body>
    <?php
      function detect_iPhone() {
        $b_return = (bool) false;
        $arr_user_agents = (array) array ('iPhone', 'iPod');

        foreach ($arr_user_agents as $str_user_agent) {
          if (false != strpos($_SERVER['HTTP_USER_AGENT'], $str_user_agent)) {
            $b_return = true;
          }
        }

        return $b_return;
      }

      $b_detect = (bool) detect_iPhone();

      if (true === $b_detect) {
        echo '<p>This is an iPhone or iPod touch.</p>';
      } else {
        echo '<p>This is not an iPhone or iPod touch.</p>';
      }
    ?>
  </body>
</html>
