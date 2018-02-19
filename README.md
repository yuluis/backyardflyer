# backyardflyer
Udacity Flying car class preview class 3 project 1

Mac OS 10.13.3. Download simulator and execute FCND-Simulator.
Miniconda3-latest-MacOSX-x86_64

Mac OS 10.13.3. 
Install Xcode command line tools.
Git —version
git clone https://github.com/udacity/FCND-Term1-Starter-Kit.git
cd FCND-Term1-Starter-Kit
conda env create -f environment.yml
conda info --envs
conda clean -tp

source activate fcnd
(fcnd) Luiss-MacBook-Pro-13:FCND-Term1-Starter-Kit luisyu$

ipython

from udacidrone import Drone
from udacidrone.connection import MavlinkConnection
conn = MavlinkConnection(‘tcp:127.0.0.1:5760’, threaded=True)
drone = Drone(conn)
drone.start()

drone.take_control()
drone.arm()

drone.set_home_position(drone.global_position[0],
                       drone.global_position[1],
                       drone.global_position[2])

drone.takeoff(3)

drone.cmd_position(5,0,3,0)
