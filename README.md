# airflow-dynamics-CA
 Cellular Automata for simulating airflow using ± air pressure

## Generating approximate static airflow in confined spaces using ± air pressure
This project solves a specific problem encountered during development of `Cutwell/genetic-policy-optimisation`, i.e.: simulating airflow using simple cellular automata is difficult.
Other approaches have relied on individual cells possessing multiple characteristics, such as maginitude and direction of airflow, in order to describe airflow in the space. However, a constraint applied to the development of our own simulations was that each automata describes a single attribute.

Air pressure can be used as an approximation to describe how airborne particles might generally move through a space - leaving areas of positive pressure (inflow of air) and moving towards areas of negative pressure (outflow of air).

This automata ruleset describes a solution to this problem, following these assumptions, and can be run until the simulation stabilises in order to gain a full airflow map.

## CellPyLib extensions
These resources are extensions of the CellPyLib module.

|  |  |
|:---:|:---:|
| `airpressure.AirflowRule` | Custom ruleset, same useage as any custom CellPyLib ruleset. |
| `airpressure.until_fixed_point_or_max` | Custom timesteps rule, exits simulation once stable, or upon reaching `self.max_airflow_epochs` (user defined). |

## Additional utility
The `utility` module provides a simple helper script for converting images into numpy arrays, which can be helpful when designing large automatons. View `utility/example` for a demonstration (.xcf file opens with GIMP).

|  | Verbosity |
|:---:|:---:|
| `utility.parse_matrix_from_image` | Verbosity: > 0, display plot of image.  > 1, save matrix as .txt |
