B2GAnaFW
========

Analysis framework for Beyond Two Generations (B2G) Physics Analysis Group (PAG) of the Compact Muon Solenoid (CMS) Experiment

Version
=======

This version is used to produced B2G EDMNtuples for the re-MiniAOD of the MC and Run2012D, as weill as the Run2012D_PromptReco-v4

https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookMiniAOD#Run2_Spring15MiniAODv2_re_miniAO

https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookMiniAOD#Run2015_B_C_50ns_D_05Oct2015_re

https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookMiniAOD#Run2015D_PromptReco_v4_Data_2015

Checkout Instructions
=====================

Make a new CMSSW area

$ cmsrel CMSSW_7_4_15

$ cd CMSSW_7_4_15/src

$ cmsenv

Needed to run VID for electron ID
=================================

$ git cms-merge-topic ikrav:egm_id_7.4.12_v1

Clone the github repository
===========================

$ git clone -b v7.4.x_V8 https://github.com/cmsb2g/B2GAnaFW.git Analysis/B2GAnaFW

Compile
=======

$ scram b -j 10

Running
=======

The python configuration file for cmsRun is B2GAnaFW/test/b2gedmntuples_cfg.py. It runs on the miniAOD data tier and produces an EDM-ntuple.

The configuration file contians a header explaining usage. Do

$ cd Analysis/B2GAnaFW/test

$ python b2gedmntuples_cfg.py 

for running instructions. 

