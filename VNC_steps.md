1. In a terminal window, log in to NRAO ssh portal

2. ssh into reserved node, e.g. `nmpost007`

3. Start up VNC session with `vncserver`

4. Call `vncserver -list` to determine X Display #, e.g. :2

5. Start up jupyter lab session in correct directory, e.g. `jupyter lab --no-browser /lustre/aoc/students/mmadden`

6. In a second terminal window, log into ssh portal through the node using the display number, e.g. `ssh -N -T -L 5902:nmpost007:5902 mmadden@ssh.aoc.nrao.edu`

7. Leave terminal sessions open

8. Open TigerVNC, and enter port number the node is using, e.g. `localhost:5902`

9. Open jupyter lab session in a browser in VNC session using the port number and token number shown in the terminal session
