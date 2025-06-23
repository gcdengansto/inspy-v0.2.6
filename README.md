inspy
=========

.. warning::
    New releases may not be backwards compatibile. This software is in a fluid state and undergoes rapid changes. Bug fix and maintanence releases will generally be  backwards compatibile updates. Major number releases (x.0) could potentially break backwards compatibility, but users will be notified in the changelog.

.. warning::
    Official support for Python 2.7 and Python 3.3 has been discontinued. inspy may continue to work with these versions, but automatic testing for these versions is no longer performed, therefore compatibility cannot be guaranteed. CI tests also no longer run on OSX, but no compatibility issues are expected due to the source-only nature of this package.




inspy is a python library with commonly used tools for neutron scattering measurements, primarily for Triple Axis Spectrometer data, but easily applied to other types of data, including some *reduced* Time of Flight data. Below is a non-exhaustive list of Neutronpy's features:

    * Triple Axis Spectrometer resolution function calculation (based on ResLib), including
        * Resolution ellipses
        * Instrument visualization
        * Convolution
        * Convolution Fitting
    * Time of Flight Spectrometer resolution function calculation (not yet implemented) 
        * Resolution ellipses (not yet implemented) 
    * Least-Squares fitting (custom interface for scipy.optimize.leastsq using lmfit features), including
        * Built-in physical models





Inspy is a python package to conduct the resolution calculation for the inelastic neutron scattering experiment with triple-axis spectrometers or time-of-flight spectrometers. 
Inspy is developed on the basis of another python package, namely, Neutronpy, which was developed by David M Fobes by translating the functions in Reslib3.4c by Andrew Zheludev. 
Inspy involves significant upgrades in comparison to Neutronpy. Inspy is able to do the 3D resolution calculation and plot 3D resolution functions, fit the triple-axis spectrometer
by convolting the instrument resolution. The bugs in the resolution calculation GUI have been corrected. Two GUI interfaces were implemented to do the reolsution calcualtion and data fitting. 
inspy is a work-in-progress (see the `Roadmap <https://github.com/inspy/inspy/wiki/Roadmap>`_ in the wiki for indications of new upcoming features) and as such, still has many bugs, so use at your own risk; see Disclaimer. To report bugs or suggest features see Contributions.

Requirements
------------
The following packages are required to install this library:

* ``Python >= 3.4 (incl. Python 3.4-3.6)``
* ``numpy >= 1.10.0``
* ``scipy >= 1.0.0``
* ``lmfit >= 1.0.2``
* ``matplotlib >= 3.1.0``
* ``h5py``

The following package is required to use the ``inspy`` entry-point gui optional feature

* ``pyqt5 >= 5.4.1``

The following packages are required to test this library:

* ``pytest >= 3``
* ``mock``


Installation
------------

Local installation: go to the folder of inspy
    pip install -e .

See Installation for more detailed instructions.

Documentation
-------------
Documentation is available at `inspy.github.io <https://inspy.github.io/>`_, 
Building documentation requires the following additional packages:

* ``sphinx>=1.4``
* ``releases>=1.5.0``
* ``numpydoc>=0.8.0``
* ``inspy_rtd_sphinx_theme``

Contributions
-------------
Contributions may be made by submitting a pull-request for review using the fork-and-pull method on GitHub. Feature requests and bug reports can be made using the GitHub issues interface. Please read the `development guide <https://inspy.github.io/development.html>`_ for details on how to best contribute.



Copyright & Licensing
---------------------
Copyright (c) 2019-2025, Guochu Deng, Released under terms in LICENSE.

The source code of Inspy is partially from the python package Neutronpy (<https://neutronpy.github.io/>, which was developed by David M Fobes) after tests and fixing bugs.
The source code for the Triple Axis Spectrometer resolution calculations was partially based on or translated from the MATLAB library ResLib 3.4c (<http://www.neutron.ethz.ch/research/resources/reslib>`  which was originally developed by Andrey Zheludev, ETH Zuerich. email: zhelud@ethz.ch).

Disclaimer
----------
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
