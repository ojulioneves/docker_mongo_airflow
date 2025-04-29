# docker_mongo_airflow
Repositório com os arquivos necessários para e instalação e configuração do banco de dados MongoDB no Docker, instalação e configuração da interface gráfica Mongo Compass e a instalação e configuração do Apache Airflow

1° Passo:
-Instalação do Docker no site oficial
https://www.docker.com

2° Passo: 
-Instalação da interface gráfica Mongo Compass no site do MongoDB
https://www.mongodb.com/try/download/compass

3° Passo:
- Eu vou disponibilizar para vocês a pasta zip com todos os arquivos necessários para a instalação do AirFlow e do MongoDB no Docker, baixem e descompactem.

4° Passo:
- Abram o prompt da máquina de vocês e digitem os códigos, respectivamente:
  
   1 - cd (caminho da pasta descompactada com os arquivos)

   2 - docker compose up airflow-init

   3 - docker compose up -d

- Pront seu ambiente já está criado!
- Para acessar o servido web do AirFlow basta entrar na porta que ele está ocupando, ou você pode clicar nela no própio docker
- ![image](https://github.com/user-attachments/assets/ce1a2744-c7f9-4b8f-bc09-655a460fc330)
-  Login: airflow  senha: airflow  


  5° Passo:
  -Configurando o MongoDB no AirFlow
  
  ![image](https://github.com/user-attachments/assets/976f4f69-edca-4008-8999-42a720ca3e42)
  
  2 - No canto superior direito vai ter a caixa "Add Connection", nela vocês vão preencher com as seguintes configurações
  
  ![image](https://github.com/user-attachments/assets/adfdcfc7-5bcd-4a74-a305-8325d906e31d)

  - Caso não esteja aparecendo a Connection Type (mongo), será necessário instalar a providers package do Mongodb:
  - Abra o prompt da sua máquina novamente e copie os seguintes códigos
  - cd (caminho da pasta descompactada com os arquivos)
  - docker exec -it airflow-airflow-apiserver-1 bash
  - pip install apache-airflow-providers-mongo
  - Reinicie o AirFlow
  - docker-compose restart airflow-apiserver
    Pronto problema resolvido!

    No campo Extra Fields JSON adicione o código abaixo:
 ![image](https://github.com/user-attachments/assets/0075fd06-384c-4386-b77f-579c5b170fa9)

Código:
{
  "srv": null,
  "authSource": "admin",
  "ssl": false,
  "allow_insecure": null
}

Depois de ter executados todos esses passos seu MongoDB estará conectado no AirFlow. Agora vamos para a configuração do Mongo Compass.
- Após instalar o Compass, basta digitar a url : mongodb://root:example@localhost:27017/admin
  ![image](https://github.com/user-attachments/assets/cdbc200b-d4e8-4a81-9a2f-54497d5b6e59)

- Pronto a instalação e configuração de todos foi concluída.
  






    
