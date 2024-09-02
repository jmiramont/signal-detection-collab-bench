# Benchmark Report

## Configuration

Length of signals: 1024

Repetitions: 2000

SNRin values: 
-5, 
0, 
5, 
10, 


### Methods  

* monte_carlo_test 

* global_mad_test 

* global_rank_env_test 

### Signals  

* LinearChirp 

## Mean results tables: 

The results shown here are the average and 95\% Clopper-Pearson CI of                             the estimated detection power with Bonferroni correction.                             Best performances are **bolded**. 
### Signal: LinearChirp[[View Plot]](https://jmiramont.github.io/signal-detection-collab-bench/results/b1/plot_LinearChirp.html)    [[Get .csv]](https://jmiramont.github.io/signal-detection-collab-bench/results/b1/results_LinearChirp.csv)
|    | Method + Param                                                                                                    | SNRin=-5dB (average)   | SNRin=-5dB (CI)                            | SNRin=0dB (average)   | SNRin=0dB (CI)                            | SNRin=5dB (average)   | SNRin=5dB (CI)                           | SNRin=10dB (average)   | SNRin=10dB (CI)           |
|---:|:------------------------------------------------------------------------------------------------------------------|:-----------------------|:-------------------------------------------|:----------------------|:------------------------------------------|:----------------------|:-----------------------------------------|:-----------------------|:--------------------------|
|  0 | monte_carlo_test{'statistic': 'Frs', 'pnorm': 2, 'rmax': 1.0, 'MC_reps': 199}                                     | 0.10                   | [0.0779198581219754, 0.11427223385055933]  | 0.34                  | [0.31075757789791586, 0.3691050865481202] | 0.90                  | [0.883566178032573, 0.9202529204418928]  | **1.00**               | [0.9971199946972821, 1.0] |
|  1 | monte_carlo_test{'statistic': 'Frs_vs', 'pnorm': 2, 'rmax': 1.0, 'MC_reps': 199}                                  | 0.12                   | [0.10091507103259163, 0.14113806456356023] | 0.65                  | [0.6151331684264468, 0.6740875710141729]  | **1.00**              | [0.9971199946972821, 1.0]                | 1.00                   | [0.9971199946972821, 1.0] |
|  2 | global_mad_test{'statistic': 'Frs', 'MC_reps': 199}                                                               | 0.09                   | [0.07472808873967307, 0.11048362511682755] | 0.31                  | [0.2824970632553394, 0.33952174762562476] | 0.86                  | [0.8354536742366723, 0.8786142548967406] | 1.00                   | [0.9971199946972821, 1.0] |
|  3 | global_mad_test{'statistic': 'Frs_vs', 'MC_reps': 199}                                                            | 0.11                   | [0.08891728232082022, 0.1272078789175078]  | 0.65                  | [0.6247895619182606, 0.6833800629566581]  | 1.00                  | [0.9971199946972821, 1.0]                | 1.00                   | [0.9971199946972821, 1.0] |
|  4 | global_rank_env_test{'fun': 'Fest', 'correction': 'rs'}                                                           | 0.10                   | [0.08340852263096467, 0.1207500424319543]  | 0.57                  | [0.5398272598661568, 0.6007940027714392]  | 1.00                  | [0.9971199946972821, 1.0]                | 1.00                   | [0.9971199946972821, 1.0] |
|  5 | global_rank_env_test{'fun': 'Fest', 'correction': 'rs', 'rmin': 0.65, 'rmax': 1.05}                               | **0.15**               | [0.12465942256908788, 0.16825346254519633] | 0.73                  | [0.7066441137795977, 0.7610944306300808]  | 1.00                  | [0.9971199946972821, 1.0]                | 1.00                   | [0.9971199946972821, 1.0] |
|  6 | global_rank_env_test{'fun': 'Fest', 'correction': 'rs', 'transform': 'asin(sqrt(.))'}                             | 0.11                   | [0.08799782567776983, 0.12613289504004419] | 0.58                  | [0.5493899770368037, 0.6101802361199339]  | 1.00                  | [0.9971199946972821, 1.0]                | 1.00                   | [0.9971199946972821, 1.0] |
|  7 | global_rank_env_test{'fun': 'Fest', 'correction': 'rs', 'rmin': 0.65, 'rmax': 1.05, 'transform': 'asin(sqrt(.))'} | 0.14                   | [0.12372364537420322, 0.16719471958657817] | **0.74**              | [0.7087038598755453, 0.763023887786904]   | 1.00                  | [0.9971199946972821, 1.0]                | 1.00                   | [0.9971199946972821, 1.0] |
