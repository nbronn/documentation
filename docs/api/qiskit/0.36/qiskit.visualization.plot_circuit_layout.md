---
title: plot_circuit_layout
description: API reference for qiskit.visualization.plot_circuit_layout
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.visualization.plot_circuit_layout
---

# qiskit.visualization.plot\_circuit\_layout

<span id="qiskit.visualization.plot_circuit_layout" />

`plot_circuit_layout(circuit, backend, view='virtual', qubit_coordinates=None)`

Plot the layout of a circuit transpiled for a given target backend.

**Parameters**

*   **circuit** ([*QuantumCircuit*](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")) – Input quantum circuit.
*   **backend** ([*Backend*](qiskit.providers.Backend "qiskit.providers.Backend")) – Target backend.
*   **view** (*str*) – Layout view: either ‘virtual’ or ‘physical’.
*   **qubit\_coordinates** (*Sequence*) – An optional sequence input (list or array being the most common) of 2d coordinates for each qubit. The length of the sequence much mast the number of qubits on the backend. The sequence should be the planar coordinates in a 0-based square grid where each qubit is located.

**Returns**

A matplotlib figure showing layout.

**Return type**

Figure

**Raises**

*   **QiskitError** – Invalid view type given.
*   [**VisualizationError**](qiskit.visualization.VisualizationError "qiskit.visualization.VisualizationError") – Circuit has no layout attribute.

## Example

```python
import numpy as np
from qiskit import QuantumCircuit, IBMQ, transpile
from qiskit.visualization import plot_histogram, plot_gate_map, plot_circuit_layout
from qiskit.tools.monitor import job_monitor
import matplotlib.pyplot as plt
%matplotlib inline

IBMQ.load_account()

ghz = QuantumCircuit(3, 3)
ghz.h(0)
for idx in range(1,3):
    ghz.cx(0,idx)
ghz.measure(range(3), range(3))

provider = IBMQ.get_provider(hub='ibm-q')
backend = provider.get_backend('ibmq_vigo')
new_circ_lv3 = transpile(ghz, backend=backend, optimization_level=3)
plot_circuit_layout(new_circ_lv3, backend)
```

![../\_images/qiskit.visualization.plot\_circuit\_layout\_1\_0.png](/images/api/qiskit/0.36/qiskit.visualization.plot_circuit_layout_1_0.png)
