
Suite de tratamento da base H2 para o dependency check
Nesta suite e possivel inicializar, parar, verificar status (se está online ou não), realizar backup, restore da base e atualização.

Sintaxe básica: h2 <parâmetro>

h2 <status|start|stop|backup|restore|update>

Exemplos de uso:

h2 status - Informa o status do banco

h2 start - Inicia o serviço do H2

h2 stop - Faz a parada do serviço do H2 usando SIGTERM, evitando assim o corrompimento da base.

h2 backup - Para o serviço do H2, faz o backup do arquivo de base (odc.mv.db) compactando e armazenando na pasta de backup informada nas variáveis de ambiente do código e inicializa novamente o serviço do H2.

h2 restore - Para o serviço do H2, Modifica o arquivo dc.mv.db atual (por questões de segurança e rollback), 

h2 update - Atualiza a base do dependency check, parando o serviço do H2 (evitando gravações concorrentes) e executa a atualização a nível de arquivo.
