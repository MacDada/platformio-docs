..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _board_nordicnrf51_redBearLab:

RedBearLab nRF51822
===================

.. contents::

Hardware
--------

Platform :ref:`platform_nordicnrf51`: The Nordic nRF51 Series is a family of highly flexible, multi-protocol, system-on-chip (SoC) devices for ultra-low power wireless applications. nRF51 Series devices support a range of protocol stacks including Bluetooth Smart (previously called Bluetooth low energy), ANT and proprietary 2.4GHz protocols such as Gazell.

.. list-table::

  * - **Microcontroller**
    - NRF51822
  * - **Frequency**
    - 16MHz
  * - **Flash**
    - 256KB
  * - **RAM**
    - 16KB
  * - **Vendor**
    - `RedBearLab <https://www.seeedstudio.com/RedBearLab-nRF51822-p-2126.html?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``redBearLab`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:redBearLab]
  platform = nordicnrf51
  board = redBearLab

You can override default RedBearLab nRF51822 settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `redBearLab.json <https://github.com/platformio/platform-nordicnrf51/blob/master/boards/redBearLab.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:redBearLab]
  platform = nordicnrf51
  board = redBearLab

  ; change microcontroller
  board_build.mcu = nrf51822

  ; change MCU frequency
  board_build.f_cpu = 16000000L


Uploading
---------
RedBearLab nRF51822 supports the following uploading protocols:

* ``blackmagic``
* ``cmsis-dap``
* ``jlink``
* ``nrfjprog``
* ``stlink``

Default protocol is ``cmsis-dap``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:redBearLab]
  platform = nordicnrf51
  board = redBearLab

  upload_protocol = cmsis-dap

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

RedBearLab nRF51822 has on-board debug probe and **IS READY** for debugging. You don't need to use/buy external debug probe.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_blackmagic`
    - 
    - 
  * - :ref:`debugging_tool_cmsis-dap`
    - Yes
    - Yes
  * - :ref:`debugging_tool_jlink`
    - 
    - 
  * - :ref:`debugging_tool_stlink`
    - 
    - 

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_arduino`
      - Arduino Wiring-based Framework allows writing cross-platform software to control devices attached to a wide range of Arduino boards to create all kinds of creative coding, interactive objects, spaces or physical experiences