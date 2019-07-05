#### Table of Content

- [Electron](#electron)
    - [CMS Official Recommendation](#cms-official-recommendation)
    - [Code implementation](#code-implementation)
        - [Electron ID](#electron-id)
        - [Electron Trigger Scale Factor](#electron-trigger-scale-factor)
        - [Electron ID/ISO Scale Factor](#electron-id/iso-scale-factor)

---

# CMS Official Recommendation

## ID

**94X-tuned selection, barrel cuts ( |eta supercluster| &lt;= 1.479)**

| |  Veto (94X) |  Loose (94X) |  Medium (94X) |  Tight (94X) | 
|---    |---    |---           |---         |---            |---  |
| full5x5_sigmaIetaIeta   |  0.0126 |  0.0112 |  0.0106 |  0.0104 |
| abs(dEtaSeed)   |  0.00463 |  0.00377 |  0.0032 |  0.00255 | 
| abs(dPhiIn)   |  0.148 |  0.0884 |  0.0547 |  0.022 | 
| H/E   |  0.05+1.16/E<sub>SC</sub>+0.0324&rho;/E<sub>SC</sub>  |  0.05+1.16/E<sub>SC</sub>+0.0324&rho;/E<sub>SC</sub>  |  0.046+1.16/E<sub>SC</sub>+0.0324&rho;/E<sub>SC</sub>  |  0.026+1.15/E<sub>SC</sub>+0.0324&rho;/E<sub>SC</sub>  |
| relIsoWithEA   |  0.198+0.506/p<sub>T</sub> |  0.112+0.506/p<sub>T</sub> |  0.0478+0.506/p<sub>T</sub> |  0.0287+0.506/p<sub>T</sub> | 
| abs(1/E-1/p)   |  0.209 |  0.193 |  0.184 |  0.159 |
| expected missing inner hits &lt;=  |  2 |  1 |  1 |  1 | 
| pass conversion veto  |  yes |  yes |  yes |  yes |


**94X-tuned selection, endcap cuts ( |eta supercluster| &gt; 1.479)**

| |  Veto (94X) |  Loose (94X) |  Medium (94X) |  Tight (94X) |
|---    |---    |---           |---         |---            |---  |
| full5x5_sigmaIetaIeta &lt;  |  0.0457 |  0.0425 |  0.0387 |  0.0353 |
| abs(dEtaSeed) &lt;  |  0.00814 |  0.00674 |  0.00632 |  0.00501 |
| abs(dPhiIn) &lt;  |  0.19 |  0.169 |  0.0394 |  0.0236 | 
| H/E &lt;  |  0.05+2.54/E<sub>SC</sub>+0.183*&rho;/E<sub>SC</sub>  |  0.0441+2.54/E<sub>SC</sub>+0.183*&rho;/E<sub>SC</sub>  |  0.0275+2.52/E<sub>SC</sub>+0.183*&rho;/E<sub>SC</sub>  |  0.0188+2.06/E<sub>SC</sub>+0.183*&rho;/E<sub>SC</sub>  | 
| relIsoWithEA &lt;  |  0.203+0.963/p<sub>T</sub> |  0.108+0.963/p<sub>T</sub> |  0.0658+0.963/p<sub>T</sub> |  0.0445+0.963/p<sub>T</sub>  | 
| abs(1/E-1/p) &lt;  |  0.132 |  0.111 |  0.0721 |  0.0197 |
| expected missing inner hits &lt;=  |  3 |  1 |  1 |  1 | 
| pass conversion veto  |  yes |  yes |  yes |  yes |

**Impact parameter cuts:**

|    | barrel  |  endcap  |
|---    |---      |---      |
|  d0, cm  |  0.05  |  0.10  |
|  dz, cm  |  0.10  |  0.20  |


**Reference:** [https://twiki.cern.ch/twiki/bin/view/CMS/CutBasedElectronIdentificationRun2#Working_points_for_94X_and_later](https://twiki.cern.ch/twiki/bin/view/CMS/CutBasedElectronIdentificationRun2#Working_points_for_94X_and_later)

## ID Scale Factor

- ID scale factor root file can be found [here](https://twiki.cern.ch/twiki/pub/CMS/EgammaIDRecipesRun2/2017_ElectronTight.root)
- Reference: [https://twiki.cern.ch/twiki/bin/view/CMS/EgammaRunIIRecommendations#Fall17v2](https://twiki.cern.ch/twiki/bin/view/CMS/EgammaRunIIRecommendations#Fall17v2)

## GSF Scale Factor

- GSF scale factor root file can be found [here](https://twiki.cern.ch/twiki/pub/CMS/Egamma2017DataRecommendations/egammaEffi.txt_EGM2D_runBCDEF_passingRECO.root)
- Reference: [https://twiki.cern.ch/twiki/bin/view/CMS/EgammaRunIIRecommendations#Electron_Scale_Factors](https://twiki.cern.ch/twiki/bin/view/CMS/EgammaRunIIRecommendations#Electron_Scale_Factors)

# Code implementation

## Electron ID

[https://github.com/osWW-VBS/WWAnalysisRun2/blob/bacon_80x_MuonPtScale/src/Utils.cc#L111-L277](https://github.com/osWW-VBS/WWAnalysisRun2/blob/bacon_80x_MuonPtScale/src/Utils.cc#L111-L277)

### Electron Trigger Scale Factor

### Electron ID/ISO Scale Factor