# Relatório da Aula 1 — Fundamentos de IA, Ambiente e Versionamento

## Introdução
Nesta primeira aula o objetivo foi assentar a base do curso antes de entrar na parte prática de fato. Trabalhamos a definição de Inteligência Artificial, as diferenças entre Machine Learning e Deep Learning, os tipos de aprendizado e, por fim, dois pontos voltados para a organização do trabalho: a criação de um ambiente isolado e o versionamento com Git e GitHub. A seguir registro o que foi abordado em cada parte.

## Conceito de Inteligência Artificial
A IA foi apresentada como a ciência que busca executar tarefas que normalmente exigiriam inteligência humana, como percepção, raciocínio, aprendizagem e tomada de decisão. O propósito central é construir sistemas capazes de pensar, aprender, adaptar-se e agir de forma inteligente.

Ficou claro que a IA funciona como uma área ampla, que reúne vários subcampos: redes neurais artificiais, processamento de linguagem natural, visão computacional, machine learning, robótica autônoma e processamento de áudio e voz. Para tornar o conceito mais concreto, foram citadas aplicações reais, como a otimização de rotas na coleta de lixo em cidades inteligentes, o monitoramento de plantações na agricultura, a inspeção de qualidade por câmeras na indústria e o apoio ao diagnóstico na área da saúde.

## Tipos de aprendizado
Um ponto que considerei importante foi a recomendação de, antes de iniciar qualquer projeto, responder a três perguntas: se há dados com a resposta correta, qual é o objetivo do problema e se a intenção é prever algo ou descobrir padrões. Essas respostas orientam a escolha do tipo de aprendizado.

No **aprendizado supervisionado**, o modelo é treinado com dados que já possuem a resposta esperada, ou seja, recebe a entrada (X) junto com a saída conhecida (y). É indicado para classificação, regressão e previsões. O exemplo usado foi o de imagens rotuladas de cães e gatos, que permitem ao modelo classificar uma imagem nova.

Já no **aprendizado não supervisionado**, o modelo recebe apenas os dados, sem rótulos, e precisa encontrar a estrutura por conta própria. É aplicado em agrupamento, clusterização e descoberta de padrões. O exemplo foi o de um conjunto de dados sem identificação que o modelo separa sozinho em grupos distintos. A forma mais simples de distinguir os dois é pela presença ou ausência de rótulos.

## Machine Learning e Deep Learning
A aula deixou clara a relação entre os dois. Ambos aprendem a partir de dados, mas a diferença está em quem define as características relevantes. No Machine Learning, em geral é o ser humano quem seleciona as features, e os exemplos citados foram árvore de decisão, regressão e SVM. No Deep Learning, que é uma subárea do ML baseada em redes neurais profundas, o próprio modelo aprende essas características de forma automática, como ocorre em CNNs, RNNs e Transformers.

Entendi também a hierarquia entre os conceitos: a IA contém o Machine Learning, que por sua vez contém o Deep Learning. Para fixar a diferença prática, comparamos duas aplicações: a previsão do preço de um imóvel, mais característica de ML, em que informo dados como tamanho, número de quartos e localização para obter um valor estimado; e o reconhecimento de imagens, típico de DL, em que a rede recebe os pixels e identifica sozinha quais padrões são importantes.

## Ambientes virtuais
A segunda parte da aula foi mais prática. O ambiente virtual foi descrito como um espaço isolado dentro do computador, onde se instalam as bibliotecas de um projeto sem afetar os demais — uma espécie de "caixinha separada" para cada aplicação. Dentro dela ficam apenas as dependências necessárias, com as versões controladas, mantendo o projeto independente do sistema.

A justificativa para o uso ficou evidente na comparação: sem o ambiente virtual surgem conflitos de versão, projetos quebram inesperadamente e as instalações ficam desorganizadas. Com ele, cada projeto fica isolado, é possível usar versões diferentes da mesma biblioteca, garante-se a reprodutibilidade e evita-se que um projeto interfira no outro. Foi reforçado que, em projetos reais de IA, esse cuidado não é opcional, e sim obrigatório. As ferramentas mencionadas foram o venv do Python e o Anaconda.

## Git e GitHub
Por fim, tratamos do versionamento. O Git foi apresentado como um sistema de controle de versão que permite salvar versões do código, acompanhar mudanças, retornar a estados anteriores e trabalhar em equipe, funcionando como um histórico inteligente do projeto. O GitHub, por sua vez, é a plataforma online onde esses projetos ficam armazenados, possibilitando compartilhar código, colaborar com outras pessoas, construir um portfólio profissional e manter os arquivos na nuvem.

A diferença entre trabalhar com e sem essas ferramentas também foi discutida. Sem o Git, perdem-se versões antigas, não há clareza sobre o que foi alterado e o trabalho em equipe se desorganiza. Com o Git, cada alteração fica registrada, é possível reverter problemas e o desenvolvimento segue um padrão profissional. Concluiu-se que o versionamento é essencial em projetos de tecnologia.

Como boas práticas de gerenciamento de repositório, foram destacados o uso do arquivo `.gitignore` para ignorar arquivos, a escrita de mensagens de commit claras, a adoção de estratégias de branch para organizar o fluxo, a documentação do projeto e o uso de tags para marcar pontos importantes do histórico.

Também revisamos os comandos básicos mais utilizados:

```bash
git clone URL                  # baixar um repositório do GitHub
git add .                      # preparar as alterações
git commit -m "mensagem"       # salvar no histórico
git push                       # enviar as mudanças para o GitHub
git pull                       # atualizar com o que está no GitHub
git branch                     # criar/listar branches
git checkout                   # trocar de branch
git merge                      # unir mudanças de uma branch
```

E a sequência típica para iniciar um projeto do zero:

```bash
git init
git status
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/repository.git
git push -u origin main
git log
```

## Conclusão
A aula cumpriu o papel de nivelar os conceitos antes da prática. Saí com a distinção entre IA, ML e DL bem definida, com clareza sobre quando usar aprendizado supervisionado ou não supervisionado e com a noção de por que ambiente virtual e versionamento são parte obrigatória de qualquer projeto sério de IA. Os próximos passos práticos são montar o ambiente isolado e criar o repositório próprio no GitHub.
