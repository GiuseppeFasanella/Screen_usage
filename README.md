**How to use screen**

* Vai su lxplus o sulle M machines [**devi ricordarti su che nodo ti sei loggato!!**]
```
screen -R -D mio_nome
#mi piace perche' se non c'e' uno screen aperto con quel nome
#te ne crea uno, altrimenti ti apre quello esistente
#Invece screen -S nome, puo' prolificare screen a volonta'
```
* Sulle **M machines**

source $VO_CMS_SW_DIR/cmsset_default.sh

**cmsenv** (deve essere un alias in bash)

source /cvmfs/cms.cern.ch/crab3/crab.sh

* Su **lxplus** semplicemente:

**cmsenv** (deve essere un alias in bash)

Lancia il programma

* Per staccarti: **Ctrl+A e poi D**

* Per riagganciarti alla stessa sessione: **screen -R -D mio_nome**

* Per uccidere tutto: exit

* Puoi anche killare tutto con screen -X -S [session # you want to kill] quit

Per vedere tutte le sessioni di screeen aperte:
screen -ls: mi dice i nomi dei Socket, in modo da poter fare: screen -R -D nome_giusto

****************************************************************
Per la precisione in ~/.bashrc ci deve essere questo alias

alias cmsenv='eval `scramv1 runtime -sh`'
