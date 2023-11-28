# qiskit.chemistry.algorithms.BOPESSampler

<span id="undefined" />

`BOPESSampler(gss, tolerance=0.001, bootstrap=True, num_bootstrap=None, extrapolator=None)`

Class to evaluate the Born-Oppenheimer Potential Energy Surface (BOPES).

**Parameters**

*   **gss** (`GroundStateSolver`) – GroundStateSolver
*   **tolerance** (`float`) – Tolerance desired for minimum energy.
*   **bootstrap** (`bool`) – Whether to warm-start the solution of variational minimum eigensolvers.
*   **num\_bootstrap** (`Optional`\[`int`]) – Number of previous points for extrapolation and bootstrapping. If None and a list of extrapolators is defined, the first two points will be used for bootstrapping. If no extrapolator is defined and bootstrap is True, all previous points will be used for bootstrapping.
*   **extrapolator** (`Optional`\[`Extrapolator`]) – Extrapolator objects that define space/window and method to extrapolate variational parameters.

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – If `num_boostrap` is an integer smaller than 2, or if `num_boostrap` is larger than 2 and the extrapolator is not an instance of `WindowExtrapolator`.

<span id="undefined" />

`__init__(gss, tolerance=0.001, bootstrap=True, num_bootstrap=None, extrapolator=None)`

**Parameters**

*   **gss** (`GroundStateSolver`) – GroundStateSolver
*   **tolerance** (`float`) – Tolerance desired for minimum energy.
*   **bootstrap** (`bool`) – Whether to warm-start the solution of variational minimum eigensolvers.
*   **num\_bootstrap** (`Optional`\[`int`]) – Number of previous points for extrapolation and bootstrapping. If None and a list of extrapolators is defined, the first two points will be used for bootstrapping. If no extrapolator is defined and bootstrap is True, all previous points will be used for bootstrapping.
*   **extrapolator** (`Optional`\[`Extrapolator`]) – Extrapolator objects that define space/window and method to extrapolate variational parameters.

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – If `num_boostrap` is an integer smaller than 2, or if `num_boostrap` is larger than 2 and the extrapolator is not an instance of `WindowExtrapolator`.

## Methods

|                                                                                                                                                       |                                                                    |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [`__init__`](#qiskit.chemistry.algorithms.BOPESSampler.__init__ "qiskit.chemistry.algorithms.BOPESSampler.__init__")(gss\[, tolerance, bootstrap, …]) | **type gss**`GroundStateSolver`                                    |
| [`sample`](#qiskit.chemistry.algorithms.BOPESSampler.sample "qiskit.chemistry.algorithms.BOPESSampler.sample")(driver, points)                        | Run the sampler at the given points, potentially with repetitions. |

<span id="undefined" />

`sample(driver, points)`

Run the sampler at the given points, potentially with repetitions.

**Parameters**

*   **driver** (`BaseDriver`) – BaseDriver specific for the problem. The driver should be based on a Molecule object that has perturbations to be varied.
*   **points** (`List`\[`float`]) – The points along the degrees of freedom to evaluate.

**Return type**

`BOPESSamplerResult`

**Returns**

BOPES Sampler Result

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if the driver does not have a molecule specified.