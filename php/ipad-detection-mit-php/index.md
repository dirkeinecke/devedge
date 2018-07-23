---
title: iPad Detection mit PHP
---

## iPad Detection mit PHP

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
    <title>iPad detection with PHP</title>
    <style type="text/css">
      * {
        font-size: 30px;
      }
    </style>
  </head>
  <body>
    <?php
      function detect_iPad() {
        $b_return = (bool) false;
        $arr_user_agents = (array) array ('iPad');

        foreach ($arr_user_agents as $str_user_agent) {
          if (false != strpos($_SERVER['HTTP_USER_AGENT'], $str_user_agent)) {
            $b_return = true;
          }
        }

        return $b_return;
      }

      $b_detect = (bool) detect_iPad();

      if (true === $b_detect) {
        echo '<p>This is an iPad.</p>';
      } else {
        echo '<p>This is not an iPad.</p>';
      }
    ?>
  </body>
</html>
