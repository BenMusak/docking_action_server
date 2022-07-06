# Description

This is a docking action server reposetory for the P6-project:
<https://github.com/kasperfg16/p6-swarm>

## Installation

This code is to be installed on the robot computer.

This is done by connecting a mouse and keyboard to the robot computer. Then plug a monitor to the robot computer. From here:

1. In a terminal

    Clone the reposetory into a **PATH** of your choice

    ``` bash
    cd PATH/
    ```

    ``` bash
    git clone https://github.com/BenMusak/docking_action_server
    ```

## Update the docking code / Uploading of updates Over The Air (OTA)

On the robots there are a script to easily update the robots if the firmware is changed:

1. Open a new terminal in root

    - a)

        SSH onto the robot computer e.g. via the use of putty SSH client: <https://itsfoss.com/putty-linux/>

        Then run the following command

        ``` bash
        python3 Upload_firmware_code
        ```
