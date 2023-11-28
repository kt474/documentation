<span id="qiskit-qobj-pulseqobjconfig" />

# qiskit.qobj.PulseQobjConfig

<span id="undefined" />

`PulseQobjConfig(meas_level, meas_return, pulse_library, qubit_lo_freq, meas_lo_freq, memory_slot_size=None, rep_time=None, rep_delay=None, shots=None, max_credits=None, seed_simulator=None, memory_slots=None, **kwargs)`

A configuration for a Pulse Qobj.

Instantiate a PulseQobjConfig object.

**Parameters**

*   **meas\_level** (*int*) – The measurement level to use.
*   **meas\_return** (*int*) – The level of measurement information to return.
*   **pulse\_library** (*list*) – A list of [`PulseLibraryItem`](qiskit.qobj.PulseLibraryItem#qiskit.qobj.PulseLibraryItem "qiskit.qobj.PulseLibraryItem") objects which define the set of primative pulses
*   **qubit\_lo\_freq** (*list*) – List of frequencies (as floats) for the qubit driver LO’s in GHz.
*   **meas\_lo\_freq** (*list*) – List of frequencies (as floats) for the’ measurement driver LO’s in GHz.
*   **memory\_slot\_size** (*int*) – Size of each memory slot if the output is Level 0.
*   **rep\_time** (*int*) – Time per program execution in sec. Must be from the list provided by the backend (`backend.configuration().rep_times`). Defaults to the first entry in `backend.configuration().rep_times`.
*   **rep\_delay** (*float*) – Delay between programs in sec. Only supported on certain backends (`backend.configuration().dynamic_reprate_enabled` ). If supported, `rep_delay` will be used instead of `rep_time` and must be from the range supplied by the backend (`backend.configuration().rep_delay_range`). Default is `backend.configuration().default_rep_delay`.
*   **shots** (*int*) – The number of shots
*   **max\_credits** (*int*) – the max\_credits to use on the IBMQ public devices.
*   **seed\_simulator** (*int*) – the seed to use in the simulator
*   **memory\_slots** (*list*) – The number of memory slots on the device
*   **kwargs** – Additional free form key value fields to add to the configuration

<span id="undefined" />

`__init__(meas_level, meas_return, pulse_library, qubit_lo_freq, meas_lo_freq, memory_slot_size=None, rep_time=None, rep_delay=None, shots=None, max_credits=None, seed_simulator=None, memory_slots=None, **kwargs)`

Instantiate a PulseQobjConfig object.

**Parameters**

*   **meas\_level** (*int*) – The measurement level to use.
*   **meas\_return** (*int*) – The level of measurement information to return.
*   **pulse\_library** (*list*) – A list of [`PulseLibraryItem`](qiskit.qobj.PulseLibraryItem#qiskit.qobj.PulseLibraryItem "qiskit.qobj.PulseLibraryItem") objects which define the set of primative pulses
*   **qubit\_lo\_freq** (*list*) – List of frequencies (as floats) for the qubit driver LO’s in GHz.
*   **meas\_lo\_freq** (*list*) – List of frequencies (as floats) for the’ measurement driver LO’s in GHz.
*   **memory\_slot\_size** (*int*) – Size of each memory slot if the output is Level 0.
*   **rep\_time** (*int*) – Time per program execution in sec. Must be from the list provided by the backend (`backend.configuration().rep_times`). Defaults to the first entry in `backend.configuration().rep_times`.
*   **rep\_delay** (*float*) – Delay between programs in sec. Only supported on certain backends (`backend.configuration().dynamic_reprate_enabled` ). If supported, `rep_delay` will be used instead of `rep_time` and must be from the range supplied by the backend (`backend.configuration().rep_delay_range`). Default is `backend.configuration().default_rep_delay`.
*   **shots** (*int*) – The number of shots
*   **max\_credits** (*int*) – the max\_credits to use on the IBMQ public devices.
*   **seed\_simulator** (*int*) – the seed to use in the simulator
*   **memory\_slots** (*list*) – The number of memory slots on the device
*   **kwargs** – Additional free form key value fields to add to the configuration

## Methods

|                                                                                                                                |                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| [`__init__`](#qiskit.qobj.PulseQobjConfig.__init__ "qiskit.qobj.PulseQobjConfig.__init__")(meas\_level, meas\_return, …\[, …]) | Instantiate a PulseQobjConfig object.                               |
| [`from_dict`](#qiskit.qobj.PulseQobjConfig.from_dict "qiskit.qobj.PulseQobjConfig.from_dict")(data)                            | Create a new PulseQobjConfig object from a dictionary.              |
| [`to_dict`](#qiskit.qobj.PulseQobjConfig.to_dict "qiskit.qobj.PulseQobjConfig.to_dict")()                                      | Return a dictionary format representation of the Pulse Qobj config. |

<span id="undefined" />

`classmethod from_dict(data)`

Create a new PulseQobjConfig object from a dictionary.

**Parameters**

**data** (*dict*) – A dictionary for the config

**Returns**

The object from the input dictionary.

**Return type**

[PulseQobjConfig](#qiskit.qobj.PulseQobjConfig "qiskit.qobj.PulseQobjConfig")

<span id="undefined" />

`to_dict()`

Return a dictionary format representation of the Pulse Qobj config.

**Returns**

The dictionary form of the PulseQobjConfig.

**Return type**

dict