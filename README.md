<h1 align="center">Corretor de Redações para o ENEM com LLM, LoRA e RAG</h1>

Desenvolvido para a disciplina **Tópicos em Inteligência Computacional** do Programa de Pós-Graduação em Informática (PPGI-CP/DV).

Este projeto desenvolve um protótipo de corretor de redações para o ENEM, combinando o poder dos Modelos de Linguagem de Grande Escala (LLMs) com técnicas de Low-Rank Adaptation (LoRA) para fine-tuning e Retrieval-Augmented Generation (RAG) para contextualização e feedback detalhado.

<h2>🎓 Sobre o Projeto</h2>

**Problema**

O Exame Nacional do Ensino Médio (ENEM) é crucial para o acesso ao ensino superior no Brasil, onde a redação desempenha um papel fundamental. No entanto, o acesso a feedback personalizado e detalhado sobre as redações pode ser limitado.

**Objetivo**

Criar um corretor de redações para o ENEM que utiliza um LLM finetunado em português e adaptado com LoRA, integrado a um sistema RAG. O sistema recebe uma redação e o tema proposto, e emprega um banco de dados vetorial de redações anteriores para gerar feedback contextualizado e aderente aos critérios de avaliação do ENEM.

**Tecnologias e Abordagens**

* **LLM Base**: Qwen2.5-0.5B-PT-BR-Instruct (um modelo com bom desempenho em português).
* **Fine-tuning**: Low-Rank Adaptation (LoRA) para adaptação eficiente do modelo ao domínio de redações do ENEM.
* **RAG**: Retrieval-Augmented Generation, utilizando ChromaDB (banco de dados vetorial) e Sentence Transformers (para embeddings de texto).
* **Dataset**: Redações do ENEM provenientes do repositório ```uol-redacoes-xml``` (https://github.com/gpassero/uol-redacoes-xml).
* **Tokenização**: Utilizando o tokenizer do modelo Qwen2.5.
* **Avaliação**: Métricas como ROUGE, BERTScore e BLEU são empregadas para avaliar a qualidade do feedback gerado.

<h2>⚠️ Escopo e Limitações</h2>

Este projeto é um protótipo e, como tal, apresenta algumas limitações:
* O feedback gerado pode necessitar de refinamentos para cobrir todas as nuances de cada competência avaliada pelo ENEM.
* O dataset utilizado é limitado em termos de quantidade e temporalidade (principalmente dados até 2017, conforme o repositório original).

No entanto, a experiência de desenvolver este projeto foi uma jornada de aprendizado intensa e recompensadora!

<h2>📚 Referências</h2>

* **Dataset de Redações**: UOL Redações XML (https://github.com/gpassero/uol-redacoes-xml)
* **Modelo pré-treinado**: https://huggingface.co/amadeusai/Amadeus-Verbo-FI-Qwen2.5-0.5B-PT-BR-Instruct
* **Modelo de embeddings**: https://huggingface.co/sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2
* **Bibliotecas Essenciais**: Hugging Face Transformers, PEFT, Datasets, Evaluate, Sentence Transformers, ChromaDB.
