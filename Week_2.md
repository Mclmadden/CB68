### Monday 1/30

Continue inspecting PV diagrams in CARTA with the primary-beam-corrected images.

Start with $H_2CO$, CS, CCH, SO, and SiO.

Encountering error when attempting to install jupyter and jupyterlab: `pip3 install --user jupyter`

Work station has Python 3.6.8 and pip 9.0.3

--> updated pip3 and force reinstalled

--> `pip3 install --user jupyterlab` resulted in `Successfully installed babel-2.11.0 json5-0.9.11 jupyter-server-1.13.1 jupyterlab-3.2.9 jupyterlab-server-2.10.3 nbclassic-0.3.5`

--> must add the user-level bin directory to PATH environment variable in order to launch jupyter lab as per the jupyter lab documentation 


### Tuesday 1/31

Attempting to ssh into Jupyter Lab from birdseye.

"Must add user-level `bin` directory to `PATH` environment bariable in order to launch `jupyter lab`" by running `export PATH="$HOME/.local/bin:$PATH"` before `pip3 install --user jupyterlab`

SSH into jupyter lab: `jupyter lab --no-browser` (usually port 8888) and open local host in browser.

Error: `channel 2: open failed: administratively prohibited: open failed` when trying to open browser. (Sometimes it's `channel 1`.

Returning same error when attempting to ssh into CARTA again... 

In the meantime, download FITS cube from ALMA Archive (CCH) to experiment with in Python.


### Wednesday 2/1

Took 3 tries to ssh into birdseye, running into `connection timed out` and `connection refused` the initial attempts.

Remove `/usr/local/bin:` from PATH in `~/.bashrc`, leaving `PATH=/usr/local/gnu/bin:/usr/bin:/usr/sbin:/usr/openwin/bin ; export PATH` --> still prohibited from opening any ssh tunnel.

Continue with CCH Archive data on local drive.

Convert spectral axis of FITS files from default frequency (Hz) to velocity (km/s) using rest value found in file headers: `with_spectral_unit(u.km/u.s, velocity_convention='radio', rest_value=Value * u.Hz)`

### Thursday 2/2

Running CCH Archive file through `with_spectral_unit()` results in `KeyError: PhysicalType('frequency')`

Adele posted issue on spectral-cube Github Issues page: https://github.com/radio-astro-tools/spectral-cube/issues/830

Solution is the update spectral-cube to version 0.6.0. Imported spectral-cube and default installation was version 0.5.0.

`pip3 install --upgrade spectral-cube` updates to spectral-cube v0.6.0 (and successfully carries over to jupyterlab).

Able to convert spectral axis from frequency to velocity! 

