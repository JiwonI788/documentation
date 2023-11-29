---
title: utils
description: API reference for qiskit.utils
in_page_toc_min_heading_level: 1
python_api_type: module
python_api_name: qiskit.utils
---

<span id="module-qiskit.utils" />

<span id="qiskit-utils" />

# Utilities

<span id="module-qiskit.utils" />

`qiskit.utils¶`

|                                                                                                                         |                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| [`deprecate_arguments`](qiskit.utils.deprecate_arguments "qiskit.utils.deprecate_arguments")(kwarg\_map\[, category])   | Decorator to automatically alias deprecated argument names and warn upon use.                                   |
| [`deprecate_function`](qiskit.utils.deprecate_function "qiskit.utils.deprecate_function")(msg\[, stacklevel, category]) | Emit a warning prior to calling decorated function.                                                             |
| [`local_hardware_info`](qiskit.utils.local_hardware_info "qiskit.utils.local_hardware_info")()                          | Basic hardware information about the local machine.                                                             |
| [`is_main_process`](qiskit.utils.is_main_process "qiskit.utils.is_main_process")()                                      | Checks whether the current process is the main one                                                              |
| [`apply_prefix`](qiskit.utils.apply_prefix "qiskit.utils.apply_prefix")(value, unit)                                    | Given a SI unit prefix and value, apply the prefix to convert to standard SI unit.                              |
| [`detach_prefix`](qiskit.utils.detach_prefix "qiskit.utils.detach_prefix")(value\[, decimal])                           | Given a SI unit value, find the most suitable prefix to scale the value.                                        |
| [`wrap_method`](qiskit.utils.wrap_method "qiskit.utils.wrap_method")(cls, name, \*\[, before, after])                   | Wrap the functionality the instance- or class method `cls.name` with additional behaviour `before` and `after`. |

## Algorithm Utilities

<span id="module-qiskit.utils" />

`¶`

|                                                                                                                       |                                                                              |
| --------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [`summarize_circuits`](qiskit.utils.summarize_circuits "qiskit.utils.summarize_circuits")                             | Summarize circuits based on QuantumCircuit, and five metrics are summarized. |
| [`get_entangler_map`](qiskit.utils.get_entangler_map "qiskit.utils.get_entangler_map")                                | Utility method to get an entangler map among qubits.                         |
| [`validate_entangler_map`](qiskit.utils.validate_entangler_map "qiskit.utils.validate_entangler_map")                 | Validate a user supplied entangler map and converts entries to ints.         |
| [`has_ibmq`](qiskit.utils.has_ibmq "qiskit.utils.has_ibmq")                                                           | Check if IBMQ is installed                                                   |
| [`has_aer`](qiskit.utils.has_aer "qiskit.utils.has_aer")                                                              | check if Aer is installed                                                    |
| [`name_args`](qiskit.utils.name_args "qiskit.utils.name_args")                                                        | Decorator to convert unnamed arguments to named ones.                        |
| [`algorithm_globals`](qiskit.utils.algorithm_globals#qiskit.utils.algorithm_globals "qiskit.utils.algorithm_globals") | Class for global properties.                                                 |

|                                                                                  |                                              |
| -------------------------------------------------------------------------------- | -------------------------------------------- |
| [`QuantumInstance`](qiskit.utils.QuantumInstance "qiskit.utils.QuantumInstance") | Quantum Backend including execution setting. |

A QuantumInstance holds the Qiskit backend as well as a number of compile and runtime parameters controlling circuit compilation and execution. Quantum [`algorithms`](algorithms#module-qiskit.algorithms "qiskit.algorithms") are run on a device or simulator by passing a QuantumInstance setup with the desired backend etc.

<span id="optional-depedency-checkers-qiskit-utils-optionals" />

## Optional Depedency Checkers

<span id="module-qiskit.utils" />

`qiskit.utils.optionals¶`

Qiskit Terra, and many of the other Qiskit components, have several features that are enabled only if certain *optional* dependencies are satisfied. This module is a collection of objects that can be used to test if certain functionality is available, and optionally raise `MissingOptionalLibraryError` if the functionality is not available.

### Available Testers[¶](#available-testers "Permalink to this headline")

#### Qiskit Components[¶](#qiskit-components "Permalink to this headline")

|                |                                                                                                                                                                               |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **HAS\_AER**   | `Qiskit Aer` provides high-performance simulators for the quantum circuits constructed within Qiskit Terra.                                                                   |
| **HAS\_IBMQ**  | The [`Qiskit IBMQ Provider`](ibmq_provider#module-qiskit.providers.ibmq "qiskit.providers.ibmq") is used for accessing IBM Quantum hardware in the IBM cloud.                 |
| **HAS\_IGNIS** | `Qiskit Ignis` provides tools for quantum hardware verification, noise characterization, and error correction.                                                                |
| **HAS\_TOQM**  | [Qiskit TOQM](https://github.com/qiskit-toqm/qiskit-toqm) provides transpiler passes for the [Time-optimal Qubit mapping algorithm](https://doi.org/10.1145/3445814.3446706). |

#### External Python Libraries[¶](#external-python-libraries "Permalink to this headline")

|                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **HAS\_CONSTRAINT**    | python-constraint \<[https://github.com/python-constraint/python-constraint>\_\_](https://github.com/python-constraint/python-constraint>__) is a constraint satisfaction problem solver, used in the :class:\`\~.CSPLayout transpiler pass.                                                                                                                                                                                                         |
| **HAS\_CPLEX**         | The [IBM CPLEX Optimizer](https://www.ibm.com/analytics/cplex-optimizer) is a high-performance mathematical programming solver for linear, mixed-integer and quadratic programming. It is required by the [`BIPMapping`](qiskit.transpiler.passes.BIPMapping "qiskit.transpiler.passes.BIPMapping") transpiler pass.                                                                                                                                 |
| **HAS\_CVXPY**         | [CVXPY](https://www.cvxpy.org/) is a Python package for solving convex optimization problems. It is required for calculating diamond norms with [`quantum_info.diamond_norm()`](qiskit.quantum_info.diamond_norm "qiskit.quantum_info.diamond_norm").                                                                                                                                                                                                |
| **HAS\_DOCPLEX**       | [IBM Decision Optimization CPLEX Modelling](http://ibmdecisionoptimization.github.io/docplex-doc/) is a library for prescriptive analysis. Like CPLEX, it is required for the [`BIPMapping`](qiskit.transpiler.passes.BIPMapping "qiskit.transpiler.passes.BIPMapping") transpiler pass.                                                                                                                                                             |
| **HAS\_FIXTURES**      | The test suite has additional features that are available if the optional [fixtures](https://launchpad.net/python-fixtures) module is installed. This generally also needs [`HAS_TESTTOOLS`](#qiskit.utils.optionals.HAS_TESTTOOLS "qiskit.utils.optionals.HAS_TESTTOOLS") as well. This is generally only needed for Qiskit developers.                                                                                                             |
| **HAS\_IPYTHON**       | If [the IPython kernel](https://ipython.org/) is available, certain additional visualisations and line magics are made available.                                                                                                                                                                                                                                                                                                                    |
| **HAS\_IPYWIDGETS**    | Monitoring widgets for jobs running on external backends can be provided if [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/) is available.                                                                                                                                                                                                                                                                                                 |
| **HAS\_JAX**           | Some methods of gradient calculation within [`opflow.gradients`](qiskit.opflow.gradients#module-qiskit.opflow.gradients "qiskit.opflow.gradients") require [JAX](https://github.com/google/jax) for autodifferentiation.                                                                                                                                                                                                                             |
| **HAS\_MATPLOTLIB**    | Qiskit Terra provides several visualisation tools in the [`visualization`](visualization#module-qiskit.visualization "qiskit.visualization") module. Almost all of these are built using [Matplotlib](https://matplotlib.org/), which must be installed in order to use them.                                                                                                                                                                        |
| **HAS\_NETWORKX**      | No longer used by Terra. Internally, Qiskit now uses the high-performance [rustworkx](https://github.com/Qiskit/rustworkx) library as a core dependency, and during the change-over period, it was sometimes convenient to convert things into the Python-only [NetworkX](https://networkx.org/) format. Some tests of application modules, such as [Qiskit Nature](https://qiskit.org/documentation/nature/) still use NetworkX.                    |
| **HAS\_NLOPT**         | [NLopt](https://nlopt.readthedocs.io/en/latest/) is a nonlinear optimization library, used by the global optimizers in the [`algorithms.optimizers`](qiskit.algorithms.optimizers#module-qiskit.algorithms.optimizers "qiskit.algorithms.optimizers") module.                                                                                                                                                                                        |
| **HAS\_PIL**           | PIL is a Python image-manipulation library. Qiskit actually uses the [pillow](https://pillow.readthedocs.io/en/stable/) fork of PIL if it is available when generating certain visualizations, for example of both [`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit") and [`DAGCircuit`](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit") in certain modes.                                               |
| **HAS\_PYDOT**         | For some graph visualisations, Qiskit uses [pydot](https://github.com/pydot/pydot) as an interface to GraphViz (see [`HAS_GRAPHVIZ`](#qiskit.utils.optionals.HAS_GRAPHVIZ "qiskit.utils.optionals.HAS_GRAPHVIZ")).                                                                                                                                                                                                                                   |
| **HAS\_PYLATEX**       | Various LaTeX-based visualizations, especially the circuit drawers, need access to the [pylatexenc](https://github.com/phfaist/pylatexenc) project to work correctly.                                                                                                                                                                                                                                                                                |
| **HAS\_QASM3\_IMPORT** | The functions [`qasm3.load()`](qasm3#qiskit.qasm3.load "qiskit.qasm3.load") and [`qasm3.loads()`](qasm3#qiskit.qasm3.loads "qiskit.qasm3.loads") for importing OpenQASM 3 programs into [`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit") instances use [an external importer package](https://qiskit.github.io/qiskit-qasm3-import).                                                                                |
| **HAS\_SEABORN**       | Qiskit Terra provides several visualisation tools in the [`visualization`](visualization#module-qiskit.visualization "qiskit.visualization") module. Some of these are built using [Seaborn](https://seaborn.pydata.org/), which must be installed in order to use them.                                                                                                                                                                             |
| **HAS\_SKLEARN**       | Some of the gradient functions in [`opflow.gradients`](qiskit.opflow.gradients#module-qiskit.opflow.gradients "qiskit.opflow.gradients") use regularisation methods from [Scikit Learn](https://scikit-learn.org/stable/).                                                                                                                                                                                                                           |
| **HAS\_SKQUANT**       | Some of the optimisers in [`algorithms.optimizers`](qiskit.algorithms.optimizers#module-qiskit.algorithms.optimizers "qiskit.algorithms.optimizers") are based on those found in [Scikit Quant](https://github.com/scikit-quant/scikit-quant), which must be installed to use them.                                                                                                                                                                  |
| **HAS\_SQSNOBFIT**     | [SQSnobFit](https://pypi.org/project/SQSnobFit/) is a library for the “stable noisy optimization by branch and fit” algorithm. It is used by the [`SNOBFIT`](qiskit.algorithms.optimizers.SNOBFIT "qiskit.algorithms.optimizers.SNOBFIT") optimizer.                                                                                                                                                                                                 |
| **HAS\_SYMENGINE**     | [Symengine](https://github.com/symengine/symengine) is a fast C++ backend for the symbolic-manipulation library [Sympy](https://www.sympy.org/en/index.html). Qiskit uses special methods from Symengine to accelerate its handling of [`Parameter`](qiskit.circuit.Parameter "qiskit.circuit.Parameter")s if available.                                                                                                                             |
| **HAS\_TESTTOOLS**     | Qiskit Terra’s test suite has more advanced functionality available if the optional [testtools](https://pypi.org/project/testtools/) library is installed. This is generally only needed for Qiskit developers.                                                                                                                                                                                                                                      |
| **HAS\_TWEEDLEDUM**    | [Tweedledum](https://github.com/boschmitt/tweedledum) is an extension library for synthesis and optimization of circuits that may involve classical oracles. Qiskit Terra’s [`PhaseOracle`](qiskit.circuit.library.PhaseOracle "qiskit.circuit.library.PhaseOracle") uses this, which is used in turn by amplification algorithms via the [`AmplificationProblem`](qiskit.algorithms.AmplificationProblem "qiskit.algorithms.AmplificationProblem"). |
| **HAS\_Z3**            | [Z3](https://github.com/Z3Prover/z3) is a theorem prover, used in the [`CrosstalkAdaptiveSchedule`](qiskit.transpiler.passes.CrosstalkAdaptiveSchedule "qiskit.transpiler.passes.CrosstalkAdaptiveSchedule") and [`HoareOptimizer`](qiskit.transpiler.passes.HoareOptimizer "qiskit.transpiler.passes.HoareOptimizer") transpiler passes.                                                                                                            |

#### External Command-Line Tools[¶](#external-command-line-tools "Permalink to this headline")

|                     |                                                                                                                                                                                                                                              |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **HAS\_GRAPHVIZ**   | For some graph visualisations, Qiskit uses the [GraphViz](https://graphviz.org/) visualisation tool via its `pydot` interface (see [`HAS_PYDOT`](#qiskit.utils.optionals.HAS_PYDOT "qiskit.utils.optionals.HAS_PYDOT")).                     |
| **HAS\_PDFLATEX**   | Visualisation tools that use LaTeX in their output, such as the circuit drawers, require `pdflatex` to be available. You will generally need to ensure that you have a working LaTeX installation available, and the `qcircuit.tex` package. |
| **HAS\_PDFTOCAIRO** | Visualisation tools that convert LaTeX-generated files into rasterised images use the `pdftocairo` tool. This is part of the [Poppler suite of PDF tools](https://poppler.freedesktop.org/).                                                 |

### Lazy Checker Classes[¶](#lazy-checker-classes "Permalink to this headline")

Each of the lazy checkers is an instance of [`LazyDependencyManager`](#qiskit.utils.LazyDependencyManager "qiskit.utils.LazyDependencyManager") in one of its two subclasses: [`LazyImportTester`](#qiskit.utils.LazyImportTester "qiskit.utils.LazyImportTester") and [`LazySubprocessTester`](#qiskit.utils.LazySubprocessTester "qiskit.utils.LazySubprocessTester"). These should be imported from [`utils`](aer_utils#module-qiskit_aer.utils "qiskit_aer.utils") directly if required, such as:

```python
from qiskit.utils import LazyImportTester
```

<span id="qiskit.utils.LazyDependencyManager" />

`LazyDependencyManager(*, name=None, callback=None, install=None, msg=None)`

A mananger for some optional features that are expensive to import, or to verify the existence of.

These objects can be used as Booleans, such as `if x`, and will evaluate `True` if the dependency they test for is available, and `False` if not. The presence of the dependency will only be tested when the Boolean is evaluated, so it can be used as a runtime test in functions and methods without requiring an import-time test.

These objects also encapsulate the error handling if their dependency is not present, so you can do things such as:

```python
from qiskit.utils import LazyImportManager
HAS_MATPLOTLIB = LazyImportManager("matplotlib")

@HAS_MATPLOTLIB.require_in_call
def my_visualisation():
    ...

def my_other_visualisation():
    # ... some setup ...
    HAS_MATPLOTLIB.require_now("my_other_visualisation")
    ...

def my_third_visualisation():
    if HAS_MATPLOTLIB:
        from matplotlib import pyplot
    else:
        ...
```

In all of these cases, `matplotlib` is not imported until the functions are entered. In the case of the decorator, `matplotlib` is tested for import when the function is called for the first time. In the second and third cases, the loader attempts to import `matplotlib` when the [`require_now()`](#qiskit.utils.LazyDependencyManager.require_now "qiskit.utils.LazyDependencyManager.require_now") method is called, or when the Boolean context is evaluated. For the `require` methods, an error is raised if the library is not available.

This is the base class, which provides the Boolean context checking and error management. The concrete classes [`LazyImportTester`](#qiskit.utils.LazyImportTester "qiskit.utils.LazyImportTester") and [`LazySubprocessTester`](#qiskit.utils.LazySubprocessTester "qiskit.utils.LazySubprocessTester") provide convenient entry points for testing that certain symbols are importable from modules, or certain command-line tools are available, respectively.

**Parameters**

*   **name** – the name of this optional dependency.
*   **callback** – a callback that is called immediately after the availability of the library is tested with the result. This will only be called once.
*   **install** – how to install this optional dependency. Passed to `MissingOptionalLibraryError` as the `pip_install` parameter.
*   **msg** – an extra message to include in the error raised if this is required.

### \_is\_available

<span id="qiskit.utils.LazyDependencyManager._is_available" />

`abstract _is_available()`

Subclasses of [`LazyDependencyManager`](#qiskit.utils.LazyDependencyManager "qiskit.utils.LazyDependencyManager") should override this method to implement the actual test of availability. This method should return a Boolean, where `True` indicates that the dependency was available. This method will only ever be called once.

**Return type**

`bool`

### disable\_locally

<span id="qiskit.utils.LazyDependencyManager.disable_locally" />

`disable_locally()`

Create a context, during which the value of the dependency manager will be `False`. This means that within the context, any calls to this object will behave as if the dependency is not available, including raising errors. It is valid to call this method whether or not the dependency has already been evaluated. This is most useful in tests.

### require\_in\_call

### require\_in\_call

<span id="qiskit.utils.LazyDependencyManager.require_in_call" />

`require_in_call(feature_or_callable: Callable) → Callable`

<span id="qiskit.utils.LazyDependencyManager.require_in_call" />

`require_in_call(feature_or_callable: str) → Callable[[Callable], Callable]`

Create a decorator for callables that requires that the dependency is available when the decorated function or method is called.

**Parameters**

**feature\_or\_callable** (*str or Callable*) – the name of the feature that requires these dependencies. If this function is called directly as a decorator (for example `@HAS_X.require_in_call` as opposed to `@HAS_X.require_in_call("my feature")`), then the feature name will be taken to be the function name, or class and method name as appropriate.

**Returns**

a decorator that will make its argument require this dependency before it is called.

**Return type**

Callable

### require\_in\_instance

### require\_in\_instance

<span id="qiskit.utils.LazyDependencyManager.require_in_instance" />

`require_in_instance(feature_or_class: Type) → Type`

<span id="qiskit.utils.LazyDependencyManager.require_in_instance" />

`require_in_instance(feature_or_class: str) → Callable[[Type], Type]`

A class decorator that requires the dependency is available when the class is initialised. This decorator can be used even if the class does not define an `__init__` method.

**Parameters**

**feature\_or\_class** (*str or Type*) – the name of the feature that requires these dependencies. If this function is called directly as a decorator (for example `@HAS_X.require_in_instance` as opposed to `@HAS_X.require_in_instance("my feature")`), then the feature name will be taken as the name of the class.

**Returns**

a class decorator that ensures that the wrapped feature is present if the class is initialised.

**Return type**

Callable

### require\_now

<span id="qiskit.utils.LazyDependencyManager.require_now" />

`require_now(feature)`

Eagerly attempt to import the dependencies in this object, and raise an exception if they cannot be imported.

**Parameters**

**feature** (`str`) – the name of the feature that is requiring these dependencies.

**Raises**

**MissingOptionalLibraryError** – if the dependencies cannot be imported.

<span id="qiskit.utils.LazyImportTester" />

`LazyImportTester(name_map_or_modules, *, name=None, callback=None, install=None, msg=None)`

A lazy dependency tester for importable Python modules. Any required objects will only be imported at the point that this object is tested for its Boolean value.

**Parameters**

**name\_map\_or\_modules** (`Union`\[`str`, `Dict`\[`str`, `Iterable`\[`str`]], `Iterable`\[`str`]]) – if a name map, then a dictionary where the keys are modules or packages, and the values are iterables of names to try and import from that module. It should be valid to write `from <module> import <name1>, <name2>, ...`. If simply a string or iterable of strings, then it should be valid to write `import <module>` for each of them.

**Raises**

**ValueError** – if no modules are given.

<span id="qiskit.utils.LazySubprocessTester" />

`LazySubprocessTester(command, *, name=None, callback=None, install=None, msg=None)`

A lazy checker that a command-line tool is available. The command will only be run once, at the point that this object is checked for its Boolean value.

**Parameters**

**command** (`Union`\[`str`, `Iterable`\[`str`]]) – the strings that make up the command to be run. For example, `["pdflatex", "-version"]`.

**Raises**

**ValueError** – if an empty command is given.
