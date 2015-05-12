# AKJetsMatchingCFIs
Two cfi.py files to be used for matching AK4 and AK8 jets to Gen level particles (u,d,s,c,t,b,W), to be used with CMSSW package PhysicsTools/HepMCCandAlgos
Comprises of two EDFilter modules for AK4 jets and AK8 jets. 
The modules create one-to-one association maps between the spicified MC and Generator level objects, of the same name as the module

To use the modules do the following:
First, in your version of CMSSW checkout the PhysicsTools/HepMCCandAlgos package:

    git cms-addpkg PhysicsTools/HepMCCandAlgos
    
clone this repository into the PhysicsTools/HepMCCandAlgos/python directory

    git clone http://github.com/EJDomi/AKJetsMatchingCFIs.git PhysicsTools/HepMCCandAlgos/python
    
Compile the package
  
    scram b
    
To access the modules in your Analyzer use:

    from PhysicsTools.HepMCCandAlgos.jetsAK4GenParticlesMatch_cfi import *
    from PhysicsTools.HepMCCandAlgos.jetsAK8GenParticlesMatch_cfi import *
    
If the names "jetsAK4" and "jetsAK8" do not properly match the label for the AK4 and AK8 jet objects used in the root files just edit the names in the cfi.py files so that they properly match
