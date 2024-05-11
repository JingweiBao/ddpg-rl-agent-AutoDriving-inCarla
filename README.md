## Requirements

Software:
- Python 3.7
- CARLA 0.9.9
- Libraries: install from `requirements.txt`

Hardware (minimum):
- CPU: at least quad or octa core.
- GPU: dedicated, with as much memory as possible.
- RAM: at least 16 or 32 Gb.

---

## Installation

Before running any code from this repo you have to:
1. **Clone this repo**: `git clone https://github.com/JingweiBao/ddpg-rl-agent-AutoDriving-inCarla.git`
2. **Download CARLA 0.9.9** from their GitHub repo, [here](https://github.com/carla-simulator/carla/releases/tag/0.9.9) 
   where you can find precompiled binaries which are ready-to-use. Refer to [carla-quickstart](https://carla.readthedocs.io/en/latest/start_quickstart/)
   for more information.
3. **Install CARLA Python bindings** in order to be able to manage CARLA from Python code. Open your terminal and type:
   
    * *Windows*: `cd your-path-to-carla/CARLA_0.9.9.4/WindowsNoEditor/PythonAPI/carla/dist/`
    * *Linux*: `cd your-path-to-carla/CARLA_0.9.9.4/PythonAPI/carla/dist/`
    * Extract `carla-0.9.9-py3.7-XXX-amd64.egg` where `XXX` depends on your OS, e.g. `win` for Windows.
    * Create a `setup.py` file within the extracted folder and write the following:
      ```python
      from distutils.core import setup
      
      setup(name='carla',
            version='0.9.9',
            py_modules=['carla']) 
      ```
    * Install via pip: `pip install -e ~/CARLA_0.9.9.4/PythonAPI/carla/dist/carla-0.9.9-py3.7-XXX-amd64`

---

## Examples
Turn on Carla
'
YOUR_PATH_TO_CARLA/carla/CARLA_0.9.9.4/./CarlaUE4.sh
'

Run the 1st stage training:
'
cd /YOUR_PATH_TO_CARLA/carla/carla-driving-rl-agent
python3 main.py
'
