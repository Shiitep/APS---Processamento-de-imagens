# APS---Processamento-de-imagens
Repositório do código fonte para a APS
SENTINELA — Sistema de Identificação e Autenticação Biométrica Facial
=====================================================================
APS de Processamento de Imagem e Visão Computacional (PIVC) — UNIP 2026/2
Davi Rodrigues Nanartonis — RA R100CH9

COMO EXECUTAR (código-fonte)
----------------------------
1. Extraia SENTINELA_codigo_fonte.zip.
2. No prompt de comando, dentro da pasta:
      python -m venv .venv
      .venv\Scripts\activate
      pip install -r requirements.txt
      python ferramentas\baixar_modelos.py
      python main.py

PRIMEIROS PASSOS NO PROGRAMA
----------------------------
- Cadastrar (F3): informe nome, RA e nível (1, 2 ou 3) e capture 5 amostras
  pela câmera ou importe fotos.
- Autenticar (F2): posicione-se e mova levemente a cabeça quando solicitado.
- Consultas (F4): usuários, registros de acesso e desbloqueio da estação.
- Relatórios (F5): PDF, HTML e CSV do dia.

DOCUMENTAÇÃO
------------
- README.md ....... instalação, arquitetura, as cinco fases, configuração.
- MANUAL.md ....... manual do operador (uso diário).
TESTES
------
    pytest testes -q      (39 testes)

OBSERVAÇÃO SOBRE OS MODELOS
---------------------------
O programa usa dois modelos pré-treinados do OpenCV Zoo:
  - face_detection_yunet_2023mar.onnx  (detecção facial + 5 pontos)
  - face_recognition_sface_2021dec.onnx (descritor facial de 128 dimensões)
Ambos são executados em CPU, sem GPU, e já acompanham o pacote.
