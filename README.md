<h1>#ElectricSelfConsumptionMonitor</h1>
<h2>Progetto per il monitoraggio della produzione, cosumo e scambio di energia elettrica di un sistema che integara un impianto di pannelli solari o eolico.</h2>
<p>L'hardware che si occupa di ricavare le quantit&agrave;di energia transitati sui fili dell'impianto &egrave; costituito da una scheda <strong>Arduino Uno</strong>,<br /> collegata alla rete tramite <strong>Ethernet-Shield</strong>.<br />La lettura dell'energia trasitate viene ricavata tramite 3 pinze amperometriche non invasive che vengono applicate</p>
<ul>
<li>sul filo che collega l'impiamto fotovoltaico al contatore.</li>
<li>sul filo che arriva dalla rete elettrica verso il contatore.</li>
<li>sul filo che collega il contatore con l'impiato elettrico di casa.</li>
</ul>
<p><img src="https://raw.githubusercontent.com/Umochi/AutomaticHenHouse/master/images/arduino_uno_main_board.jpg" alt="" width="200" height="200" /><img src="https://raw.githubusercontent.com/Umochi/AutomaticHenHouse/master/images/ethernet-shield.jpg" alt="Ethernet-Shield" width="200" />&nbsp;</p>
<p><img src="https://raw.githubusercontent.com/Umochi/ElectricSelfConsumptionMonitor/master/images/schemaEnergia.jpg" width="439" height="405" /></p>
<hr />
<p>La parte Hardware del sistema di monitoraggio, &egrave; costituira da un modulo <strong>Arduino Uno</strong>, integrato con una <strong>ethernet-shield</strong>, si collega alla rete lan e invia periodicamente le informazioni al server.<br />Al fine di ridurre il traffico dati, viene inviata una nuova lettura, solo quando questa varia in modo sensibile rispetto all'ultima inviata.<br />Viene invece inviata anche in caso di variazioni minime allo scadere di un timeout.</p>
<hr />
<h3>Il comportamento del sistema &egrave; il seguente:</h3>
<ul>
<li>Arduino</li>
<li>L'interfaccia pu&ograve; essere esposta su internet, nel mio caso utilizzo un servizio gratuito di <strong>DDNS</strong> e <strong>NginX</strong> per gestire reverse proxy e autenticazione.</li>
</ul>
