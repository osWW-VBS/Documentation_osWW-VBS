#### Table of Content

- [WWAnalysisRun2 Framework](#wwanalysisrun2-framework)
	- [Analysis Full Chain](#analysis-steps)
    - [Machine Learning Studies](#machine-learning-studies)
- [Several other repository in osWW-VBS organisation](#several-other-repository-in-osww-vbs-organisation)
	
---

# WWAnalysisRun2 Framework

All code for our analysis is placed [https://github.com/osWW-VBS](https://github.com/osWW-VBS)

## Analysis steps

- **STEP: 1:** Need Bacon output root files [To be updated...]
- **STEP: 2:** Run WWAnalysisRun2: [WWAnalysisRun2 Framework](https://github.com/osWW-VBS/WWAnalysisRun2)
    + This step applies [pre-selection](documentation/pre-selection.md)
    + To process this step quickly our batch job script divides the jobs into many based on number of input root files.
    + After completation of the batch job we need to merge the root files belonging to same categories.
        * For this we have a script named [makeTxtFileForPlotting.py](https://github.com/osWW-VBS/WWAnalysisRun2/blob/bacon_80x_MuonPtScale/Scripts/makeTxtFileForPlotting.py)
        * This script hadds similar root files and also creates a text file having info of sample name, its cross-section, number of events, number of negative events, etc.
        * Our plotting macro uses this text file for making data-mc distrib
        * Also, Hadd root files for background estimation using script : [hadd.py](https://github.com/osWW-VBS/WWAnalysisRun2/blob/bacon_80x_MuonPtScale/hadd.py)
- **STEP: 3:** Control plots [https://github.com/osWW-VBS/PlottingCodes/tree/master/ControlPlots](https://github.com/osWW-VBS/PlottingCodes/tree/master/ControlPlots)
- **STEP: 4:** Data driven background estimation using : [EXOVVFitter Framework](https://github.com/osWW-VBS/EXOVVFitter)
    + Get Systematic shape and root file up/down for combine using script [GetAll_Systematic_Shape.C](https://github.com/ram1123/EXOVVFitter/blob/master/GetAll_Systematic_Shape.C)
- **STEP: 5:** Get root file for combine: [https://github.com/osWW-VBS/PlottingCodes/tree/master/LimitCardGenerate](https://github.com/osWW-VBS/PlottingCodes/tree/master/LimitCardGenerate)
- **STEP: 6:** Combine uses: *To be updated...*

## Machine Learning Studies

1. Link of TMVA setup done for 2016 analysis : [https://github.com/osWW-VBS/TMVA_Studies](https://github.com/osWW-VBS/TMVA_Studies)


# Several other repository in osWW-VBS organisation

1. https://github.com/osWW-VBS/GridPack_Generation
2. https://github.com/osWW-VBS/MadGraph_With_Condor
3. https://github.com/osWW-VBS/PlottingCodes
4. https://github.com/osWW-VBS/GEN-SIM-analyzer
5. https://github.com/osWW-VBS/LimitSettingTool
6. https://github.com/osWW-VBS/CMS_FulllSimulation
7. https://github.com/osWW-VBS/LHEAnalyzer

