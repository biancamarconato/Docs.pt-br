**Aviso**: O código a seguir usa `GetTempFileName`, que gera um `IOException` se mais de 65.535 arquivos são criados sem excluir os arquivos temporários anteriores. Um aplicativo real deverá excluir arquivos temporários ou use `GetTempPath` e `GetRandomFileName` para criar nomes de arquivo temporário. O limite de 65535 arquivos é por servidor, para que possa usar outro aplicativo no servidor de backup de todos os arquivos de 65535. 