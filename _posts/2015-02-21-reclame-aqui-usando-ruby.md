---
layout: post
title: Verificando uma empresa no Reclame Aqui usando Ruby
---

Na [Agrid](http://agrid.com.br), um dos pilares da nossa proposta de valor é termos somente fornecedores confiáveis. Para garantir isso, fazemos algumas verificações que visam garantir que um fornecedor seja confiável e não possua débitos com a justiça ou reclamações não solucionadas de clientes. 

Uma das verificações feitas é a do ReclameAqui. Essa verificação é feita automaticamente após o cadastro do fornecedor e posteriormente conferida por um de nossos funcionários **agressores**.

Para solucionarmos esse problema, optamos por desenvolver uma gem que consultasse a reputação do fornecedor no ReclameAqui e nos dissesse se há ou não reclamaçõe desse fornecedor, nós a chamamos de [reclame_aqui](https://github.com/givigier/reclame_aqui). Sua utilização é bem trivial e basta que o utilizador passe o site da empresa que deseja consultar.

```ruby
ReclameAqui.reputation("http://ricardoeletro.com.br")
```

Futuramente pretendemos implementar a consulta também pelo nome. Caso você também seja um agressor e queira essa funcionalidade para ontem, basta fazer um fork do repositório da gem e implementar as mudanças. Também pretendemos fechar as issues o mais rápido possível, qualquer dúvida, manda lá!

