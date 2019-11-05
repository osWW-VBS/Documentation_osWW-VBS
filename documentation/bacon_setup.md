# Bacon setup

```bash
cmsrel CMSSW_10_2_13
cd CMSSW_10_2_13/src
cmsenv
git cms-merge-topic cmantill:baconprod-10213-v15
git clone https://github.com/ksung25/BaconProd
git clone https://github.com/ksung25/BaconAna
scram b -j 10
cd BaconProd/Ntupler/
mkdir crab
```
