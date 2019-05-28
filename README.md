# Temporally-language-grounding
A Pytorch implemention for some state-of-the-art models for "Temporally language grounding in untrimmed videos"

## Requirements
- Python 2.7
- Pytorch 0.4.1
- matplotlib
- The code is for [Charades-STA](https://arxiv.org/pdf/1705.02101.pdf) dataset.

## Three Models for this task
### Supervised Learning based methods
- [TALL](http://openaccess.thecvf.com/content_ICCV_2017/papers/Gao_TALL_Temporal_Activity_ICCV_2017_paper.pdf): Temporal Activity Localization via Language Query
- [MAC](https://arxiv.org/pdf/1811.08925.pdf): MAC: Mining Activity Concepts for Language-based Temporal Localization.
### Reinforcement Learning based method
- [A2C]((https://arxiv.org/abs/1901.06829v1)): Read, Watch, and Move: Reinforcement Learning for Temporally Grounding Natural Language Descriptions in Videos.

## Performance
| Methods        | R@1, IoU0.7   |  R@1, IoU0.5  | R@5, IoU0.7   |  R@5, IoU0.5  |
| --------   | -----:   | :----: | :----: | :----: |
| TALL        | 1      |   5    |1      |   5    |
|  MAC        | 1      |   6    |1      |   5    |
|  A2C        | 1      |   7    |  None      |   None    |

## Features Download
- [visual features](https://drive.google.com/open?id=1vFxDw4AkGVgfILH-6xaHofLZ7PbWwFC2)
- [visual activity concepts](https://drive.google.com/open?id=1biKPDmb7hbzowKLMIRSTLE0w_tWbGPAe) (for MAC)
- [ref_info](https://drive.google.com/open?id=16rFGu9rnhnH-WQeUmN7VtMgljrhGspll)
- [RL_pickle]() (for A2C)

### Training and Testing for TALL
python main_charades_SL.py --model TALL

### Training and Testing for MAC
python main_charades_SL.py --model MAC

### Training and Testing for A2C
python main_charades_RL.py


## Acknowledgements
Thanks the original [TALL](https://github.com/jiyanggao/TALL), [MAC](https://github.com/runzhouge/MAC) and awesome PyTorch team.

