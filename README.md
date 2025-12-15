minimal
=======

A minimal fork of a minimal fork of [subnixr's minimal] prompt theme.

<img width="761" src="https://github.com/user-attachments/assets/af40b472-d23f-4adb-94ec-7df6ae6bdcbe"/>

What does it show?
------------------

Left prompt:
  * The hostname only if current session is through a SSH connection.
  * An indicator displaying the following information:
    * User privilege: `#` when root, one of the following otherwise.
    * Last command success: indicator's color is set to MNML_OK_COLOR and
      the prompt character is set to MNML_OK_CHAR when last command was
      successful, MNML_ERR_COLOR and MNML_ERR_CHAR otherwise.
    * Background jobs: MNML_BGJOB_MODE is applied to the indicator if at least
      one job is in background.

Right prompt:
  * The last 2 components of the current working directory.
  * The current git branch, when inside a git repo. Color is set to
    MNML_OK_COLOR if the branch is clean, MNML_ERR_COLOR if the branch is dirty.

Magic enter
-----------

A fork of the magic enter feature from [subnixr's minimal] is available
separately in Zim's [magic-enter] module.

Settings
--------

This theme can be customized with the following environment variables. If a
variable is not defined, the respective default value is used.

| Variable         | Description                                 | Default value |
| ---------------- | ------------------------------------------- | ------------- |
| MNML_OK_COLOR    | Color for successful things                 | `green`       |
| MNML_ERR_COLOR   | Color for failures                          | `red`         |
| MNML_BGJOB_MODE  | Mode applied when there are background jobs | `4`           |
| MNML_OK_CHAR     | Character used for successful things        | `󰋑`           |
| MNML_ERR_CHAR    | Character used for unsuccessful things      | `󰋔`           |

Advanced settings
-----------------

You can customize how the current working directory is shown with the
[prompt-pwd module settings].

These advanced settings must be overridden after the theme is initialized.

Requirements
------------

Requires Zim's [prompt-pwd] module to show the current working directory, and
[git-info] to show git information.

[zimfw's minimal]: https://github.com/zimfw/minimal
[subnixr's minimal]: https://github.com/subnixr/minimal
[magic-enter]: https://github.com/zimfw/magic-enter
[prompt-pwd module settings]: https://github.com/zimfw/prompt-pwd/blob/master/README.md#settings
[prompt-pwd]: https://github.com/zimfw/prompt-pwd
[git-info]: https://github.com/zimfw/git-info
