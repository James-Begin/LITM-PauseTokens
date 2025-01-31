\# LITM-PauseTokens

 


### Baseline Results  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.27 +/- 0.6 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.76 +/- 0.08  | 9.27 +/- 0.20 | 8.84 +/- 0.31 |
| Llama 3.2 1B Instruct | 7.67 +/- 0.93 | 6.64 +/- 1.86 | 4.11 +/- 1.89 | 3.67 +/- 0.81 | 1.4 +/- 0.38 | 1.38 +/- 0.69 | 1.04 +/- 0.08 | 1 +/- 0 |
| Llama 3.2 3B Instruct | 10 +/- 0 | 9.87 +/- 0.23 | 10 +/- 0 | 9.13 +/- 0.58  | 6.31 +/- 1.37 | 3.75 +/- 0.4 | 5.73 +/- 1.75 | 5.15 +/- 0.95 |
| Llama 3.1 8B Instruct | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.6 +/- 0.69 | 9.4 +/- 0 | 7.89 +/- 1.35 | 7.4 +/- 0.18 |

### PauseToken1: Inserted &lt;PAUSE&gt; after all paragraphs ending in []    
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.44 +/- 0.23 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0| 10 +/- 0 | 9.71 +/-0.08 | 9.47 +/- 0 |
| Llama 3.2 1B Instruct | 7.75 +/- 0.47 | 6.31 +/- 0.33 | 4.13 +/- 0.28 | 4 +/- 1.37 | 2 +/- 0.28| 1.4 +/- 0.85 | 1 +/- 0 | 1 +/- 0 |
| Llama 3.2 3B Instruct | 10 +/- 0 | 9.93 +/- 0.12 | 9.67 +/- 0.23 | 9.62 +/- 0.33 | 6.51 +/- 1.81 | 5.24 +/- 0.45 | 5.6 +/- 0.35 | 5.64 +/- 0.48 |
| Llama 3.1 8B Instruct | 10 +/- 0 | 10 +/- 0 | 9.7 +/- 0.35 | 10 +/- 0 | 9.6 +/- 0.35 | 8.82 +/- 0.86 | 8.4 +/- 1.51 | 7.15 +/- 0.68 |
| Llama 3.2 3B Instruct Pause-Tuned | 10 +/- 0 | 9.93 +/- 0.12 | 9.87 +/- 0.23 | 9.29 +/- 0.54 | 7.91 +/- 1.64 | 6.29 +/- 1.74 | 5.89 +/- 1.37 | 4.56 +/- 0.42 |
| Llama 3.1 8B Instruct Pause-Tuned | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.44 +/- 0.53 | 9.16 +/- 0.27 | 7.98 +/- 0.37 |

### PauseToken2: Inserted &lt;PAUSE Stop and absorb the information you have just read&gt; after all paragraphs ending in []     
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.44 +/- 0.12 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.54 +/- 0.12 |
| Llama 3.2 1B Instruct | 7.96 +/- 0.66 | 6.6 +/- 1.94 | 5.31 +/- 2.86 | 3.14 +/- 1.30 | 1.87 +/- 0.83 | 1.04 +/- 0.39 | 1 +/- 0 | 1 +/- 0 |
| Llama 3.2 3B Instruct | 10 +/- 0 | 9.93 +/- 0.12 | 9.93 +/- 0.12 | 9.4 +/- 0.35 | 6.35 +/- 1.31 | 3.67 +/- 0.37 | 5.36 +/- 1.61 | 4.29 +/- 1.49 |
| Llama 3.1 8B Instruct | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.8 +/- 0.35 | 8.8 +/- 0.60 | 7.49 +/- 0.20 | 6.27 +/- 0.91 |

### PauseToken1 + Single Shot Prompt: Inserted &lt;PAUSE&gt; after all paragraphs ending in []  and added prompt: "When You read &lt;PAUSE&gt; in the context, stop and absorb the information you have previously read."  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.44 +/- 0.08 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 10 +/- 0 | 9.71 +/- 0.08 | 9.62 +/- 0.08 |
| Llama 3.2 1B Instruct | 7.24 +/- 0.60 | 7.62 +/- 0.73 | 5.95 +/- 2.31 | 3.73 +/- 0.61 | 1.76 +/- 0.33 | 1.69 +/- 0.31 | 1 +/- 0 | 1 +/- 0 |
| Llama 3.2 3B Instruct | 9.8 +/- 0.35 | 9.93 +/- 0.12 | 10 +/- 0 | 9.58 +/- 0.40 | 6.02 +/- 2.24 | 5.84 +/- 0.77 | 4.47 +/- 1.30 | 3.27 +/- 1.01 |
| Llama 3.1 8B Instruct | 10 +/- 0 | 10 +/- 0 | 9.8 +/- 0.35 | 9.8 +/- 0.35 | 9.6 +/- 0.35 | 9.2 +/- 0.69 | 8.84 +/- 0.53 | 7.153 +/- 0.08 |


### PauseToken1: % improvement over baseline (Non-fine-tuned % Change: +4.21%) (Fine-Tuned % Change: +12.53%)    
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k | Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | - | - | - | 1.83 | NA | NA | NA | 1.83 |
| GPT 4o mini 2024-07-18  | - | - | - | - | - | 2.46 | 4.75 | 7.13 | 4.78 |
| Llama 3.2 1B Instruct | 1.04 | -4.97 | 0.49 | 3.2 | 3.17 | 39.73 | -3.85 | 0 | 5.75 |
| Llama 3.2 3B Instruct | - | 0.61 | -3.3 | 5.37 | 14.75 | 47.37 | -2.27 | 9.51 | 10.29 |
| Llama 3.1 8B Instruct | - | - | -3.0 | - | 0 | -8.13 | 6.46 | -3.38 | -1.61 |
| Llama 3.2 3B Instruct Fine-Tuned | - | 0.61 | -1.3 | 1.75 | 25.36 | 67.73 | 2.79 | -11.46 | 12.21 |
| Llama 3.1 8B Instruct Fine-Tuned | - | - | - | - | 4.17 | -1.67 | 16.09 | 32.78 | 12.84 |
 

### PauseToken2: % improvement over baseline (AVG % change: +0.31%)
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k | Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | - | - | - | 1.83 | NA | NA | NA | 1.83 |
| GPT 4o mini 2024-07-18  | - | - | - | - | - | 2.46 | 7.87 | 7.92 | 6.08 |
| Llama 3.2 1B Instruct | 3.78 | -0.6 | 29.20 | -14.44 | 33.57 | -24.64 | -3.85 | 0 | 2.88 |
| Llama 3.2 3B Instruct | - | 0.61 | 2.96 | 0.63 | -2.13 | -6.46 | 2.89 | -16.7 | -2.6 |
| Llama 3.1 8B Instruct | - | - | - | - | 2.08 | -8.33 | -5.07 | -15.27 | -6.65 |


### PauseToken1 + Single Shot Prompt: % improvement over baseline (AVG % Change: + 3.80%)  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |  Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | - | - | - | 1.83 | NA | NA | NA | 1.83 |
| GPT 4o mini 2024-07-18  | - | - | - | - | - | 2.46 | 4.75 | 8.82 | 5.34 |
| Llama 3.2 1B Instruct | -5.61 | 14.76 | 44.77 | 1.63 | 25.71 | 22.46 | -3.85 | 0 | 12.48 |
| Llama 3.2 3B Instruct | -2.0 | -0.61 | - | 4.93 | -4.6 | 55.73 | -22.0 | -36.51 | -0.72 |
| Llama 3.1 8B Instruct | - | - | -2.0 | -2.0 | 0 | -4.17 | 12.04 | -3.33 | 0.09 |

### All-Context Average Table
| Model    | Baseline | PauseToken1 | PauseToken2 | PauseToken1 + Prompt |
| --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 9.854 | 9.888 | 9.888 | 9.888 | 
| GPT 4o mini 2024-07-18  | 9.734 | 9.898 | 9.943 | 9.916 | 
| Llama 3.2 1B Instruct | 3.364 | 3.449 | 3.49 | 3.749 | 
| Llama 3.2 3B Instruct | 7.493 | 7.57 | 7.366 | 7.364 | 
| Llama 3.1 8B Instruct | 9.286 | 9.131 | 9.045 | 9.299 | 
| Llama 3.2 3B Instruct Fine-Tuned | - | 8.651 | - | - |
| Llama 3.1 8B Instruct Fine-Tuned | - | 9.573 | - | - |

### All-Context Average % Change Table
| Model    | Baseline | PauseToken1 | PauseToken2 | PauseToken1 + Prompt |
| --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | 0.35 | 0.35 | 0.35 | 
| GPT 4o mini 2024-07-18  | - | 1.68 | 2.15 | 1.87 | 
| Llama 3.2 1B Instruct | - | 2.53 | 3.75 | 11.44 | 
| Llama 3.2 3B Instruct | - | 1.03 | -1.70 | -1.72 | 
| Llama 3.1 8B Instruct | - | -1.67 | -2.60 | 0.14 | 
| Average % Change | - | 0.78 | 0.39 | 2.42 |
| Llama 3.2 3B Instruct Fine-Tuned | - | 15.45 | - | - |
| Llama 3.1 8B Instruct Fine-Tuned | - | 3.09 | - | - |


### Baseline Multi-Needle Results  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 9.6 +/- 1.06 | 9.87 +/- 0.52 | 8 +/- 1.73 | 8 +/- 1.36 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 9.6 +/- 1.06 | 10 +/- 0 | 9.27 +/- 1.55 | 8.8 +/- 2.48 | 8.87 +/- 2.26 | 7.2 +/- 2.65 | 8.53 +/- 2.64 | 7.6 +/- 1.68 |
| Llama 3.2 1B Instruct | 6.4 +/- 4.56 | 8.6 +/- 3.18 | 7.0 +/- 4.39 | 1.0 +/- 0 | 3.6 +/- 4.06 | 1.0 +/- 0 | 2.2 +/- 3.17 | 1.0 +/- 0 |
| Llama 3.2 3B Instruct | 7.2 +/- 3.10 | 6.2 +/- 2.40 | 5.2 +/- 2.21 | 3.6 +/- 1.92 | 4.2 +/- 2.11 | 3.4 +/- 1.68 | 3.4 +/- 2.32 | 2.2 +/- 1.52 |
| Llama 3.1 8B Instruct | 8.07 +/- 2.69 | 7.47 +/- 1.92 | 6.8 +/- 1.78 | 6.4 +/- 1.68 | 4.4 +/- 2.1 | 4.27 +/- 1.55 | 4.27 +/- 0.8 | 4.2 +/- 0.77 |
| Llama 3.1 8B Instruct Long-Context Fine Tuned | 5.6 +/- 1.92 | 6.8 +/- 2.88 | 6.8 +/- 3.30 | 5.6 +/- 2.50 | 5.2 +/- 2.21 | 5.0 +/- 2.17 | 4.8 +/- 1.78 | 3.0 +/- 1.46 |

### PauseToken1: Inserted &lt;PAUSE&gt; after all paragraphs ending in []    
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 9.4 +/- 1.24 | 9.93 +/- 0.26 | 8.67 +/- 2.17  | 7.67 +/- 1.68 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 9.2 +/- 1.37 | 9.8 +/- 0.77 | 9.6 +/- 1.06 | 9 +/- 1.46 | 8.47 +/- 1.78 | 8 +/- 2.45 | 7.8 +/- 2.4 | 8.4 +/- 1.92 |
| Llama 3.2 1B Instruct | 8.2 +/- 3.73 | 9.4 +/- 2.32 | 9.4 +/- 2.32 | 6.2 +/- 4.46 | 5.0 +/- 4.49 | 3.4 +/- 4.12 | 2.8 +/- 3.72 | 1.0 +/- 0 |
| Llama 3.2 3B Instruct | 8 +/- 2.17 | 7.4 +/- 1.92 | 6.13 +/- 2.36 | 5.53 +/- 1.85 | 4.8 +/- 1.37 | 4.93 +/- 1.75 | 4.27 +/- 0.8 | 3.13 +/- 2.72 |
| Llama 3.1 8B Instruct | 8 +/- 2.7 | 7.4 +/- 1.55 | 6.67 +/- 2.5 | 7 +/- 1.96 | 5.2 +/- 1.52 | 5 +/- 1.46 | 4.47 +/- 1.55 | 4.2 +/- 1.37 |
| Llama 3.2 3B Instruct Pause-Tuned | 7.0 +/- 3.59 | 5.8 +/- 2.73 | 4.8 +/- 4.0 | 2.8 +/- 2.96 | 1.2 +/- 4.93 | 1.0 +/- 0.0 | 1.0 +/- 0.0 | 1.0 +/- 0.0 |
| Llama 3.1 8B Instruct Pause-Tuned | 8.33 +/- 2.32 | 7.93 +/- 2.66 | 8 +/- 2.45| 7.07 +/- 2.46 | 6 +/- 2.07 | 5.8 +/- 2.34 | 4.73 +/- 2.58 | 4.33 +/- 2.66 |

### PauseToken2: Inserted &lt;PAUSE Stop and absorb the information you have just read&gt; after all paragraphs ending in []     
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 |10 +/- 0 | 10 +/- 0 | 9.87 +/- 0.52 | 8.53 +/- 1.46 | 8.2 +/- 1.37 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 +/- 0 | 9 +/- 1.06 | 8.6 +/- 1.92 | 9.4 +/- 1.24 | 8 +/- 2.45 | 7 +/- 3.21 | 7.67 +/- 2.32 | 7 +/- 2.27 |
| Llama 3.2 1B Instruct | 3.0 +/- 1.85 | 2.2 +/- 1.90 | 2.8 +/- 2.73 | 2.2 +/- 2.21 | 1.4 +/- 1.06 | 1.8 +/- 2.40 | 1.6 +/- 1.68| 1.0 +/- 0 |
| Llama 3.2 3B Instruct | 7.13 +/- 2.59 | 5.67 +/- 2.72 | 5.33 +/- 1.29 | 4.27 +/- 1.39 | 5 +/- 2.07 | 4.07 +/- 1.16 | 3.67 +/- 1.11 | 3.33 +/- 2.47 |
| Llama 3.1 8B Instruct | 9 +/- 1.46 | 7.67 +/- 1.54 | 7.47 +/- 1.41 | 7.07 +/- 0.96 | 6.73 +/- 0.7 | 6.86 +/- 0.52 | 6.6 +/- 1.55 | 5.71 +/- 1.68 |

### PauseToken1 + Single Shot Prompt: Inserted &lt;PAUSE&gt; after all paragraphs ending in []  and added prompt: "When You read &lt;PAUSE&gt; in the context, stop and absorb the information you have previously read."  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 9.6 +/- 1.55 | 9.6 +/- 1.06 | 8.93 +/- 1.44 | 7.87 +/- 2.10 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 9.8 +/- 0.77 | 10 +/- 0 | 9.2 +/- 1.78 | 9.4 +/- 1.24 | 8.8 +/- 1.52 | 8.2 +/- 1.9 | 7.0 +/- 2.27 | 7.2 +/- 1.37 |
| Llama 3.2 1B Instruct | 2.4 +/- 1.55 | 2.2 +/- 1.52 | 2.4 +/- 1.55 | 2.8 +/- 1.90 | 1.4 +/- 1.06 | 1.6 +/- 1.68 | 1.4 +/- 1.06 | 1.0 +/- 0 |
| Llama 3.2 3B Instruct | 7.2 +/- 2.65 | 7.0 +/- 2.27 | 6.0 +/- 1.46 | 4.4 +/- 1.92 | 4.6 +/- 2.32 | 4 +/- 1.6 | 4.2 +/- 1.37 | 3 +/- 1.46 |
| Llama 3.1 8B Instruct | 8.2 +/- 1.52 | 7.4 +/- 1.95 | 7.6 +/- 1.24 | 7.07 +/- 1.22 | 7.27 +/- 0.8 | 7.2 +/- 0.77 | 7 +/- 0 | 5.27 +/- 2.25 |


### PauseToken1 Multi: % improvement over baseline   
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k | Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | -2.08 | 0.61 | 8.38 | -4.13 | NA | NA | NA | 0.70 |
| GPT 4o mini 2024-07-18  | -4.17 | -2.0 | 3.56 | 2.27 | -4.51 | 11.11 | -8.56 | 10.53 | 1.03 |
| Llama 3.2 1B Instruct | 28.13 | 9.30 | 34.29 | 520 | 38.89 | 240 | 27.27 | 0 | 112.24 |
| Llama 3.2 3B Instruct | 11.11 | 19.35 | 17.88 | 53.61 | 14.29 | 45 | 25.59 | 42.27 | 28.64 |
| Llama 3.1 8B Instruct | -0.87 | -0.94 | -1.91 | 9.38 | 18.18 | 17.10 | 4.68 | 0 | 5.70 |
| Llama 3.2 3B Instruct Fine-Tuned | -2.78 | -6.45 | -7.69 | -22.23 | -71.33 | -70.59 | -70.59 | -54.55 | -38.28 |
| Llama 3.1 8B Instruct Fine-Tuned | 3.22 | 6.16 | 17.65 | 10.47 | 36.36 | 35.83 | 10.77 | 3.10 | 15.45 |

### PauseToken2 Multi: % improvement over baseline 
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k | Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | 4.2 | 0 | 6.63 | 2.5 | NA | NA | NA | 3.33 |
| GPT 4o mini 2024-07-18  | 4.17 | -10 | -7.23 | 6.82 | -9.81 | -2.78 | -10.08 | -7.89 | -4.61 |
| Llama 3.2 1B Instruct | -53.13 | -74.42 | -60.0 | 120 | -61.11 | 80.0 | -27.27 | 0 | -75.93 |
| Llama 3.2 3B Instruct | -0.97 | -8.55 | 2.5 | 18.61 | 19.05 | 19.71 | 7.94 | 51.36 | 13.71 |
| Llama 3.1 8B Instruct | 11.52 | 2.68 | 9.85 | 10.47 | 52.95 | 60.66 | 54.57 | 35.95 | 29.83 |

### PauseToken1 + Single Shot Prompt Multi: % improvement over baseline (AVG % Change: + %)  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |  Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | - | -2.74 | 11.63 | -1.63 | NA | NA | NA | 2.42 |
| GPT 4o mini 2024-07-18  | 2.08 | - | -0.76 | 6.82 | -0.79 | 13.89 | -17.94 | -5.26 | -0.28 |
| Llama 3.2 1B Instruct | -62.5 | 74.42 | -65.72 | 180 | -61.11 | 60 | -36.36 | 0 | 12.22 |
| Llama 3.2 3B Instruct | 0 | 12.90 | 15.38 | 22.22 | 9.52 | 17.65 | 23.53 | 36.36 | 17.20 |
| Llama 3.1 8B Instruct | 1.61 | -0.94 | 11.76 | 10.47 | 65.23 | 68.62 | 63.93 | 25.48 | 30.77 |

Evaluator prompt for multi-needle:  
```  
Score 1: The answer contains none of the referenced ingredients.  
Score 4: The answer contains exactly 1 of the 3 referenced ingredients.  
Score 7: The answer contains exactly 2 of the 3 referenced ingredients.  
Score 10: The answer contains all 3 of the referenced ingredients.  
Only respond with a numerical score
```

Evaluator prompt for single needle:  
```  
Score 1: The answer is completely unrelated to the reference.
Score 3: The answer has minor relevance but does not align with the reference.
Score 5: The answer has moderate relevance but contains inaccuracies.
Score 7: The answer aligns with the reference but has minor omissions.
Score 10: The answer is completely accurate and aligns perfectly with the reference.
Only respond with a numberical score
```

Single Needle Question:  
```
What is the best thing to do in San Francisco?
```
Single Needle:  
```
The best thing to do in San Francisco is eat a sandwich and sit in Dolores Park on a sunny day.
```
Multi Needle Question:  
```
What are the secret ingredients needed to build the perfect pizza?
```
Multi Needle:  
```
Figs are one of the secret ingredients needed to build the perfect pizza.
Prosciutto is one of the secret ingredients needed to build the perfect pizza.
Goat cheese is one of the secret ingredients needed to build the perfect pizza.
```

* Note that some models such as those from OpenAI have a strict limit at 16k or 128k tokens for input. To account for the token length of the prompt, the context may be slightly shortened
