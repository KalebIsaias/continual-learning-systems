# **Proposta de Fomento ao Aprendizado Contínuo em Sistemas Conversacionais**

## **Introdução**

O aprendizado contínuo é um paradigma essencial para manter sistemas conversacionais atualizados em um mundo em constante mudança. A tecnologia de grandes modelos de linguagem (LMs), como os apresentados por Jang et al. (2022), armazena uma vasta quantidade de conhecimento do mundo em seus parâmetros durante o pré-treinamento, permitindo que sejam usados em tarefas como perguntas e respostas, diálogo aberto e verificação de fatos. No entanto, o conhecimento do mundo muda rapidamente, e esses modelos enfrentam desafios para atualizar informações sem esquecer o conhecimento previamente aprendido, fenômeno conhecido como "esquecimento catastrófico" (McCloskey & Cohen, 1989).

Diante disso, é crucial propor soluções que permitam a atualização contínua do conhecimento em sistemas de IA conversacional, sem comprometer o desempenho. Este trabalho propõe uma arquitetura baseada no conceito de "Continual Knowledge Learning" (CKL) (Jang et al., 2022), que visa integrar novos conhecimentos sem degradar o conhecimento antigo.

## **Solução Proposta**

### Arquitetura

### Descrição dos Módulos

<div style="display: flex; justify-content: center; align-items: center; margin-top: 20px;">
    <img src="https://github.com/user-attachments/assets/4fbe93c7-03a7-4392-8670-568197183478" alt="diagrama" style="width: 60%; border: 1px solid #ccc; padding: 10px;" />
</div>

- **Pré-treinamento contínuo**: O sistema deve ser capaz de ser continuamente pré-treinado com novos dados. Utiliza-se um processo de pré-treinamento incremental, como no benchmark CKL, para evitar o esquecimento de conhecimento invariante e integrar novas informações.
  
- **Memória externa**: Para lidar com o esquecimento catastrófico, propõe-se o uso de uma memória externa baseada em técnicas de recuperação de conhecimento, como a utilização de fontes externas em tempo real, similar aos modelos como o RAG (Lewis et al., 2020a).
  
- **Módulo de atualização de conhecimento**: Este módulo identifica e atualiza conhecimentos desatualizados sem alterar informações invariante. Ele utiliza o conjunto de dados "UPDATEDLAMA" proposto por Jang et al. (2022), que avalia o desempenho do modelo em atualizações de conhecimento.

- **Monitoramento e avaliação**: Um componente dedicado ao monitoramento da eficiência do processo de aprendizado contínuo, medindo o trade-off entre esquecimento de conhecimento e aquisição de novos fatos através de métricas como FUAR (Jang et al., 2022).

## **Conclusão**

A proposta de fomentar o aprendizado contínuo em sistemas conversacionais visa garantir que os modelos possam adquirir novos conhecimentos sem esquecer informações essenciais. A implementação dessa solução requer esforço significativo, especialmente na integração de novos métodos de treinamento contínuo e na gestão da memória externa para conhecimento. Contudo, os benefícios de manter os modelos atualizados em tempo real e melhorar a eficiência do sistema justificam esse investimento.

## **Referências**

- JANG, Joel; YE, Seonghyeon; YANG, Sohee; et al. Towards Continual Knowledge Learning of Language Models. ArXiv preprint, 2022. Disponível em: https://arxiv.org/abs/2110.03215v4.
- MCCLOSKEY, Michael; COHEN, Neal J. Catastrophic interference in connectionist networks: The sequential learning problem. *Psychology of Learning and Motivation*, v. 24, p. 109-165, 1989.
