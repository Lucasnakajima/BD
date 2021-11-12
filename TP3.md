1-

CLASSES

Marca(*idMarca*, nome, origem, pontos);
Carro(*idCarro*, Peso, Potencia, Velocidade Máxima, idMarca->Marca);
Piloto(*idPiloto*, Nome, Morada, Idade, Nacionalidade, Pontos, idCarro -> Carro);
Circuito(*idCircuito*, Nome, Local, Pais, Perímetro);
Corrida(*idCorrida*, Data, Número de Voltas,idCircuito->Circuito)


ASSOCIAÇÕES

Participação(*idPiloto -> Piloto*, *idCorrida -> Corrida*, posiçãoGrelha, Classificação Final);
Desistência(*idPiloto -> Piloto*, *idCorrida -> Corrida*, numeor da volta, Motivo);



3-

CLASSES

Cliente(*idCliente*, título, nome, Morada, Código Postal, Localidade, Telefone);
TipoConta(*idTipo*, Nome);
Conta(*idConta*, Numero da conta, idTipo -> TipoConta, Saldo);
TipoMovimento(*IdTipoMovimento*, nome);

ASSOCIAÇÕES

titular(*idConta* -> conta, *idCliente* -> Cliente, titularidade);
Movimentos(*idMovimento*, montante, data, *IdTipoMovimento* -> Movimentos, idcontaorigem -> Conta, idcontadestino -> Conta);




6-

CLASSES

Evento(*idEvento*, Minuto, idjogo -> Jogo, idJogador -> Jogador, TipodeEvento_Descrição);
Substituição(*IdEvento* -> Evento, IdjgEntra -> Jogador);
