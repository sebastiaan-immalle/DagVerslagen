﻿Dag1: Virtual machines
Soorten VM’s

Wat is een VM?
• Een virtuele machine is een computerprogramma dat een computer nabootst, waar andere programma's op kunnen worden uitgevoerd. Deze techniek wordt gebruikt om de overdraagbaarheid van programmatuur te verbeteren, en ook om het gelijktijdig gebruik van de computer door verschillende gebruikers robuuster te maken.
Waarom zou je het nodig hebben?	
• Meerdere OS-omgevingen kunnen gelijktijdig bestaan op dezelfde machine, geïsoleerd van elkaar; Virtuele machine kan een instructieset-architectuur bieden die verschilt van die van echte computers; Eenvoudig onderhoud, provisionering* van toepassingen, beschikbaarheid en handig herstel. 
Nadelen?:
-  Virtuele machines zijn minder efficiënt dan echte machines omdat ze indirect toegang hebben tot de hardware. Het draaien van software bovenop het host besturingssysteem betekent dat het de host om toegang tot de hardware moet vragen. Dat zal de bruikbaarheid vertragen.
provisionering*:Provisioning is het proces van het verstrekken van faciliteiten en permissies aan een persoon. De term is afkomstig van het Engelse werkwoord to provide, ofwel verstrekken of voorzien.
https://nl.wikipedia.org/wiki/Provisioning
GET:
GET: Vmware 
Virtual machine = belankrijk.
Veel virtual machines.
Meeste dingen gebeuren digitaal.
 
VMware:
VMware biedt een zeer uitgebreide selectie virtualisatieproducten, 
 Fusion = Apple Mac 
Workstation Player = de pc.
(dezelfde oplossing: 
het op maat gemaakt voor elk host-besturingssysteem)
 
 
Workstation is, zoals de versienummering suggereert, een volwassener product en levert een van de meest geavanceerde VM-implementaties tot nu toe.
 
Ondersteunt: DirectX 10 en OpenGL 3.3 
CAD & GPU-versnelde applicaties kunnen onder de virtualisatie werken.
 
(CAD(Computer-aided design): 
 CAD is het ontwerpen van onder meer constructies en apparaten met behulp van computerprogramma's.)

 
Workstation Player voor Windows of Linux is gratis voor persoonlijk gebruik
Pro is voor zakelijke gebruikers en voor degenen die beperkte VM's willen uitvoeren(=virtual machine willen beperken voor bepaalde omstandigheden) 


 
 
 




Hyper-V:
Viridian -> Windows Server Virtualization -> Hyper-V Server toen het voor het eerst werd uitgebracht eind 2008.
 
Tegenwoordig maakt het deel uit van Windows 10 Pro en Windows Server (2012 en 2016), geen extra kosten voor de gebruiker.
 
• een zeer eenvoudige hypervisor* die niet de slimme dingen kan die VMware biedt.
• Met Hyper-V kunnen relatief onervaren gebruikers een virtuele serveromgeving creëren.( Maar dan praten we wel over het minimale.)
• De gast OS-ondersteuning omvat Windows Server
Windows XP SP3 of hoger, Linux met een 3.4 of betere Kernel en FreeBSD.
 
 
• driverondersteuning voor Linux is niet geweldig en er is geen virtuele GPU-ondersteuning is. 








 



Hypervisor*: Meerdere virtuele machines kunnen tegelijkertijd op dezelfde fysieke computer worden uitgevoerd, allemaal beheerd door een hypervisor.

Virtualbox:
 
• Dan is VirtualBox een goede keuze omdat het een verbazingwekkend brede selectie van host- en clientcombinaties ondersteunt.
• Windows vanaf XP, elk Linux-niveau 2.4 of beter, Windows NT, Server 2003, Solaris, OpenSolaris en zelfs OpenBSD Unix.
(Er zijn zelfs mensen die nostalgisch Windows 3.x of zelfs IBM OS/2 draaien op hun moderne systemen
• Het werkt ook op Apple Mac en voor Apple-gebruikers kan het een client Mac VM-sessie hosten.
• Oracle ondersteunt VirtualBox en gaf een brede selectie vooraf gebouwde VM's voor ontwikkelaars om gratis te downloaden en te gebruiken.
 
• En dit alles is gratis, zelfs de Enterprise-release.


















Virtualisatie:

ESX host:
ESX-hosts zijn de servers/gegevensopslagapparaten waarop de ESX- of ESXi-hypervisor is geïnstalleerd. Het gebruik van hypervisors zoals ESX en ESXi om VM's te creëren (virtualisatie) is zeer efficiënt, aangezien één hostapparaat meerdere (tot een dozijn of meer) VM's kan ondersteunen.

In plaats van meerdere VM’s te instaleren kan je één ESXhost hebben. Je kan geld besparen 




Type-1, native of bare-metal hypervisors
Deze hypervisors draaien rechtstreeks op de hardware van de host om de hardware te controleren en gastbesturingssystemen te beheren. Om deze reden worden ze ook wel bare-metal hypervisors genoemd. De eerste hypervisors, die IBM in de jaren zestig ontwikkelde, waren native hypervisors.[4] Hiertoe behoorden de testsoftware SIMMON en het besturingssysteem CP/CMS, de voorloper van IBM z/VM. Moderne equivalenten zijn onder meer AntsleOS,[5] Microsoft Hyper-V en Xbox One systeemsoftware, Nutanix AHV, XCP-ng, Oracle VM Server voor SPARC, Oracle VM Server voor x86, POWER Hypervisor,[6] QNX Hypervisor,[7] VMware ESXi (voorheen ESX), Proxmox Virtual Environment en Xen.


Type-2 of gehoste hypervisors
Deze hypervisors draaien op een conventioneel besturingssysteem (OS), net zoals andere computerprogramma's dat doen. Een gast-besturingssysteem draait als een proces op de host. Type 2-hypervisors abstraheren gast-besturingssystemen van het host-besturingssysteem. Parallels Desktop voor Mac, QEMU, VirtualBox, VMware Player en VMware Workstation zijn voorbeelden van type 2-hypervisors.
Het onderscheid tussen deze twee typen is niet altijd duidelijk. Kernel-based Virtual Machine (KVM) en bhyve zijn bijvoorbeeld kernelmodules*[8] die het host-besturingssysteem effectief omzetten in een type-1 hypervisor.[9] Tegelijkertijd kunnen KVM en bhyve, aangezien Linux-distributies en FreeBSD nog steeds general-purpose besturingssystemen zijn, waarbij applicaties met elkaar concurreren om VM-resources, ook worden gecategoriseerd als type-2 hypervisors.[10]
Met type 2 (gehoste hypervisors) kan je dingen doen bv. VPN op VMware ESXhost plaatsen. 
Zodat als je wilt verbinden met een klant. En je een VPN moet gebruiken verbind met VMware en dan verbind je met de klant. Inplaats van handmatig een VPN op alle pc’s te plaatsen.

Er zijn ook manieren om er illegaal gebruik van te maken. Bv. Hyperjacking*. Het is de cybersecurity team’s job om dit te vermijden. Er zijn 2 simpele manieren hiervoor:

1. Verbind de beheerfuncties van uw hypervisor nooit met een minder veilige omgeving dan de virtuele instanties. Plaats de toegang tot uw beheerfuncties niet in de DMZ. Hoewel dit klinkt als een kwestie van gezond verstand, hebben we allemaal wel eens horrorverhalen gehoord. Zorg dat je niet het horrorverhaal wordt.

2. Je gast besturingssystemen mogen nooit toegang hebben tot de hypervisor. Ze mogen er ook niets van weten. Gast besturingssystemen mogen nooit weten dat ze virtueel zijn. En uw hypervisor mag een gast besturingssysteem nooit vertellen dat het gehost wordt. Geheim geheim.






Snapshots:
Een snapshot van een virtuele machine is slechts een afbeelding van de toestand en gegevens van een virtuele machine, die op een bepaald tijdstip wordt vastgelegd en opgeslagen. De VM-status kan als volgt zijn: actief, uitgeschakeld, onbekend, opgeschort, afgebroken of gepauzeerd, en actief of losgekoppeld. De gegevens van een virtuele machine omvatten alle bestanden op schijf, in het geheugen en op andere ondersteunde opslagapparaten.
Tip: Net voordat je jouw VM voor het eerst opstart maak je altijd een snapshot. Als je later bv. Wilt clean beginnen in jouw VM dan haal je die snapshot terug naar boven. In plaats van een nieuwe VM te maken. Want dan verlies je jouw Windows Licentie.

Kernelmodules*:Kernel modules are pieces of code that can be loaded and unloaded into the kernel upon demand.
Hyperjacking*: is een aanval waarbij een hacker controle krijgt over de hypervisor die de virtuele omgeving creëert binnen een virtuele machine (VM) host.


Lager stroomverbruik en koeling
Als gevolg van deze efficiëntie hoeft u in verhouding minder hardware aan te schaffen om uw bedrijfsprocessen te draaien. Dit leidt logischerwijs tot een lager stroomverbruik van uw IT-omgeving, minder vereiste koeling en uiteraard minder ruimte.

Disaster Recovery*
Disaster Recovery staat niet voor niets hoog op het lijstje van prioriteiten voor veel bedrijven en hier is nog makkelijker aan te voldoen dankzij virtualisatie. Mede dankzij snapshots, back-up functionaliteiten en het loskoppelen van processen van de fysieke hardware. De virtuele omgevingen kunnen zodoende op meerdere servers tegelijkertijd worden gedraaid. In het geval van problemen met de ene server, kunnen deze omgevingen snel worden overgenomen door een andere server.

Disaster Recovery*:Disaster Recovery omvat een reeks beleidslijnen, tools en procedures om het herstel of de voortzetting van vitale technologische infrastructuur en systemen mogelijk te maken na een natuurramp of een door de mens veroorzaakte ramp.
Hogere uptime
Downtime moet zoveel mogelijk worden voorkomen. Daarom is het fijn dat virtuele machines niet hoeven te worden verstoord bij het toevoegen van hardware zoals geheugen, processors of zelfs volledige servers. Daarnaast kunnen virtuele machines ook gemakkelijk worden gemigreerd van de ene hardware naar de andere. In veel gevallen is dit migreren zelfs mogelijk zonder enige vorm van downtime.

Testomgevingen
Een afgeschermde virtuele omgeving creëert een perfecte gelegenheid om te testen. Fouten hebben geen directe gevolgen voor cruciale processen die niet mogen worden verstoord. En zodra u tevreden bent met de testomgeving kan deze gemakkelijk worden verplaatst naar een live omgeving.
Windows licensie VM clean te maken…
Esx host.
Revert to Snapshots.
Cloud
Door de virtuele omgevingen en processen los te koppelen van de onderliggende hardware is het uiteindelijk ook makkelijker om de overstap te maken richting de private of public cloud. Een ontwikkeling die ook sterk blijft groeien en voordelen kan bieden voor uw organisatie. 

Kostenbesparing
Minder vereiste hardware, minder koeling, minder stroomverbruik, minder downtime, vereenvoudigd beheer en een hogere flexibiliteit. Al deze punten leiden tot een kostenbesparing die over de langere termijn flink kan oplopen.

Het mag duidelijk zijn dat virtualisatie een groot voordeel kan opleveren voor uw organisatie. Virtualisatie is een krachtige tool en kan op verschillende manieren en op verschillende niveaus worden toegepast. Niet alleen op het gebied van server virtualisatie, maar ook bij storage- en netwerkvirtualisatie.

















Interessante dingen over virtual machines:

CubeOS:
	Een OS waar alles bijna in een VM is. 

























Dag2: Netwerk

DMZ: een demilitarized zone, is een computernetwerk dat bereikbaar is van buitenaf (buiten de organisatie netwerk). het wordt beschermt door een firewall maar moet zo ingesteld worden (gaten in de firewall) zodat diensten nog mogelijk zijn. Het checkt of verbinding van een privé laptop/pc wel zijn toegestaan. Het wordt ook als een veiligheidszone gezien.

Port Address Translation (PAT) Geeft Meerdere pc’s op een LAN één publiek IP-adres.  Als een pc inlogt krijgt hij dezelfde IP-adres als andere pc’s op dezelfde LAN maar een andere port nummer.

2x 2-poorts firewalls: 2 firewalls waarbij de DMZ tussen de firewalls bevindt

1x 3-poorts firewall: 1 firewall waarbij de DMZ rechtstreeks verbinding mee maakt.






VPN: een vpn is een Virtueel persoonlijk Netwerk en zorgt voor beveiliging van jouw verbindingen en anonimiteit.  

PPTP (Point to Point Tunneling Protocol): is een VPN dat 2 LAN’s verbindt. Het creëert een tunnel door het internet waar je veilig informatie kan doorgeven. Vaak is het zo dat de computer van de ene netwerk als server dient en de andere als client.

WireGuard: gratis en open-source software die versleutelde virtuele privénetwerken implementeert 
• Voordeel:
o Open source
o Gratis
o Hoge prestatie

• Nadeel:



OpenVPN: open source VPN dat OpenSSL* en SSLv3/TLSv1* protocol gebruikt voor versleuteling.


• Voordeel:
o Open source

• Nadeel:
o Kan geen traffic schijden

OpenSSL*: opensource implementatie van het SSL/TLS protocol
SSLv3/TLSv1 (Transport Layer Security)*: SSL zorgt voor een veilige communicatie 

Site-to-Site VPN:  is een verbinding tussen 2 permanente locaties.

Niet ideaal voor het thuiswerken











IPsec (internet protocol security)/ L2TP: de netwerk beheerder heeft macht over poort 500.
Als poort 500 dicht is dan is de VPN protocol onbruikbaar. (je kan geen verbinding maken.)

       Kan gebruikt worden om van thuis te werken.

• Voordeel: 
o je kan veilig verbinding maken het bedrijf netwerk met een wachtwoord en een username.

• Nadeel:
o  je hebt een clientapplicatie nodig voor uw privé pc/laptop en als je er 2 wilt verbinden dan moet je 2 licenties gebruiken in plaats van 1.

https://www.firewallshop.nl/klantenservice/informatie/thuiswerken-via-vpn/



SSL VPN (Secure Socket Layer):  gebruikt een webbrowser. Het creëert een tunnel wanneer de webbrowser wordt opgestart (https verbinding). Er wordt wel nog altijd gevraagd voor jouw wachtwoord en username op de webbrowser zelf. 
       
       Het meest populaire protocol voor thuiswerken
       
• Voordeel:
o  geen clientapplicatie nodig.
o kan veilig verbinding maken het bedrijf netwerk
o eenvoudig gebruik
o kan op meerdere devices werken (smartphone, laptop, tablet, ect.)


PABX(Private Automatic Branch eXchange ): een telefooncentrale voor bedrijven
Het heeft 3 hoofdtaken: 
• Verbinding maken met 2 telefoontoestellen
• Verbinding behouden
• Informatie en statistieken behouden









• IP-adress:
o IPv4 is een 32-bit (wordt gescheiden door puntjes) 
o IPv6 is een 128-bit (wordt gescheiden door een colon) 
o Ipv-6


	SAAS(Software as a Service): is een software dat een client kan huren met een abonnement.
		(Bv. Netflix, Office 365,ect.) 











Switches: een apparaat waarmee werknemers efficiënter mee kunnen communiceren.
Cisco switches:
• Voordeel:
o Cisco-switches hebben geïntegreerde beveiliging
o Vereenvoudig het managen van mobiliteit, Internet of Things (IoT), datacenter en cloud
o uitgebreid portfolio van switches (daarom ideaal voor bedrijven)

• Nadeel:
o Kan duur zijn voor kleine bedrijfjes. 

HP aruba:
• Voordeel:
o Bekent voor hun prestaties en betrouwbaarheid.
o Heeft HPE Smart Rate multi-gigabit-poorten voor snelle verbindingen.
o moderne, programmeerbare schakelaars.
o Heel aruba is ontworpen om te voldoen aan de uitdagingen van de mobiele cloud en het IoT-tijdperk, waarin zichtbaarheid, automatisering en beveiliging uitgegroeid zijn tot een platform om te overleven
o Deze switches worden geleverd met ingebouwde beveiligingsfuncties die zijn ontworpen voor mobiel en IoT.


• Nadeel:
o Meer aan de dure kant.







FireWalls: is een systeem dat netwerken en computers kan beschermen tegen ongewenste gedoe van buitenaf.

Er zijn 4 soorten firewalls:
• Packet filtering firewall.
o Met paar zelf ingestelde regels bepaalt de firewall of een IP-pakket wordt doorgelaten of tegengehouden (in de netwerklaag)
• Application layer firewall.
o Voor elk ondersteund protocol bepaalt een stukje software of pakketjes worden tegengehouden of doorgelaten (in de applicatielaag)
• Stateless firewall.
o controleert elk pakketje op zichzelf
• Stateful firewall.
o houdt informatie bij van connecties die door de firewall gaan.
Voorbeeld van een soort firewall gebruikt in bedrijven:
• Watchguard:
o complete security
o zeer hoge prestatie
o ideaal voor middelgrote en gedistribueerde bedrijfsorganisaties.	
GET’s Topologie: (image)










verbeteringen voor GET: (image)


(Distributed ster-topologie)
*DMZ tussen 2 fire walls.* Dit is wel een verbetering maar het ideaalste is dat de 2 firewals naast elkaar tussen het internet en het bedrijfsnetwerk zit. Zodat als 1 firewall uit gaat dat het bedrijf nog internet heeft omdat er een 2de firewall klaar staat.







FireWalls: is een systeem dat netwerken en computers kan beschermen tegen ongewenste gedoe van buitenaf.

Er zijn 4 soorten firewalls:
•	Packet filtering firewall.
o	Met paar zelf ingestelde regels bepaalt de firewall of een IP-pakket wordt doorgelaten of tegengehouden (in de netwerklaag)
•	Application layer firewall.
o	Voor elk ondersteund protocol bepaalt een stukje software of pakketjes worden tegengehouden of doorgelaten (in de applicatielaag)
•	Stateless firewall.
o	controleert elk pakketje op zichzelf
•	Stateful firewall.
o	houdt informatie bij van connecties die door de firewall gaan.
Voorbeeld van een soort firewall gebruikt in bedrijven:
•	Watchguard:
o	complete security
o	zeer hoge prestatie
o	ideaal voor middelgrote en gedistribueerde bedrijfsorganisaties.	
GET’s Topologie: (image)










verbeteringen voor GET: (image)

 
(Distributed ster-topologie)
*DMZ tussen 2 fire walls.* Dit is wel een verbetering maar het ideaalste is dat de 2 firewals naast elkaar tussen het internet en het bedrijfsnetwerk zit. Zodat als 1 firewall uit gaat dat het bedrijf nog internet heeft omdat er een 2de firewall klaar staat.

