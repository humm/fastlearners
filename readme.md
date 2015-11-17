## fastlearners

`fastlearners` contains C++ implementations of some algorithms of the [learners](http://https://github.com/humm/learners) library. Once installed, the `learners` library will automatically and transparently make use of the faster implementations.

This code was designed and written in order to conduct scientific experiments. It is probably not fit for any other purpose, and certainly not for production environments. In particular, its maintenance and future depends on the direction of future research. That being said, do not hesitate to submit issues or contact me by mail for questions and comments.

### OpenScience License

This software is placed under the [OpenScience license](http://fabien.benureau.com/openscience.html), which is the LGPL, with the additional condition that if you publish scientific results using this code, you have to publish the corresponding modifications of the code.

> If you publicly release any scientific claims or data that were supported or generated by the Program or a modification thereof, in whole or in part, you will release any modifications you made to the Program. This License will be in effect for the modified program.

### Installation

1. Install [eigen3](http://eigen.tuxfamily.org/)
1. `pip install numpy fastlearners`

### Usage

`fastlearners` will automatically be used by the `learners` package. Should this not be desired, `fastlearners` should be uninstalled (`pip uninstall fastlearners`) or learners should be imported with:
```python
import learners
learners.disable_fastlearners()
```

Let's remark that should the import of `fastlearners` by the `learners` module fail, the `learners` module will silently revert to python implementation. To display a warning message when that happen, `learners` should be imported with:
```python
import learners
learners.enable_fastlearners(silent_fail=False)
```
