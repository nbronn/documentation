---
title: U1Gate
description: API reference for qiskit.circuit.library.U1Gate
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.circuit.library.U1Gate
---

# U1Gate

<span id="qiskit.circuit.library.U1Gate" />

`qiskit.circuit.library.U1Gate(theta, label=None, *, duration=None, unit='dt')`[GitHub](https://github.com/qiskit/qiskit/tree/stable/1.0/qiskit/circuit/library/standard_gates/u1.py "view source code")

Bases: [`Gate`](qiskit.circuit.Gate "qiskit.circuit.gate.Gate")

Single-qubit rotation about the Z axis.

This is a diagonal gate. It can be implemented virtually in hardware via framechanges (i.e. at zero error and duration).

<Admonition title="Warning" type="caution">
  This gate is deprecated. Instead, the following replacements should be used

  $$
  U1(\lambda) = P(\lambda)= U(0,0,\lambda)
  $$

  ```python
  circuit = QuantumCircuit(1)
  circuit.p(lambda, 0) # or circuit.u(0, 0, lambda)
  ```
</Admonition>

**Circuit symbol:**

```python
     ┌───────┐
q_0: ┤ U1(λ) ├
     └───────┘
```

**Matrix Representation:**

$$
U1(\lambda) =
    \begin{pmatrix}
        1 & 0 \\
        0 & e^{i\lambda}
    \end{pmatrix}
$$

**Examples:**

> $$
> U1(\lambda = \pi) = Z
> $$
>
> $$
> U1(\lambda = \pi/2) = S
> $$
>
> $$
> U1(\lambda = \pi/4) = T
> $$

<Admonition title="See also" type="note">
  `RZGate`: This gate is equivalent to RZ up to a phase factor.

  > $$
  > U1(\lambda) = e^{i{\lambda}/2} RZ(\lambda)
  > $$

  `U3Gate`: U3 is a generalization of U2 that covers all single-qubit rotations, using two X90 pulses.

  Reference for virtual Z gate implementation: [1612.00858](https://arxiv.org/abs/1612.00858)
</Admonition>

Create new U1 gate.

## Attributes

<span id="qiskit.circuit.library.U1Gate.base_class" />

### base\_class

Get the base class of this instruction. This is guaranteed to be in the inheritance tree of `self`.

The “base class” of an instruction is the lowest class in its inheritance tree that the object should be considered entirely compatible with for \_all\_ circuit applications. This typically means that the subclass is defined purely to offer some sort of programmer convenience over the base class, and the base class is the “true” class for a behavioural perspective. In particular, you should *not* override [`base_class`](#qiskit.circuit.library.U1Gate.base_class "qiskit.circuit.library.U1Gate.base_class") if you are defining a custom version of an instruction that will be implemented differently by hardware, such as an alternative measurement strategy, or a version of a parametrised gate with a particular set of parameters for the purposes of distinguishing it in a [`Target`](qiskit.transpiler.Target "qiskit.transpiler.Target") from the full parametrised gate.

This is often exactly equivalent to `type(obj)`, except in the case of singleton instances of standard-library instructions. These singleton instances are special subclasses of their base class, and this property will return that base. For example:

```python
>>> isinstance(XGate(), XGate)
True
>>> type(XGate()) is XGate
False
>>> XGate().base_class is XGate
True
```

In general, you should not rely on the precise class of an instruction; within a given circuit, it is expected that `Instruction.name` should be a more suitable discriminator in most situations.

<span id="qiskit.circuit.library.U1Gate.condition" />

### condition

The classical condition on the instruction.

<span id="qiskit.circuit.library.U1Gate.condition_bits" />

### condition\_bits

Get Clbits in condition.

<span id="qiskit.circuit.library.U1Gate.decompositions" />

### decompositions

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="qiskit.circuit.library.U1Gate.definition" />

### definition

Return definition in terms of other basic gates.

<span id="qiskit.circuit.library.U1Gate.duration" />

### duration

Get the duration.

<span id="qiskit.circuit.library.U1Gate.label" />

### label

Return instruction label

<span id="qiskit.circuit.library.U1Gate.mutable" />

### mutable

Is this instance is a mutable unique instance or not.

If this attribute is `False` the gate instance is a shared singleton and is not mutable.

<span id="qiskit.circuit.library.U1Gate.name" />

### name

Return the name.

<span id="qiskit.circuit.library.U1Gate.num_clbits" />

### num\_clbits

Return the number of clbits.

<span id="qiskit.circuit.library.U1Gate.num_qubits" />

### num\_qubits

Return the number of qubits.

<span id="qiskit.circuit.library.U1Gate.params" />

### params

return instruction params.

<span id="qiskit.circuit.library.U1Gate.unit" />

### unit

Get the time unit of duration.

## Methods

### control

<span id="qiskit.circuit.library.U1Gate.control" />

`control(num_ctrl_qubits=1, label=None, ctrl_state=None, annotated=False)`

Return a (multi-)controlled-U1 gate.

**Parameters**

*   **num\_ctrl\_qubits** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.12)")) – number of control qubits.
*   **label** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.12)") *or None*) – An optional label for the gate \[Default: None]
*   **ctrl\_state** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.12)")  *or*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.12)") *or None*) – control state expressed as integer, string (e.g. ‘110’), or None. If None, use all 1s.
*   **annotated** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.12)")) – indicates whether the controlled gate can be implemented as an annotated gate.

**Returns**

controlled version of this gate.

**Return type**

[ControlledGate](qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate")

### inverse

<span id="qiskit.circuit.library.U1Gate.inverse" />

`inverse(annotated=False)`

Return inverted U1 gate ($U1(\lambda)^{\dagger} = U1(-\lambda)$)
