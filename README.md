# NRF5340 Audio DK buildprog
This is a hacky version of Nordic Semiconductor's [buildprog tool](https://github.com/nrfconnect/sdk-nrf/tree/v2.0-branch/applications/nrf5340_audio/tools/buildprog) developed for NRF5340 Audio DevKits. 

In some linux distributions `nrfjprog`, the executable that is used to program nordic boards, doesn't exit after flashing and causes `buildprog.py` to stuck. This modified, dirty version tracks the log file and if it detects inactivity after some time, it assumes the flashing process is finished and kills the `nrfjprog` process manually.

## WARNING
The way this code works may be dangerous in some cases. Interfering a flashing process is definitely not recommended. Use at your own risk.