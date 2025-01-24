# LITM-PauseTokens

Evaluator prompt for multi-needle:  
"""  
                    Score 1: The answer contains none of the referenced ingredients.  
                    Score 4: The answer contains exactly 1 of the 3 referenced ingredients.  
                    Score 7: The answer contains exactly 2 of the 3 referenced ingredients.  
                    Score 10: The answer contains all 3 of the referenced ingredients.  
                    Only respond with a numerical score"""  


### Baseline Results  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 |10 | 10 | 10 | 10 | 9.27 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 | 10 | 10 | 10 | 10 | 9.76 | 9.27 | 8.84 |
| Llama 3.2 1B Instruct | 7.67 | 6.64 | 4.11 | 3.67 | 1.4 | 1.38 | 1.04 | 1 |
| Llama 3.2 3B Instruct | 10 | 9.87 | 10 | 9.13 | 6.31 | 3.75 | 5.73 | 5.15 |
| Llama 3.1 8B Instruct | 10 | 10 | 10 | 10 | 9.6 | 9.4 | 7.89 | 7.4 |

### PauseToken1: Inserted &lt;PAUSE&gt; after all paragraphs ending in []    
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 | 10 | 10 | 10 | 9.44 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 | 10 | 10 | 10 | 10 | 10 | 9.71 | 9.47 |
| Llama 3.2 1B Instruct | 7.75 | 6.31 | 4.13 | 4 | 2 | 1.4 | 1 | 1 |
| Llama 3.2 3B Instruct | 10 | 9.93 | 9.67 | 9.62 | 6.51 | 5.24 | 5.6 | 5.64 |
| Llama 3.1 8B Instruct | 10 | 10 | 9.7 | 10 | 9.6 | 8.82 | 8.4 | 7.15 |
| Llama 3.2 3B Instruct Pause-Tuned | 10 | 9.93 | 9.87 | 9.29 | 7.91 | 6.29 | 5.89 | 4.56 |
| Llama 3.1 8B Instruct Pause-Tuned | 10 | 10 | 10 | 10 | 10 | 9.44 | 9.16 | 7.98 |

### PauseToken2: Inserted &lt;PAUSE Stop and absorb the information you have just read&gt; after all paragraphs ending in []     
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 |10 | 10 | 10 | 10 | 9.44 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 9.54 |
| Llama 3.2 1B Instruct | 7.96 | 6.6 | 5.31 | 3.14 | 1.87 | 1.04 | 1 | 1 |
| Llama 3.2 3B Instruct | 10 | 9.93 | 9.93 | 9.4 | 6.35 | 3.67 | 5.36 | 4.29 |
| Llama 3.1 8B Instruct | 10 | 10 | 10 | 10 | 9.8 | 8.8 | 7.49 | 6.27 |

### PauseToken1 + Single Shot Prompt: Inserted &lt;PAUSE&gt; after all paragraphs ending in []  and added prompt: "When You read &lt;PAUSE&gt; in the context, stop and absorb the information you have previously read."  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 |10 | 10 | 10 | 10 | 9.44 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 | 10 | 10 | 10 | 10 | 10 | 9.71 | 9.62 |
| Llama 3.2 1B Instruct | 7.24 | 7.62 | 5.95 | 3.73 | 1.76 | 1.69 | 1 | 1 |
| Llama 3.2 3B Instruct | 9.8 | 9.93 | 10 | 9.58 | 6.02 | 5.84 | 4.47 | 3.27 |
| Llama 3.1 8B Instruct | 10 | 10 | 9.8 | 9.8 | 9.6 | 9.2 | 8.84 | 7.153 |


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
| Llama 3.2 1B Instruct | - | - | - | - | - | - | - | - |
| Llama 3.2 3B Instruct | 8 +/- 2.17 | 7.4 +/- 1.92 | 6.13 +/- 2.36 | 5.53 +/- 1.85 | 4.8 +/- 1.37 | 4.93 +/- 1.75 | 4.27 +/- 0.8 | 3.13 +/- 2.72 |
| Llama 3.1 8B Instruct | 8.07 +/- 2.69 | 7.47 +/- 1.92 | 6.8 +/- 1.78 | 6.4 +/- 1.68 | 4.4 +/- 2.1 | 4.27 +/- 1.55 | 4.27 +/- 0.8 | 4.2 +/- 0.77 |

### PauseToken1: Inserted &lt;PAUSE&gt; after all paragraphs ending in []    
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 9.4 +/- 1.24 | 9.93 +/- 0.26 | 8.67 +/- 2.17  | 7.67 +/- 1.68 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 9.2 +/- 1.37 | 9.8 +/- 0.77 | 9.6 +/- 1.06 | 9 +/- 1.46 | 8.47 +/- 1.78 | 8 +/- 2.45 | 7.8 +/- 2.4 | 8.4 +/- 1.92 |
| Llama 3.2 1B Instruct | - | - | - | - | - | - | - | - |
| Llama 3.2 3B Instruct | 8.67 +/- 2.17 | 7.4 +/- 1.92 | 6.6 +/- 2.36 | 5.53 +/- 1.85 | 4.8 +/- 1.37 | 4.93 +/- 1.75 | 4.27 +/- 0.8 | 3.13 +/- 2.72 |
| Llama 3.1 8B Instruct | 8 +/- 2.7 | 7.4 +/- 1.55 | 6.67 +/- 2.5 | 7 +/- 1.96 | 5.2 +/- 1.52 | 5 +/- 1.46 | 4.47 +/- 1.55 | 4.2 +/- 1.37 |
| Llama 3.2 3B Instruct Pause-Tuned | - | - | - | - | - | - | - | - |
| Llama 3.1 8B Instruct Pause-Tuned | 8.33 +/- 2.32 | 7.93 +/- 2.66 | 8 +/- 2.45| 7.07 +/- 2.46 | 6 +/- 2.07 | 5.8 +/- 2.34 | 4.73 +/- 2.58 | 4.33 +/- 2.66 |

### PauseToken2: Inserted &lt;PAUSE Stop and absorb the information you have just read&gt; after all paragraphs ending in []     
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 |10 +/- 0 | 10 +/- 0 | 9.87 +/- 0.52 | 8.53 +/- 1.46 | 8.2 +/- 1.37 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 10 +/- 0 | 9 +/- 1.06 | 8.6 +/- 1.92 | 9.4 +/- 1.24 | 8 +/- 2.45 | 7 +/- 3.21 | 7.67 +/- 2.32 | 7 +/- 2.27 |
| Llama 3.2 1B Instruct | - | - | - | - | - | - | - | - |
| Llama 3.2 3B Instruct | 7.13 +/- 2.59 | 5.67 +/- 2.72 | 5.33 +/- 1.29 | 4.27 +/- 1.39 | 5 +/- 2.07 | 4.07 +/- 1.16 | 3.67 +/- 1.11 | 3.33 +/- 2.47 |
| Llama 3.1 8B Instruct | 9 +/- 1.46 | 7.67 +/- 1.54 | 7.47 +/- 1.41 | 7.07 +/- 0.96 | 6.73 +/- 0.7 | 6.86 +/- 0.52 | 6.6 +/- 1.55 | 5.71 +/- 1.68 |

### PauseToken1 + Single Shot Prompt: Inserted &lt;PAUSE&gt; after all paragraphs ending in []  and added prompt: "When You read &lt;PAUSE&gt; in the context, stop and absorb the information you have previously read."  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | 10 +/- 0 | 9.6 +/- 1.55 | 9.6 +/- 1.06 | 8.93 +/- 1.44 | 7.87 +/- 2.10 | NA | NA | NA |
| GPT 4o mini 2024-07-18  | 9.8 +/- 0.77 | 10 +/- 0 | 9.2 +/- 1.78 | 9.4 +/- 1.24 | 8.8 +/- 1.52 | 8.2 +/- 1.9 | 7.0 +/- 2.27 | 7.2 +/- 1.37 |
| Llama 3.2 1B Instruct | - | - | - | - | - | - | - | - |
| Llama 3.2 3B Instruct | 7.2 +/- 2.65 | 7.0 +/- 2.27 | 6.0 +/- 1.46 | 4.4 +/- 1.92 | 4.6 +/- 2.32 | 4 +/- 1.6 | 4.2 +/- 1.37 | 3 +/- 1.46 |
| Llama 3.1 8B Instruct | 8.2 +/- 1.52 | 7.4 +/- 1.95 | 7.6 +/- 1.24 | 7.07 +/- 1.22 | 7.27 +/- 0.8 | 7.2 +/- 0.77 | 7 +/- 0 | 5.27 +/- 2.25 |


### PauseToken1 Multi: % improvement over baseline   
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k | Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | -2.08 | 0.61 | 8.38 | -4.13 | NA | NA | NA | 0.70 |
| GPT 4o mini 2024-07-18  | -4.17 | -2.0 | 3.56 | 2.27 | -4.51 | 11.11 | -8.56 | 10.53 | 1.03 |
| Llama 3.2 1B Instruct | 1.04 | -4.97 | 0.49 | 3.2 | 3.17 | 39.73 | -3.85 | 0 | 5.75 |
| Llama 3.2 3B Instruct | - | - | - | - | - | - | - | - | - |
| Llama 3.1 8B Instruct | -0.87 | -0.94 | -1.91 | 9.38 | 18.18 | 17.10 | 4.68 | 0 | 5.70 |
| Llama 3.2 3B Instruct Fine-Tuned | - | - | - | - | - | - |- | - | - |
| Llama 3.1 8B Instruct Fine-Tuned | 3.22 | 6.16 | 17.65 | 10.47 | 36.36 | 35.83 | 10.77 | 3.10 | 15.45 |

### PauseToken2 Multi: % improvement over baseline 
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k | Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | 4.2 | 0 | 6.63 | 2.5 | NA | NA | NA | 3.33 |
| GPT 4o mini 2024-07-18  | 4.17 | -10 | -7.23 | 6.82 | -9.81 | -2.78 | -10.08 | -7.89 | -4.61 |
| Llama 3.2 1B Instruct | - | - | - | - | - | - | - | - | - |
| Llama 3.2 3B Instruct | -10.88 | -23.4 | -13.05 | -22.78 | 4.17 | -17.44 | -14.05 | 6.39 | -11.38 |
| Llama 3.1 8B Instruct | 11.52 | 2.68 | 9.85 | 10.47 | 52.95 | 60.66 | 54.57 | 35.95 | 29.83 |

### PauseToken1 + Single Shot Prompt Multi: % improvement over baseline (AVG % Change: + 3.80%)  
| Model    | 1k      | 2k | 4k | 8k | 16k | 32k | 64k | 128k |  Avg % Change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT 3.5 Turbo 0125 | - | - | -2.74 | 11.63 | -1.63 | NA | NA | NA | 2.42 |
| GPT 4o mini 2024-07-18  | 2.08 | - | -0.76 | 6.82 | -0.79 | 13.89 | -17.94 | -5.26 | -0.28 |
| Llama 3.2 1B Instruct | - | - | - | - | - | - | - | - | - |
| Llama 3.2 3B Instruct | -10.0 | -5.41 | -2.12 | -20.43 | -4.17 | -18.86 | -1.64 | -4.15 | -8.35 |
| Llama 3.1 8B Instruct | 1.61 | -0.94 | 11.76 | 10.47 | 65.23 | 68.62 | 63.93 | 25.48 | 30.77 |

