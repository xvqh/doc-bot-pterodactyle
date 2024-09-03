<h1 align="center">
  🛠️ 〢 Comment se connecter en utilisant Pterodactyl pour le relier à son bot.
</h1>

## 🖥️ 〢 Comment accéder à votre panel Pterodactyl

*Tout d'abord, veuillez lancer votre navigateur (Google, Opera, Firefox, etc.) via ce lien qui est totalement sécurisé et gratuit: [Google](https://google.com).*

*Une fois que vous êtes sur Google, veuillez entrer l'URL de redirection de votre panel Pterodactyl dans la barre de recherche. Lorsque vous accédez à votre panel Pterodactyl, connectez-vous à votre compte (administrateur uniquement). Une fois connecté, veuillez suivre les instructions avec les captures d'écran suivantes.*

- *Accéder au panel admin*
  
  ![Screen](https://imgur.com/xIZ97uA.png)
  
- *Accéder à l'Api*
  
  ![Screen](https://imgur.com/3Y3JeC5.png)

- *Crée une api key*
  
  ![Screen](https://imgur.com/ICog9je.png)

- *Configuration de l'api key*
  
  ![Screen](https://imgur.com/rL1LChu.png)

- *Accedér au eggs nodejs/python*
  
  ![Screen](https://imgur.com/rHKd670.png)

- *Mettez Discord (ou selon vos configurations)*
  
  ![Screen](https://imgur.com/FYrkCYz.png)

- *Accéder à nodejs/python et copier leurs id*
  
  ![Screen](https://imgur.com/KUpiliZ.png)

- *Ensuite cliqué sur nodejs/python*
  
  *Nodejs:*![Screen](https://imgur.com/XKFC9xg.png)

*Copié le docker image ça doit ressembler a ceci: ghcr.io/parkervcp/yolks:nodejs_21*

  *Python:*![Screen](https://imgur.com/fucGHQ3.png)

*Copié le docker image ça doit ressembler a ceci: ghcr.io/parkervcp/yolks:python_3.12*

- *Ensuite Startup nodejs/python (sur la meme page)*
  
  *Nodejs:*![Screen](https://imgur.com/XKFC9xg.png)

*Copié le startup ça doit ressembler a ceci: `if [[ -d .git ]] && [[ {{AUTO_UPDATE}} == "1" ]]; then git pull; fi; if [[ ! -z ${NODE_PACKAGES} ]]; then /usr/local/bin/npm install ${NODE_PACKAGES}; fi; if [[ ! -z ${UNNODE_PACKAGES} ]]; then /usr/local/bin/npm uninstall ${UNNODE_PACKAGES}; fi; if [ -f /home/container/package.json ]; then /usr/local/bin/npm install; fi; if [[ "${MAIN_FILE}" == "*.js" ]]; then /usr/local/bin/node "/home/container/${MAIN_FILE}" ${NODE_ARGS}; else /usr/local/bin/ts-node --esm "/home/container/${MAIN_FILE}" ${NODE_ARGS}; fi`*

  *Python:*![Screen](https://imgur.com/fucGHQ3.png)

*Copié le startup ça doit ressembler a ceci: `if [[ -d .git ]] && [[ "{{AUTO_UPDATE}}" == "1" ]]; then git pull; fi; if [[ ! -z "{{PY_PACKAGES}}" ]]; then pip install -U --prefix .local {{PY_PACKAGES}}; fi; if [[ -f /home/container/${REQUIREMENTS_FILE} ]]; then pip install -U --prefix .local -r ${REQUIREMENTS_FILE}; fi; /usr/local/bin/python /home/container/{{PY_FILE}}`*

- *Configuré l'api client (retourner a l'accueil Pterodactyle)*
  
  ![Screen](https://imgur.com/1k9ephw.png)

- *Accéder à l'api client*
  
  ![Screen](https://imgur.com/qteXwvJ.png)

- *Crée l'api client*
  
  ![Screen](https://imgur.com/BwcVUZb.png)

- *Un fois crée copié la key.*
  
  ![Screen](https://imgur.com/SEr3TSZ.png)


*Configuré maintenant votre bot !*

## 🌐 〢 Configuration

*Remplissez le `config.js` avec les informations données (Info importante : "limits" est la configuration de l'espace de vos serveurs crée.).*

![Screen](https://imgur.com/gtSd8Fo.png)

---

<h1 align="center">
  🛠️ 〢 How to connect using Pterodactyl to link it to your bot.
</h1>

## 🖥️ 〢 How to access your Pterodactyl panel

*First, please open your browser (Google Chrome, Opera, Firefox, etc.) and go to this link, which is completely secure and free: [Google](https://google.com).*

*Once you are on Google, please enter the redirect URL for your Pterodactyl panel in the search bar. When you access your Pterodactyl panel, log in to your account (administrator only). Once logged in, please follow the instructions and the following screenshots.*

- *Access the admin panel*
  
  ![Screen](https://imgur.com/xIZ97uA.png)
  
- *Access the API*
  
  ![Screen](https://imgur.com/3Y3JeC5.png)

- *Create an API key*
  
  ![Screen](https://imgur.com/ICog9je.png)

- *API Key Configuration*
  
  ![Screen](https://imgur.com/rL1LChu.png)

- *Access Node.js/Python eggs*
  
  ![Screen](https://imgur.com/rHKd670.png)

- *Enter Discord (or according to your configurations)*
  
  ![Screen](https://imgur.com/FYrkCYz.png)

- *Access Node.js/Python and copy their IDs*
  
  ![Screen](https://imgur.com/KUpiliZ.png)

- *Then click on Node.js/Python*
  
  *Nodejs:*![Screen](https://imgur.com/XKFC9xg.png)

*Copy the Docker image it should look like this: ghcr.io/parkervcp/yolks:nodejs_21*

  *Python:*![Screen](https://imgur.com/fucGHQ3.png)

*Copy the Docker image it should look like this: ghcr.io/parkervcp/yolks:python_3.12*

- *Then configure the startup for Node.js/Python (on the same page)*
  
  *Nodejs:*![Screen](https://imgur.com/XKFC9xg.png)

*Copy the startup it should look like this: `if [[ -d .git ]] && [[ {{AUTO_UPDATE}} == "1" ]]; then git pull; fi; if [[ ! -z ${NODE_PACKAGES} ]]; then /usr/local/bin/npm install ${NODE_PACKAGES}; fi; if [[ ! -z ${UNNODE_PACKAGES} ]]; then /usr/local/bin/npm uninstall ${UNNODE_PACKAGES}; fi; if [ -f /home/container/package.json ]; then /usr/local/bin/npm install; fi; if [[ "${MAIN_FILE}" == "*.js" ]]; then /usr/local/bin/node "/home/container/${MAIN_FILE}" ${NODE_ARGS}; else /usr/local/bin/ts-node --esm "/home/container/${MAIN_FILE}" ${NODE_ARGS}; fi`*

  *Python:*![Screen](https://imgur.com/fucGHQ3.png)

*Copy the startup it should look like this: `if [[ -d .git ]] && [[ "{{AUTO_UPDATE}}" == "1" ]]; then git pull; fi; if [[ ! -z "{{PY_PACKAGES}}" ]]; then pip install -U --prefix .local {{PY_PACKAGES}}; fi; if [[ -f /home/container/${REQUIREMENTS_FILE} ]]; then pip install -U --prefix .local -r ${REQUIREMENTS_FILE}; fi; /usr/local/bin/python /home/container/{{PY_FILE}}`*

- *Configure the client API (return to the Pterodactyl homepage)*
  
  ![Screen](https://imgur.com/1k9ephw.png)

- *Access the API Client*
  
  ![Screen](https://imgur.com/qteXwvJ.png)

- *Create an API key Client*
  
  ![Screen](https://imgur.com/BwcVUZb.png)

- *Once created, copy the key.*
  
  ![Screen](https://imgur.com/SEr3TSZ.png)


*Now configure your bot !*

## 🌐 〢 Configuration

*Fill in the config.js with the provided information (important note: "limits" is the configuration for the space of your created servers).*

![Screen](https://imgur.com/gtSd8Fo.png)
