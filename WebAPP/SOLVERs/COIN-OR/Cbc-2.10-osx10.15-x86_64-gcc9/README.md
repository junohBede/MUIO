# Cbc 2.10.12

[![A COIN-OR Project](https://coin-or.github.io/coin-or-badge.png)](https://www.coin-or.org)

Projects such as this one are maintained by a small group of volunteers under
the auspices of the non-profit [COIN-OR Foundation](https://www.coin-or.org)
and we need your help! Please consider [sponsoring our
activities](https://github.com/sponsors/coin-or) or [volunteering](mailto:volunteer@coin-or.org) to help!

[![Latest Release](https://img.shields.io/github/v/release/coin-or/Cbc?sort=semver)](https://github.com/coin-or/Cbc/releases)

_This file is auto-generated from [config.yml](.coin-or/config.yml) using the 
[generate_readme](.coin-or/generate_readme) script.
To make changes, please edit [config.yml](.coin-or/config.yml) or the generation scripts
[here](.coin-or/generate_readme) and [here](https://github.com/coin-or/coinbrew/blob/master/scripts/generate_readme)._

Cbc (*C*oin-or *b*ranch and *c*ut) is an open-source mixed integer linear programming solver written in C++.
It can be used as a callable library or using a stand-alone executable.
It can be used in a wide variety of ways through various modeling systems, packages, etc. 
 * Stand-alone modeling languages and systems
   * AIMMS (via the [AIMMSlinks](https://github.com/coin-or/AIMMSlinks) project),
   * AMPL (natively),
   * [CMPL](https://github.com/coin-or/Cmpl),
   * GAMS (through the [GAMSlinks](https://github.com/coin-or/GAMSlinks) project),
   * Mathematica,
   * Matlab (https://inverseproblem.co.nz/OPTI/)
   * [MiniZinc](http://www.minizinc.org/),
   * MPL (through the [CoinMP](https://github.com/coin-or/CoinMP) project),
   * R (https://rdrr.io/github/yuehmeir2/myFormAssembler/man/cbc.html)
 * Python-based modeling languages and extensions
   * [cbcpy](https://pypi.org/project/cbcpy).
   * [cvxpy](https://github.com/cvxpy/cvxpy)
   * [CyLP](https://github.com/coin-or/CyLP),
   * [Google's or-tools](https://developers.google.com/optimization),
   * [PuLP](https://github.com/coin-or/PuLP)/[DiPPy](https://github.com/coin-or/Dip),
   * [python-mip](https://github.com/coin-or/python-mip),
   * [yaposib](https://github.com/coin-or/yaposib)
 * Extensions in other languages
   * [JuMP](https://github.com/JuliaOpt/JuMP.jl) (Julia),
   * [rust-lp-modeler](https://github.com/jcavat/rust-lp-modeler) (Rust)
   * [good_lp](https://github.com/rust-or/good_lp) (Rust)
 * Spreadsheet extensions
   * [OpenSolver for Excel](http://opensolver.org)
   * [OpenSolver for Google Sheets](https://opensolver.org/opensolver-for-google-sheets/)

Binaries for most platforms are available for download from
[Bintray](https://bintray.com/coin-or/download/Cbc). AMPL also provides
stand-alone [Cbc
executables](http://ampl.com/products/solvers/open-source/#cbc) that can be
used with (or without) AMPL. Julia provides a wide range of
[binaries](https://github.com/JuliaBinaryWrappers/Cbc_jll.jl/releases).
Alternatives include [conda](https://github.com/conda-forge/coin-or-cbc-feedstock) and
your favorite package manager, as detailed [below](https://github.com/coin-or/Cbc#binaries).

Cbc is developed by John Forrest, now retired from IBM Research, and others.
The project is currently managed by John Forrest, [Ted
Ralphs](http://coral.ie.lehigh.edu/~ted/), [Stefan
Vigerske](https://github.com/svigerske), [Haroldo Gambini
Santos](https://github.com/h-g-s), and the rest of the Cbc team. 

Cbc is written in C++ and is released as open source under the [Eclipse Public License 2.0](http://www.opensource.org/licenses/EPL-2.0).

It is distributed under the auspices of the [COIN-OR Foundation](https://www.coin-or.org).

The Cbc development site is https://github.com/coin-or/Cbc.

## CITE

Code: [![DOI](https://zenodo.org/badge/173509563.svg)](https://zenodo.org/badge/latestdoi/173509563)

## CURRENT BUILD STATUS

[![Windows Builds](https://github.com/coin-or/Cbc/actions/workflows/windows-ci.yml/badge.svg?branch=releases/2.10.12)](https://github.com/coin-or/Cbc/actions/workflows/windows-ci.yml?query=branch%3Areleases/2.10.12)

[![Linux and MacOS Builds](https://github.com/coin-or/Cbc/actions/workflows/linux-ci.yml/badge.svg?branch=releases/2.10.12)](https://github.com/coin-or/Cbc/actions/workflows/linux-ci.yml?query=branch%3Areleases/2.10.12)

## DOWNLOAD

What follows is a quick start guide for obtaining or building
Cbc on common platforms. More detailed information is
available [here](https://coin-or.github.io/user_introduction.html).

### Docker image

There is a Docker image that provides Cbc, as well as other projects
in the [COIN-OR Optimization
Suite](https://github.com/coin-or/COIN-OR-OptimizationSuite) [here](https://hub.docker.com/repository/docker/coinor/coin-or-optimization-suite)

### Binaries

For newer releases, binaries will be made available as assets attached to
releases in Github
[here](https://github.com/coin-or/Cbc/releases). Older binaries
are archived as part of Cbc
[here](https://www.coin-or.org/download/binary/Cbc).

 * *Linux* (see https://repology.org/project/coin-or-cbc/versions for a complete listing): 
   * arch:
     ```
     $ sudo pacman -S  coin-or-cbc
     ```
   * Debian/Ubuntu:
     ```
     $ sudo apt-get install  coinor-cbc coinor-libcbc-dev
     ```
   * Fedora/Redhat/CentOS:
     ```
     $ sudo yum install  coin-or-Cbc coin-or-Cbc-devel
     ```
   * freebsd:
     ```
     $ sudo pkg install math/cbc
     ```
   * linuxbrew:
     ```
     $ brew install cbc
     ```
 * *Windows*: The easiest way to get Cbc on Windows is to download an archive as described above.
 * *Mac OS X*: The easiest way to get Cbc on Mac OS X is through [Homebrew](https://brew.sh).
     ```
     $ brew tap coin-or-tools/coinor
     $ brew install coin-or-tools/coinor/cbc
     ```

* *conda* (cross-platform, no Windows for now):
     ```
     $ conda install coin-or-cbc
     ```

Due to license incompatibilities, pre-compiled binaries lack some 
functionality. If binaries are not available for your platform for the latest 
version and you would like to request them to be built and posted, feel free 
to let us know on the mailing list. 

### Source

Source code can be obtained either by

 * Downloading a snapshot of the source code for the latest release version of Cbc from the
 [releases](https://github.com/coin-or/Cbc/releases) page,
 * Cloning this repository from [Github](https://github.com/coin-or/Cbc), or 
 * Using the [coinbrew](https://github.com/coin-or/coinbrew) script to get the project and all dependencies (recommended, see below).   

### Dependencies

Cbc has a number of dependencies, which are detailed in
[config.yml](.coin-or/config.yml). Dependencies on other COIN-OR projects are
automatically downloaded when obtaining the source with `coinbrew`. For some
of the remaining third-party dependencies, automatic download scripts and
build wrappers are provided (and will also be automatically run for required
and recommended dependencies), while other libraries that are aeasy to obtain
must be installed using an appropriate package manager (or may come with your
OS by default). 

## BUILDING from source

These quick start instructions assume you are in a bash shell. 

### Using `coinbrew`

To download and build Cbc from source, execute the 
following on the command line. 
```
wget https://raw.githubusercontent.com/coin-or/coinbrew/master/coinbrew
chmod u+x coinbrew
./coinbrew fetch Cbc@2.10.12
./coinbrew build Cbc
```
For more detailed instructions on coinbrew, see https://coin-or.github.io/coinbrew.
The `coinbrew` script will fetch the additional projects specified in the Dependencies section of [config.yml](.coin-or/config.yml).

### Without `coinbrew` (Expert users)

 * Download the source code, e.g., by cloning the git repo https://github.com/coin-or/Cbc
 * Download and install the source code for the dependencies listed in [config.yml](.coin-or/config.yml)
 * Build the code as follows (make sure to set PKG_CONFIG_PTH to install directory for dependencies).

```
./configure -C
make
make test
make install
```

### With Microsoft Visual Studio

For Microsoft Visual C++ users, there are project files for version 10
available in the `MSVisualStudio` directory. First, obtain the source code
using either a Windows git client or download a snapshot. In MSVC++ Version
10, open the solution file (this should be converted to whatever version of
MSVC+ you are using) and build the Cbc project. The code should build out of
the box with default settings.

It is also possible to build Cbc with the Visual Studio compiler from the
command line using the procedure for Unix-like environments, using the Msys2
shell or CYGWIN. This is the recommended and best-supported way of building
Cbc in Windows from source. To do so, make sure the `cl` compiler is in your
path and add `--enable-msvc to build command of `coinbrew`.  

If you want to build a *parallel version* of CBC using Visual Studio you can
following instructions: (thanks to Tobias Stengel and Alexis Guigue).

Assumptions:

- A VS solution with all necessary projects (libCbc, libClp, libCbcSolver,
  libCgl, libCoinUtils, libOsi, libOsiCbc, libOsiClp). The project files can
  be found inside the `MSVisualStudio` folders. 

Steps (based on VS 2013):

1. for each of the lib* projects do:
   add `CBC_THREAD` under Properties -> Configuration Properties -> C/C++ ->
   Preprocessor -> Preprocessor Definitions (a subset of the lib* projects may
   be sufficient, but it doesn't hurt to do it for all) 

2. Link against a pthreads library.
   [PThreadsWin32](https://www.sourceware.org/pthreads-win32/) works (even in
   64 bits systems) and is distributed under the LGPL. If you decide to use
   the precompiled binaries: both pthreadVC2 and pthreadVS2 seem to work.
   Otherwise: third party VS project files for pthreads4win can be found on
   github.

   Note: If you use C++/Cli, make sure that no callback (eventHandlers, custom
   cut generators, custom heuristics, ...) contains managed code. Otherwise
   your code will crash at runtime with AssembyNotFoundExceptions inside the
   native threads created by Cbc. Even if not, problems with the GC are
   likely.

3. If you link statically against pthreads4win, you have to define
   PTW32_STATIC_LIB when building your program/Cbc (e.g. via Properties ->
   C/C++/Preprocessor -> Preprocessor Definitions) AND - only if you build
   pthreads yourself - when building pthreads. Linking pthreads dynamically
   works without additional preprocessor definitions.

4. pass `-threads yourNumber` to `CbcMain1`

## Doxygen Documentation

If you have `Doxygen` available, you can build a HTML documentation by typing

`make doxydoc` 

in the build directory. If Cbc was built via `coinbrew`, then the build
directory will be `./build/Cbc/2.10.12` by default. The doxygen documentation main file
is found at `<build-dir>/doxydoc/html/index.html`.

If you don't have `doxygen` installed locally, you can use also find the
documentation [here](http://coin-or.github.io/Cbc/Doxygen).

## DOCUMENTATION

 * [User's Guide](https://coin-or.github.io/Cbc) (from 2005)
 * Source code [examples](examples)
 * [Cbc command-line guide](https://github.com/coin-or/COIN-OR-OptimizationSuite/raw/master/Installer/files/doc/cbcCommandLine.pdf)


## Project Links

 * [Code of Conduct](https://www.coin-or.org/code-of-conduct/)
 * [COIN-OR Web Site](http://www.coin-or.org/)
 * [COIN-OR general discussion forum](https://github.com/orgs/coin-or/discussions)
 * [Cbc Discussion forum](https://github.com/coin-or/Cbc/discussions)
 * [Report a bug](https://github.com/coin-or/Cbc/issues/new)
 * [Doxygen generated documentation](http://coin-or.github.io/Cbc/Doxygen)

## CHANGELOG

 * Release 3.0 (in preparation)
   * Added possibility for incomplete MIP start files.
     The filename suffix indicates which values Cbc should choose for
     missing variables (see change r2549)
   * Larger renovation of the build system and a changed directory structure.
     As a consequence, a monolithic build of Cbc, which builds Cbc with
     all its dependencies in one run of configure and make is no longer
     possible. Dependencies should now be build and installed before
     building Cbc.
     - Removed svn:externals. Dependencies (CoinUtils, Osi, Clp, Cgl, etc)
       now need to be build and installed in advance, either manually or
       by using coinbrew.
     - When using a GCC-compatible compiler, the Cbc interface
       functions are now declared with `visibility(default)`-attribute,
       thus building Cbc with `-fvisibility=hidden` still produces a
       usable library.
     - When using a MSVC-compatible compiler, Cbc interface functions
       are now declared with `dllimport`-attribute, so that a Cbc C++ DLL
       can be used.
     - Under Windows/Msys2, DLLs are now build by default.
     - Cygwin and MSys1 are no longer supported.
     - pkg-config is now mandatory. On Windows, make sure to use a
       pkg-config version that produces Unix-style paths.
     - `*_addlibs` files have been removed, pkg-config should be used instead.
     - Script `compile` is now used to wrap around calls of cl/icl/ifort
       and translate GCC-style compiler flags to MSVC style.
     - Header files are now installed in the better named
       `$prefix/include/coin-or` instead of `$prefix/include/coin`.
     - The default for `--prefix` is no longer the build directory, but
       the autotools-default, probably `/usr/local`.
     - `--enable-debug` does not imply `--disable-shared` anymore.
     - Removed `--enable-debug-cbc`, use `--enable-debug` instead.
     - Removed configure variables OPT/DBG_C/CXXFLAGS. Use C/CXXFLAGS instead.
     - Silent build output is now enabled by default, use configure
       flag `--disable-silent-rules` or call make with `V=1` to disable.
     - Also for static builds, PIC objects are now generated by default,
       use `--without-pic` to disable.
     - The `--with-*-incdir` and `--with-*-lib` configure flags have been
       replaced by corresponding `--with-*-cflags` and `--with-*-lflags`
       flags. Note that the include directories need to be specified
       via `-I<dir>` in `--with-*-cflags`.
    * `--enable-cbc-parallel` is now enabled by default if a pthread library
      is found. Use `--disable-cbc-parallel` to disable.
    * Added a conflict graph infrastructure and conflict-based routines:
      - `CglCliqueStrengthening`: preprocessing routine applied on set packing constraints.
      - `CglBKClique`: clique cut separator based on an improved version of Bron-Kerbosch algorithm.
      - `CglOddWheel`: odd-cycle separator with a lifting routine.
      - New parameters in the command line:
          - `cgraph`: sets the use of conflict graph-based routines (CglBKClique, CglOddWheel and CliqueStrengthening) - "off"=turns these routines off, "on"=turns these routines on, "clq"=turns these routines off and enables the cut separator of CglClique - default="on"
          - `clqstr`: sets the use of the preprocessing routine based on clique strengthening (CglCliqueStrengthening) - "off"=turn off this routine, "before"=perform clique strengthening before initial solve, "after"=perform clique strengthening after initial solve - default="after".
          - `clique`: sets the use of CglBKClique (on, root, ifmove, forceOn, onglobal) - default="ifmove".
          - `bkpivot`: pivoting strategy used by Bron-Kerbosch algorithm in CglBKClique - 0=off, 1=random, 2=degree, 3=weight, 4=modified degree, 5=modified weight, 6=modified degree + modified weight - default=3.
          - `bkmaxcalls`: maximum number of recursive calls that can be made by Bron-Kerbosch algorithm in CglBKClique - default=1000.
          - `bkclqext`: strategy used to extend violated cliques found by CglBKClique - 0=off, 1=random, 2=degree, 3=modified degree, 4=reduced cost(inversely proportional), 5=reduced cost(inversely proportional) + modified degree - default = 4.
          - `oddwheel`: sets the use of CglOddWheel (on, root, ifmove, forceOn, onglobal) - default = ifmove.
          - `oddwext`: strategy used to search for wheel centers for the cuts found by CglOddWheel - 0=off, 1=one variable, 2=clique - default=2.
      - CglClique was replaced by CglBKClique as the default clique separator in CbcSolver.cpp.

 * Release 2.10.10
   * Fix for accidental introduction of private symbol into public header.

 * Release 2.10.9
   * Improvements to symmetry handling.
   * Maintenance release to push out accumulates patches.

 * Release 2.10.8
   * Re-generate binaries due to mistake in Github Actions configuration and 
     incorporate new release of Cgl. 

 * Release 2.10.7
   * Fix a bug that would cause the unit test not to run correctly if the 
     MIPLIB3 project was not present

 * Release 2.10.6
   * Accumulated fixes related to build, test, and CI. 

 * Release 2.10.5
   * Revert fix that stopped Clp when timelimit reached, as that lead to
     all cleanup solves afterwards to stop without proper finishing and
     giving wrong results

 * Release 2.10.4
   * Allow .lp files to be read from stdin.
   * Fix parsing of optional arguments to AMPL interface.
   * More bugfixes.

 * Release 2.10.3
   * Improve performance of some primal heuristics, incl. feasibility pump, 
     by making integer slacks continuous
   * Added additional timelimit checks
   * Fixed initialization of Cbc_clone result
   * Additional bugfixes

 * Release 2.10.2
   * Bugfixes

 * Release 2.10.1
   * Fixed Cbc_clone in C interface
   * Fixed CbcMain1() call in examples/driver3.cpp
   * Fixed possible issue with MIPstart if presolve added variables
   * More minor bugfixes

 * Release 2.10.0
   * Improved handling of SOS, starting point, and symmetries
   * Improved performance of primal heuristics regarding the handling of
     implicit integer variables
   * Mini-B&B is now disabled when solving with multiple threads
   * Changed default value for zero half cuts parameter from off to ifmove
   * Added CbcModel::postProcessedSolver() to obtained LP after presolve
   * New option `PrepNames` to indicate whether column names should be
     kept in the pre-processed model
   * New option `sosPrioritize` to determine how to prioritize SOS
   * Added new event `generatedCuts`
   * CbcSolver can now read compressed .lp files (GZIP, BZIP2)
   * New functions in the C interface: Cbc_readLp, Cbc_writeLp,
     Cbc_addCol, Cbc_addRow, Cbc_getNumIntegers, Cbc_bestSolution,
     Cbc_getObjValue, Cbc_getRowNz, Cbc_getRowIndices, Cbc_getRowCoeffs,
     Cbc_getRowRHS, Cbc_getRowSense, Cbc_getColNz, Cbc_getColIndices,
     Cbc_getColCoeffs, Cbc_getReducedCost, Cbc_numberSavedSolutions,
     Cbc_savedSolution, Cbc_savedSolutionObj, Cbc_setMIPStart,
     Cbc_setMIPStartI, Cbc_addCutCallback, Osi_getNumCols, Osi_getColName,
     Osi_getColLower, Osi_getColUpper, Osi_isInteger, Osi_getNumRows,
     Osi_getRowNz, Osi_getRowIndices, Osi_getRowCoeffs, Osi_getRowRHS,
     Osi_getRowSense, Osi_getColSolution, OsiCuts_addRowCut,
     Cbc_getAllowableGap, Cbc_setAllowableGap, Cbc_getAllowableFractionGap,
     Cbc_setAllowableFractionGap, Cbc_getAllowablePercentageGap,
     Cbc_setAllowablePercentageGap, Cbc_getCutoff, Cbc_setCutoff,
     Cbc_getMaximumNodes, Cbc_setMaximumNodes, Cbc_getMaximumSolutions,
     Cbc_setMaximumSolutions, Cbc_getLogLevel, Cbc_setLogLevel,
     Cbc_getMaximumSeconds, Cbc_setMaximumSeconds
   * New action `guess` checks properties of the model to decide the best
     parameters for solving the LP relaxation.
   * New example inc.cpp to illustrate solution callback
   * New example driver5.cpp to illustrate user-defined branching rule
   * New example clpdriver.cpp to illustrate use of ClpEventHandler
   * Added support for using OsiHiGHS with CbcGeneric
   * Added MSVC 14 project files
   * Bugfixes

 * Release 2.9.10
   * Fix a numerical issue
   * Fix some memory leaks
   * Fix issue when root node is obviously infeasible
   * Performance improvements for mini-B&B
   * Fix name of bound in final message
   * Fix names in preprocessed problem

 * Release 2.9.9

   * Fixes for SOS2
   * Updates to mipstart
   * Switching to new build system
   * Updates for CI

 * Release 2.9.8

   * Update to most current releases of dependencies
   * Small bug fixes
   * Add support for automatic build and test with Travis and Appveyor

 * Release 2.9.7

   * Small bug fixes
   * Option to switch to line buffered output

 * Release 2.9.6

   * Small bug fixes

 * Release 2.9.5

   * Small bug fixes

 * Release 2.9.4

   * Small fixes for stability
   * Fixes for Doygen documentation generation

 * Release 2.9.3

   * Minor bug fixes

 * Release 2.9.2

   * Fix for proper installation with `DESTDIR`

 * Release 2.9.1

   * Fix for dependency linking
   * Minor bug fixes

 * Release 2.9.0

   * Introduced specialized branching methods for dealing with "big Ms".
   * Introduced new methods for dealing with symmetry (requires installation of [nauty](http://pallini.di.uniroma1.it/))
   * Introduction of conflict cuts (off by default, turn on with `-constraint conflict`)

 * Release 2.8.13

   * Improved message handling
   * Miscellaneous bug fixes.

 * Release 2.8.12

   * Update for dependencies.

 * Release 2.8.11

   * Major overhaul of C interface
   * Fixes to SOS
   * Miscellaneous bug fixes

 * Release 2.8.10

   * More changes related to thread safety.
   * Fix bug in build system with Visual Studio compiler.
   * Miscellaneous bug fixes.

 * Release 2.8.9

   * Attempt to make Cbc thread safe.
   * Add parallel examples.
   * Add CbcSolverUsefulInfo.
   * Bug fixes.

 * Release 2.8.8

   * Added example to show how to use Cbc with installed libraries in MSVC++
   * Fixed inconsistency in addition of libCbcSolver to dependencies in
     {{{cbc_addlibs.txt}}}.

 * Release 2.8.7

   * Changed so that Doxygen builds LaTex
   * Fixes for build system

 * Release 2.8.6

   * Added option to explicitly link dependencies to comply with packaging
     requirements on Fedora and Debian, as well as allow building of MinGW
     DLLs.

 * Release 2.8.5

   * Minor fixes to build system

 * Release 2.8.4

   * Small bug fixes
   * Upgrades to build system

 * Release 2.8.3:

   * Fix for handling SOS.

 * Release 2.8.2:

   * Fixed recognition of Glpk source in main configure.
   * Minor bug fixes in CoinUtils, Clp, and Cbc.

 * Release 2.8.1:

   * Minor bug fixes

 * Release 2.8.0:

   * Introduced new secondaryStatus 8 to indicate that solving stopped due to
     an iteration limit.
   * Solution pool is now accessible via the command line and the CbcMain*
     interface.
   * New mipstart option to read an initial feasible solution from a file.
     Only values for discrete variables need to be provided.

   * Added Proximity Search heuristic by Fischetti and Monaci (off by
     default): The simplest way to switch it on using stand-alone version is
     `-proximity on`.

     Proximity Search is the new "No-Neighborhood Search" 0-1 MIP refinement
     heuristic recently proposed by Fischetti and Monaci (2012). The idea is
     to define a sub-MIP without additional constraints but with a modified
     objective function intended to attract the search in the proximity of the
     incumbent. The approach works well for 0-1 MIPs whose solution landscape
     is not too irregular (meaning the there is reasonable probability of
     finding an improved solution by flipping a small number of binary
     variables), in particular when it is applied to the first heuristic
     solutions found at the root node.

   * An implementation of Zero-Half-Cuts by Alberto Caprara is now available.
     By default, these cuts are off. To use add to your command line
     -zerohalfCuts root (or other options) or just -zero. So far, they may
     help only on a small subset of problems and may need some tuning.

     The implementation of these cuts is described in G. Andreello, A.
     Caprara, and M. Fischetti "Embedding Cuts in a Branch and Cut Framework:
     a Computational Study with {0,1/2}-Cuts" INFORMS Journal on Computing
     19(2), 229-238, 2007 http://dx.doi.org/10.1287/ijoc.1050.0162

   * An alternative implementation of a reduce and split cut generator by
     Giacomo Nannicini is now available. By default, these cuts are off. To
     use add to your command line -reduce2AndSplitCuts root (or other
     options).

     The implementation of these cuts is described in G. Cornuejols and G.
     Nannicini "Practical strategies for generating rank-1 split cuts in
     mixed-integer linear programming" Mathematical Programming Computation
     3(4), 281-318, 2011 http://dx.doi.org/10.1007/s12532-011-0028-6

   * An alternative robust implementation of a Gomory cut generator by Giacomo
     Nannicini is now available. By default, these cuts are off. To use add to
     your command line -GMI root (or other options).

     The implementation of these cuts is described in G. Cornuejols, F.
     Margot, and G. Nannicini "On the safety of Gomory cut generators"
     http://faculty.sutd.edu.sg/~nannicini/index.php?page=publications

   * To encourage the use of some of the more exotic/expensive cut generators
     a parameter -slowcutpasses has been added. The idea is that the code does
     these cuts just a few times - less than the more usual cuts. The default
     is 10. The cut generators identified by "may be slow" at present are just
     Lift and project and ReduceAndSplit (both versions).

   * Allow initialization of random seed by user. Pseudo-random numbers are
     used in Cbc and Clp. In Clp they are used to break ties in degenerate
     problems, while in Cbc heuristics such as the Feasibility Pump use them
     to decide whether to round up or down. So if a different pseudo-random
     seed is given to Clp then you may get a different continuous optimum and
     so different cuts and heuristic solutions. This can be switched on by
     setting randomSeed for Clp and/or randomCbcSeed for Cbc. The special
     value of 0 tells code to use time of day for initial seed.

   * Building on this idea, Andrea Lodi, Matteo Fischetti, Michele Monaci,
     Domenico Salvagnin, Yuji Shinano, and Andrea Tramontani suggest that this
     idea be improved by running at the root node with multiple copies of
     solver, each with its own different seed and then passing in the
     solutions and cuts so that the main solver has a richer set of solutions
     and possibly stronger cuts. This is switched on by setting
     -multipleRootPasses. These can also be done in parallel.

   * Few changes to presolve for special variables and badly scaled problems
     (in CoinUtils).

   * New option -extraVariables <number> which switches on a trivial
    re-formulation that introduces extra integer variables to group together
    variables with same cost.

   * For some problems, cut generators and general branching work better if
     the problem would be infeasible if the cost is too high. If the new
     option -constraintFromCutoff is set, the objective function is added as a
     constraint which rhs is set to the current cutoff value (objective value
     of best known solution).

 * Release 2.7.8:

   * Change message when LP simplex iteration limit is hit from "Exiting on
     maximum nodes" to "Exiting on maximum number of iterations"
   * Fix for using overlapping SOS.
   * Fixes in buildsystem.

 * Release 2.7.7:

   * Fix to report interruption on user event if SIGINT is received by
     CbcSolver. model->status() should now be 5 if this event happened. Added
     method CbcModel::sayEventHappened() to make cbc stop due to an 'user
     event'.

   * Other minor fixes.

 * Release 2.7.6:

   * Fixes to build system.

   * Other minor fixes.

 * Release 2.7.5:

   * Fixes to get AMPL interface working again.

   * More fixes to MSVC++ files.

 * Release 2.7.4:

   * Minor bugfixes.

 * Release 2.7.3:

   * Minor bugfixes.

   * Fixes to MSVC++ files.

 * Release 2.7.2:

   * Allow row/column names for GMPL models.

   * Added CbcModel::haveMultiThreadSupport() to indicate whether Cbc library
     has been compiled with multithread support.

   * Added CbcModel::waitingForMiniBranchAndBound() to indicate whether
     sub-MIP heuristic is currently running.

   * Cbc shell should work with readline if configured with
     `--enable-gnu-packages`.

   * Support for compressed input files (.gz, .bz2) is now enabled by default.

   * Fix problems with relative gap tolerance > 100% and further bugs.

   * Fixes for MSVC++ Version 9 files.

   * Minor fixes in buildsystem; update to BuildTools 0.7.1.

 * Release 2.7.1:

   * Fixes to MSVC++ files

 * Release 2.7.0:

   * License has been changed to the EPL.

   * Support for MSVC++ version 10 added.

   * Support for BuildTools version 0.7 to incorporate recent enhancements,
     including proper library versioning in Linux, prohibiting installation of
     private headers, etc.

   * Updated externals to new stable versions of dependent projects.

   * Improvements to heuristics.

   * New options for cut generation.

   * Improved reporting of results.

