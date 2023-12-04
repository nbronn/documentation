---
title: ManagedJobSet
description: API reference for qiskit.providers.ibmq.managed.ManagedJobSet
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.providers.ibmq.managed.ManagedJobSet
---

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

# ManagedJobSet[¶](#managedjobset "Permalink to this headline")

<span id="qiskit.providers.ibmq.managed.ManagedJobSet" />

`ManagedJobSet(name=None, short_id=None)`

Bases: `object`

A set of managed jobs.

An instance of this class is returned when you submit experiments using [`IBMQJobManager.run()`](qiskit.providers.ibmq.managed.IBMQJobManager#run "qiskit.providers.ibmq.managed.IBMQJobManager.run"). It provides methods that allow you to interact with the jobs as a single entity. For example, you can retrieve the results for all of the jobs using [`results()`](qiskit.providers.ibmq.managed.ManagedJobSet#results "qiskit.providers.ibmq.managed.ManagedJobSet.results") and cancel all jobs using [`cancel()`](qiskit.providers.ibmq.managed.ManagedJobSet#cancel "qiskit.providers.ibmq.managed.ManagedJobSet.cancel").

ManagedJobSet constructor.

**Parameters**

*   **name** (`Optional`\[`str`]) – Name for this set of jobs. If not specified, the current date and time is used.
*   **short\_id** (`Optional`\[`str`]) – Short ID for this set of jobs.

## Methods

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### cancel

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.cancel" />

`ManagedJobSet.cancel()`

Cancel all jobs in this job set.

**Return type**

`None`

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### error\_messages

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.error_messages" />

`ManagedJobSet.error_messages()`

Provide details about job failures.

This call will block until all jobs finish.

**Return type**

`Optional`\[`str`]

**Returns**

An error report if one or more jobs failed or `None` otherwise.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### job

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.job" />

`ManagedJobSet.job(experiment)`

Retrieve the job used to submit the specified experiment and its index.

For example, if [`IBMQJobManager`](qiskit.providers.ibmq.managed.IBMQJobManager "qiskit.providers.ibmq.managed.IBMQJobManager") is used to submit 1000 experiments, and [`IBMQJobManager`](qiskit.providers.ibmq.managed.IBMQJobManager "qiskit.providers.ibmq.managed.IBMQJobManager") divides them into 2 jobs: job 1 has experiments 0-499, and job 2 has experiments 500-999. In this case `job_set.job(501)` will return `(job2, 1)`.

**Parameters**

**experiment** (`Union`\[`str`, [`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.quantumcircuit.QuantumCircuit"), [`Schedule`](qiskit.pulse.Schedule "qiskit.pulse.schedule.Schedule"), `int`]) –

Retrieve the job used to submit this experiment. Several types are accepted for convenience:

> *   str: The name of the experiment.
> *   QuantumCircuit: The name of the circuit instance will be used.
> *   Schedule: The name of the schedule instance will be used.
> *   int: The position of the experiment.

**Return type**

`Tuple`\[`Optional`\[[`IBMQJob`](qiskit.providers.ibmq.job.IBMQJob "qiskit.providers.ibmq.job.ibmqjob.IBMQJob")], `int`]

**Returns**

A tuple of the job used to submit the experiment, or `None` if the job submit failed, and the experiment index.

**Raises**

[**IBMQJobManagerJobNotFound**](qiskit.providers.ibmq.managed.IBMQJobManagerJobNotFound "qiskit.providers.ibmq.managed.IBMQJobManagerJobNotFound") – If the job for the experiment could not be found.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### job\_set\_id

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.job_set_id" />

`ManagedJobSet.job_set_id()`

Return the ID of this job set.

**Return type**

`str`

**Returns**

ID of this job set.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### jobs

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.jobs" />

`ManagedJobSet.jobs()`

Return jobs in this job set.

**Return type**

`List`\[`Optional`\[[`IBMQJob`](qiskit.providers.ibmq.job.IBMQJob "qiskit.providers.ibmq.job.ibmqjob.IBMQJob")]]

**Returns**

A list of [`IBMQJob`](qiskit.providers.ibmq.job.IBMQJob "qiskit.providers.ibmq.job.IBMQJob") instances that represents the submitted jobs. An entry in the list is `None` if the job failed to be submitted.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### managed\_jobs

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.managed_jobs" />

`ManagedJobSet.managed_jobs()`

Return the managed jobs in this set.

**Return type**

`List`\[[`ManagedJob`](qiskit.providers.ibmq.managed.ManagedJob "qiskit.providers.ibmq.managed.managedjob.ManagedJob")]

**Returns**

A list of managed jobs.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### name

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.name" />

`ManagedJobSet.name()`

Return the name of this job set.

**Return type**

`str`

**Returns**

Name of this job set.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### qobjs

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.qobjs" />

`ManagedJobSet.qobjs()`

Return the Qobjs for the jobs in this set.

**Return type**

`List`\[`Union`\[[`QasmQobj`](qiskit.qobj.QasmQobj "qiskit.qobj.qasm_qobj.QasmQobj"), [`PulseQobj`](qiskit.qobj.PulseQobj "qiskit.qobj.pulse_qobj.PulseQobj")]]

**Returns**

A list of Qobjs for the jobs. An entry in the list is `None` if the Qobj could not be retrieved.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### report

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.report" />

`ManagedJobSet.report(detailed=True)`

Return a report on current job statuses.

**Parameters**

**detailed** (`bool`) – If `True`, return a detailed report. Otherwise return a summary report.

**Return type**

`str`

**Returns**

A report on job statuses.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### results

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.results" />

`ManagedJobSet.results(timeout=None, partial=False, refresh=False)`

Return the results of the jobs.

This call will block until all job results become available or the timeout is reached.

<Admonition title="Note" type="note">
  Some IBM Quantum Experience job results can only be read once. A second attempt to query the server for the same job will fail, since the job has already been “consumed”.

  The first call to this method in a `ManagedJobSet` instance will query the server and consume any available job results. Subsequent calls to that instance’s method will also return the results, since they are cached. However, attempting to retrieve the results again in another instance or session might fail due to the job results having been consumed.
</Admonition>

<Admonition title="Note" type="note">
  When partial=True, this method will attempt to retrieve partial results of failed jobs. In this case, precaution should be taken when accessing individual experiments, as doing so might cause an exception. The `success` attribute of the returned [`ManagedResults`](qiskit.providers.ibmq.managed.ManagedResults "qiskit.providers.ibmq.managed.ManagedResults") instance can be used to verify whether it contains partial results.

  For example, if one of the experiments failed, trying to get the counts of the unsuccessful experiment would raise an exception since there are no counts to return:

  ```python
  try:
      counts = managed_results.get_counts("failed_experiment")
  except QiskitError:
      print("Experiment failed!")
  ```
</Admonition>

**Parameters**

*   **timeout** (`Optional`\[`float`]) – Number of seconds to wait for job results.
*   **partial** (`bool`) – If `True`, attempt to retrieve partial job results.
*   **refresh** (`bool`) – If `True`, re-query the server for the result. Otherwise return the cached value.

**Return type**

[`ManagedResults`](qiskit.providers.ibmq.managed.ManagedResults "qiskit.providers.ibmq.managed.managedresults.ManagedResults")

**Returns**

A [`ManagedResults`](qiskit.providers.ibmq.managed.ManagedResults "qiskit.providers.ibmq.managed.ManagedResults") instance that can be used to retrieve results for individual experiments.

**Raises**

[**IBMQJobManagerTimeoutError**](qiskit.providers.ibmq.managed.IBMQJobManagerTimeoutError "qiskit.providers.ibmq.managed.IBMQJobManagerTimeoutError") – if unable to retrieve all job results before the specified timeout.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### retrieve\_jobs

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.retrieve_jobs" />

`ManagedJobSet.retrieve_jobs(provider, refresh=False)`

Retrieve previously submitted jobs in this set.

**Parameters**

*   **provider** ([`AccountProvider`](qiskit.providers.ibmq.AccountProvider "qiskit.providers.ibmq.accountprovider.AccountProvider")) – Provider used for this job set.
*   **refresh** (`bool`) – If `True`, re-query the server for the job set. Otherwise return the cached value.

**Raises**

*   [**IBMQJobManagerUnknownJobSet**](qiskit.providers.ibmq.managed.IBMQJobManagerUnknownJobSet "qiskit.providers.ibmq.managed.IBMQJobManagerUnknownJobSet") – If the job set cannot be found.
*   [**IBMQJobManagerInvalidStateError**](qiskit.providers.ibmq.managed.IBMQJobManagerInvalidStateError "qiskit.providers.ibmq.managed.IBMQJobManagerInvalidStateError") – If jobs for this job set are found but have unexpected attributes.

**Return type**

`None`

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### run

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.run" />

`ManagedJobSet.run(experiment_list, backend, executor, job_share_level=None, job_tags=None, **run_config)`

Execute a list of circuits or pulse schedules on a backend.

**Parameters**

*   **experiment\_list** (`Union`\[`List`\[`List`\[[`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.quantumcircuit.QuantumCircuit")]], `List`\[`List`\[[`Schedule`](qiskit.pulse.Schedule "qiskit.pulse.schedule.Schedule")]]]) – Circuit(s) or pulse schedule(s) to execute.
*   **backend** ([`IBMQBackend`](qiskit.providers.ibmq.IBMQBackend "qiskit.providers.ibmq.ibmqbackend.IBMQBackend")) – Backend to execute the experiments on.
*   **executor** (`ThreadPoolExecutor`) – The thread pool used to submit jobs asynchronously.
*   **job\_share\_level** (`Optional`\[`ApiJobShareLevel`]) – Job share level.
*   **job\_tags** (`Optional`\[`List`\[`str`]]) – Tags to be assigned to the job.
*   **run\_config** (`Any`) – Additional arguments used to configure the Qobj assembly. Refer to the [`qiskit.compiler.assemble()`](qiskit.compiler.assemble "qiskit.compiler.assemble") documentation for details on these arguments.

**Raises**

[**IBMQJobManagerInvalidStateError**](qiskit.providers.ibmq.managed.IBMQJobManagerInvalidStateError "qiskit.providers.ibmq.managed.IBMQJobManagerInvalidStateError") – If the jobs were already submitted.

**Return type**

`None`

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### statuses

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.statuses" />

`ManagedJobSet.statuses()`

Return the status of each job in this set.

**Return type**

`List`\[`Optional`\[[`JobStatus`](qiskit.providers.JobStatus "qiskit.providers.jobstatus.JobStatus")]]

**Returns**

A list of job statuses. An entry in the list is `None` if the job status could not be retrieved due to a server error.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### tags

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.tags" />

`ManagedJobSet.tags()`

Return the tags assigned to this job set.

**Return type**

`List`\[`str`]

**Returns**

Tags assigned to this job set.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### update\_name

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.update_name" />

`ManagedJobSet.update_name(name)`

Update the name of this job set.

**Parameters**

**name** (`str`) – The new name for this job set.

**Return type**

`str`

**Returns**

The new name associated with this job set.

<Admonition title="Warning" type="caution">
  The package `qiskit-ibmq-provider` is being deprecated and its repo is going to be archived soon. Please transition to the new packages. More information in [https://ibm.biz/provider\_migration\_guide](https://ibm.biz/provider_migration_guide)
</Admonition>

### update\_tags

<span id="qiskit.providers.ibmq.managed.ManagedJobSet.update_tags" />

`ManagedJobSet.update_tags(replacement_tags=None, additional_tags=None, removal_tags=None)`

Update the tags assigned to this job set.

When multiple parameters are specified, the parameters are processed in the following order:

> 1.  replacement\_tags
> 2.  additional\_tags
> 3.  removal\_tags

For example, if ‘new\_tag’ is specified for both additional\_tags and removal\_tags, then it is added and subsequently removed from the tags list, making it a “do nothing” operation.

<Admonition title="Note" type="note">
  *   Some tags, such as those starting with `ibmq_jobset`, are used internally by ibmq-provider and therefore cannot be modified.
  *   When removing tags, if the job does not have a specified tag, it will be ignored.
</Admonition>

**Parameters**

*   **replacement\_tags** (`Optional`\[`List`\[`str`]]) – The tags that should replace the current tags associated with this job set.
*   **additional\_tags** (`Optional`\[`List`\[`str`]]) – The new tags that should be added to the current tags associated with this job set.
*   **removal\_tags** (`Optional`\[`List`\[`str`]]) – The tags that should be removed from the current tags associated with this job set.

**Return type**

`List`\[`str`]

**Returns**

The new tags associated with this job set.

**Raises**

[**IBMQJobManagerInvalidStateError**](qiskit.providers.ibmq.managed.IBMQJobManagerInvalidStateError "qiskit.providers.ibmq.managed.IBMQJobManagerInvalidStateError") – If none of the input parameters are specified.
