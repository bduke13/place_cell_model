# Context-Dependent Spatial Representations in the Hippocampus using Place Cell Dendritic Computing

## Overview
This project explores the role of place cells in the hippocampus of rodents, focusing on how they encode physical space and exhibit context-dependent spatial representations. The project includes simulations that model place cells using dendritic computation to demonstrate how they can reuse spatial representations across different contexts while maintaining uncorrelated place fields.

## Requirements
To install the required dependencies, please ensure you have Python installed, and then run:

```bash
pip install -r requirements.txt
```

## Usage
1. **Initialize the Driver**: The `Driver` class controls the robot and its interactions with the environment. It handles the loading or initialization of neural networks (place cell network and reward cell network) and manages the robot's sensors and movements.

2. **Startup**: To start the simulation, use the `startup` method of the `Driver` class.

    Example:
    ```python
    from driver import Driver

    driver = Driver(num_place_cells=1000, num_reward_cells=10, num_head_directions=8, run_time_minutes=2, timestep=96)
    driver.startup(context=0, mode="explore", randomize=True)
    ```

3. **Customization**: Modify the `Driver` class parameters to suit your simulation needs, such as the number of place cells, reward cells, or the duration of the simulation.

## File Structure
- `driver.py`: Contains the `Driver` class which manages the simulation.
- `networks.py`: Contains neural network definitions used by the driver.
- `requirements.txt`: Lists the dependencies required to run the project.

## Research Context
This project is part of research focused on understanding how the hippocampus encodes space through place cells that show maximal firing in specific regions. The model leverages dendritic morphology and synaptic modulation to demonstrate how place cells can encode different maps for environments with identical sensory cues.

## Contributing
Feel free to submit issues or pull requests. Contributions are welcome!

## License
MIT License

Copyright (c) 2024 University of Cincinnati

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
