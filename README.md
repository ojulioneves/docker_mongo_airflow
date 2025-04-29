# docker_mongo_airflow
Repositório com os arquivos necessários para e instalação e configuração do banco de dados MongoDB no Docker, instalação e configuração da interface gráfica Mongo Compass e a instalão e configuração do Apache Airflow

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
1 - cd (caminho da pasta com arquivos)
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

  - username: root  senha: example
  - 
 ![image](https://github.com/user-attachments/assets/0075fd06-384c-4386-b77f-579c5b170fa9)

Código:
{
  "srv": null,
  "authSource": "admin",
  "ssl": false,
  "allow_insecure": null
}





    
