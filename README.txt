WHAT IS THIS?

This is the collection of all my sharable code that exists within the OpenFOAM ecosystem.  OpenFOAM is a C++
toolset for HPC with a focus on computational fluid dynamics (CFD).  It was created before STL and before
many C++ conventions.  As such, coding in OpenFOAM is quite different from conventional C++.


All this code is from my PhD work on simulating the complex flow and reactions in anaerobic digesters.

* craftsFoam - this is the "Coupled Reaction Advection Flow Transient Solver", and contains the applications
	that use all the other libraries below.
	(Not publicly released)

* equationReader - is an equation parser.  It converts text equations into sequences of operations.  This
	library adds a layer of equation expression into OpenFOAM's dictionaries, giving me the flexibility I
	needed to express the biological reaction equations as inputs
	(Available at https://github.com/Marupio/equationReader)

* multiSolver - this allows a developer to create a CFD solver that switches between two solver algorithms,
	which I needed when the control system changed the boundary conditions and the flow switched from static
	to transient.
	(Available at https://github.com/Marupio/multiSolver)

* plcEmulator - this library adds a general control system layer onto the CFD simulations, allowing the flow
	to trigger changes in the operating conditions, such as temperature control, mixing or flow on or off,
	and so on.  I needed this to simulate normal maintenance operations of the digester.
	(Not publicly released)

* reactionReader - this library fully encapsulates all the data necessary for a CFD simulation of an
	anaerobic digester.
	(Not publicly released)


See the associated publications for more details:

* Gaden 2012 Phd Thesis - Modelling Anaerobic Digesters in Three Dimensions.pdf
	My Phd Thesis explaining all these code bases in detail

* Gaden 2014 WWT Paper - A general three-dimensional extension to ADM1.pdf
	A paper written to the waste water treament academic community about the importance of 3D simulations on
	anaerobic digesters.

* Gaden 2012 CSME Paper - A programmable logic controller emulator.pdf
	A paper written to the OpenFOAM community about the PLC emulator code when I publicly released it.
