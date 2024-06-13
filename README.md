# Servidor-web-IIS
# Guia per Instal·lar, Crear i Administrar un Lloc Web amb IIS

## Requisits Previs
- Un equip amb Windows 10, Windows Server 2016 o superior.
- Accés administratiu a l'equip.

## 1. Instal·lació de l'IIS

### Pas 1: Obrir el Tauler de Control
1. Fes clic al botó **Inici** i escriu "Tauler de Control".
2. Obre el **Tauler de Control**.

### Pas 2: Activar Característiques de Windows
1. Al Tauler de Control, selecciona **Programes**.
2. Fes clic a **Activar o desactivar les característiques de Windows**.

### Pas 3: Seleccionar IIS
1. A la finestra de Característiques de Windows, cerca **Internet Information Services**.
2. Marca la casella al costat de **Internet Information Services** i expandeix l'arbre per seleccionar les característiques desitjades. Assegura't d'incloure **IIS Management Console**.
3. Fes clic a **Acceptar**.

### Pas 4: Completar la Instal·lació
1. Espera que Windows instal·li l'IIS. Això pot trigar uns minuts.
2. Una vegada completada la instal·lació, tanca la finestra.

## 2. Configuració Bàsica de l'IIS

### Pas 1: Obrir el Gestor de l'IIS
1. Prem **Win + R**, escriu `inetmgr`, i prem **Enter**. Això obrirà el Gestor d'Internet Information Services (IIS).

### Pas 2: Verificar la Instal·lació
1. Al panell de connexions de l'esquerra, expandeix el node de l'equip local.
2. Selecciona **Llocs**.
3. Veureu el lloc predeterminat anomenat **Default Web Site**. Això confirma que l'IIS està instal·lat correctament.

## 3. Creació d'un Nou Lloc Web

### Pas 1: Crear la Carpeta del Lloc Web
1. Crea una carpeta a `C:\inetpub\wwwroot\` anomenada `ElMeuLlocWeb`.

### Pas 2: Afegir Contingut al Lloc Web
1. Dins la carpeta `ElMeuLlocWeb`, crea un fitxer anomenat `index.html`.
2. Obre el fitxer amb un editor de text (com Notepad) i afegeix el següent contingut bàsic:
    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>El Meu Primer Lloc Web</title>
    </head>
    <body>
        <h1>Benvingut al Meu Primer Lloc Web en IIS</h1>
    </body>
    </html>
    ```
3. Desa i tanca el fitxer.

### Pas 3: Configurar el Nou Lloc a l'IIS
1. Al Gestor de l'IIS, fes clic amb el botó dret a **Llocs** i selecciona **Afegeix lloc web...**.
2. Al quadre de diàleg, completa els següents camps:
    - **Nom del lloc:** ElMeuLlocWeb
    - **Ruta física:** C:\inetpub\wwwroot\ElMeuLlocWeb
    - **Host name:** Deixa aquest camp en blanc o afegeix un nom de domini si en tens un configurat.
3. Fes clic a **Acceptar**.

## 4. Administració del Lloc Web

### Pas 1: Iniciar i Aturar el Lloc Web
1. Al Gestor de l'IIS, selecciona el lloc web **ElMeuLlocWeb**.
2. Al panell d'accions a la dreta, pots fer clic a **Iniciar** per engegar el lloc, i a **Aturar** per apagar-lo.

### Pas 2: Configuració de Permisos i Autenticació
1. Selecciona el lloc **ElMeuLlocWeb** i fes clic a **Autenticació** al panell central.
2. Configura els mètodes d'autenticació segons sigui necessari (per exemple, habilitar **Autenticació anònima**).

### Pas 3: Administració dels Logs
1. Al panell d'accions, fes clic a **Explorar** per obrir la carpeta de logs del lloc.
2. Revisa els fitxers de log per monitoritzar el trànsit i solucionar problemes.

## 5. Accés al Lloc Web

1. Obre un navegador web.
2. Escriu `http://localhost` o `http://localhost/ElMeuLlocWeb` a la barra d'adreces.
3. Hauries de veure la pàgina amb el missatge "Benvingut al Meu Primer Lloc Web en IIS".

## Consells Addicionals
- **Seguretat:** Assegura't de configurar les regles de tallafocs i els permisos d'usuari adequadament per protegir el teu servidor.
- **Backups:** Realitza còpies de seguretat regulars del teu contingut i configuracions de l'IIS.
- **Documentació:** Mantingues un registre de totes les configuracions i canvis realitzats a l'IIS per a futures referències.

Seguint aquests passos, els teus alumnes haurien de ser capaços d'instal·lar, configurar i administrar un lloc web bàsic utilitzant IIS.

