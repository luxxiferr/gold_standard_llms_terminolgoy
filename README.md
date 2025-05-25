# Legal Spanish Terminology Extraction: Gold-standard Generation and LLMs Evaluation
This study aims to develop a gold-standard for terminological extraction in Castilian Spanishwithin the domain of labour law. To achieve this, a methodology was developed based onestablished linguistic theories and reviewed bya community of expert terminologists . Departing from previous extraction studies andreference theoretical frameworks, candidate terms were identified by their morphosyntac-tic patterns, enriched by assessing their degree of specialisation in reference resources. The candidate terms were then subjected to manual validation. To evaluate its applicability, we assessed the performance of the LLaMA3-8B and Mistral-7B language models in extracting labour law terms from the latest version of the Real Decreto Legislativo 2/2015 Ley del Estatuto de los Trabajadores, using prompting techniques and our gold-standard as the benchmark.

This repository contains the following folders:
1. Data: contains a folder per article, which includes:
   A. The terms extracted by the terminologies following the morphosyntactic patterns: patron_N_ADJ_ADJ_LL_contexto_articulo_*.csv patron_N_ADJ_LL_contexto_articulo_*.csv,   patron_N_ADJ_PREP_N_ADJ_contexto_articulo_*.csv, patron_N_ADJ_PREP_N_contexto_articulo_*.csv,  patron_N_PREP_N_contexto_articulo_*.csv, etc
   B. The terms extracted by the models:
   
       - Mistral (zero-shot): terminos_extraidos_con_patrones_ con_ejemplos_mistral.txt
       - Mistral (one-shot): terminos_extraidos_con_patrones_sin_ejemplos_mistral.txt
       - LLaMA 3 (zero-shot): terminos_extraidos_con_patrones_sin_ejemplos.txt
       - LLaMA 3 (one-shot): terminos_extraidos_con_patrones_ejemplos.txt
   
   C. The raw text from the article: articulo_*.txt
   D. The list with all the manually validated terms from the article: terminos_validados_todos.txt

3. Code: code used for the experiments
   A. Terminology extraction with LLMs:
   
       - Mistral: mistral_extraction
       - LLaMA3: llama3_extraction
   
   B. Code used for the evaluation: evaluación

4. Evaluation_results:
   
   A. Mistral:
   
       - global zero-shot results: evaluacion_anotaciones_global_mistral_zero
       - zero-shot results per article: evaluacion_por_articulo_mistral_zero
       - global one-shot results: evaluacion_anotaciones_global_mistral_one
       - one-shot results per article: evaluacion_anotaciones_por_articulo_mistral_one
   
   B. LLaMA3:
   
       - global zero-shot results: evaluacion_anotaciones_global_llama_zero
       - zero-shot results per article: evaluacion_por_articulo_llama_zero
       - global one-shot results: evaluacion_anotaciones_global_llama_one
       - one-shot results per article: evaluacion_anotaciones_por_articulo_llama_one
       
   
