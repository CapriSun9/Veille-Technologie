# Veille-Technologie


Fin 2025 – grandes annonces cloud
3 novembre 2025 : OpenAI signe un accord d’infrastructure cloud d’environ 38 milliards de dollars avec AWS pour du compute IA à grande échelle.

5 novembre 2025 : Microsoft, Google, AWS, Oracle, SAP, Snowflake renforcent leurs partenariats croisés pour l’IA, montrant une forte interconnexion entre hyperscalers.

10 décembre 2025 : Microsoft annonce une première “AI superfactory” à Atlanta, reliant plusieurs datacenters avec des centaines de milliers de GPU et des exaoctets de stockage.

Fin décembre 2025 : plusieurs analyses parlent d’un “retour” de l’on‑prem en 2026 comme complément du cloud pour les workloads critiques, et d’un “tipping point” du cloud public (article du 26 janvier 2025, série d’analyses).

2025 – Sécurité et virtualisation
Fin mars 2025 : les architectures Zero Trust sont décrites comme en train de devenir un standard dans les environnements virtualisés pour limiter les mouvements latéraux entre VM et containers.

Toute l’année 2025 : montée en puissance des solutions de virtualisation type VMware, Hyper‑V et alternatives KVM/Proxmox, avec un focus sur la sécurité, l’isolation et la micro‑segmentation réseau.

Début 2026 – Coûts, IA et GPU
1ᵉʳ janvier 2026 : des articles indiquent que les coûts cloud deviennent le 2ᵉ poste de dépense IT des entreprises moyennes, juste derrière le personnel, surtout à cause des workloads IA et de la variabilité mensuelle des factures.

5 janvier 2026 : CoreWeave annonce l’adoption de la plateforme NVIDIA Rubin pour son cloud IA, avec des déploiements prévus en 2026, ce qui renforce la course aux GPU spécialisés.

5 janvier 2026 : plusieurs synthèses de “7 tendances cloud 2026” insistent sur l’optimisation d’infrastructures pour l’IA (GPU, réseau, stockage) et l’essor de clouds spécialisés (neoclouds).

21 janvier & 5 mars 2026 : Cisco corrige une critique zero‑day (CVE‑2026‑20045) et 48 vulnérabilités , dont deux CVSS 10/10, touchant les équipements réseaux indispensables aux architectures cloud/hybrides.

2–3 février 2026 : panne Azure de plus de 10 heures affectant VMs, AKS, Managed Identities et pipelines CI/CD, en raison d'une mauvaise configuration de comptes de stockage Microsoft.

5 mai 2026 : une faille cPanel critique (CVSS 9.8) menace plus d' un million de sites , avec exploitation active – renforce l'idée de ne jamais exposer directement un panel d'administrateur.

Mai 2026 : une extension malveillante provoque le vol de secrets GitHub, AWS, Kubernetes, Docker , affectant plusieurs milliers de dépôts privés, montrant que la supply chain dev devient un point clé de la sécurité cloud.

Toute la période : pénurie structurelle de mémoire DRAM liée à l'IA (HBM), augmentation des coûts serveurs, besoin d'optimiser la densité VM et le placement des workloads (on‑prem + cloud + neoclouds IA).

2025–2026 : les analyses sur la souveraineté des données soulignent un rééquilibrage régional, avec une opportunité pour les acteurs cloud européens et les clouds locaux alignés RGPD.

Outages, souveraineté et multicloud
Année 2025 (plusieurs dates) : gros outages AWS/Azure/GCP et de services SaaS provoquent des interruptions touchant des millions d’utilisateurs, mettant en avant la fragilité systémique et les dépendances en chaîne (DNS, paiements, sécurité, etc.).

Fin 2025 – début 2026 : de plus en plus d’architectures recommandent un modèle hybride/multicloud (on‑prem + plusieurs clouds) pour réduire le risque d’un seul point de défaillance et reprendre le contrôle des coûts.


Mise a jour - juillet 2026
Virtualisation & couts
Ete 2026 : comparatif Proxmox VE vs VMware post-Broadcom - Proxmox VE estime a ~1 000 EUR/an contre 45 000 EUR+/an pour VMware (licence Broadcom). Renforce l'interet de l'open source pour les homelabs et PME, axe cle de mon projet Proxmox.

Securite & CVE (cloud / cyber)
Juin 2026 : CVE-2026-48567 - Azure HorizonDB, elevation de privileges, CVSS 10.0 (Patch Tuesday juin 2026).
2026 : CVE-2026-20253 - Splunk Enterprise, authentification manquante sur fonction critique, ajoutee au catalogue CISA KEV (exploitation active). Souligne l'importance du patch management et de la supervision des logs.

Securite & CVE (homelab - juillet 2026)
6 juillet 2026 : Pi-hole FTL v6.7 / Core v6.4.3 corrige 6 avis dont une RCE (injection config CivetWeb, GHSA-8j7w-m3cr-6q6x) et une elevation de privileges local (pihole vers root via logrotate, GHSA-h8w9-qx2v-wrww). Mettre a jour via la commande 'pihole -up'.
2026 : Proxmox VE - "PinTheft" PSA-2026-00022-1 (CVE-2026-43494), elevation de privileges local (RDS + io_uring) ; et "DirtyFrag" PSA-2026-00019-1 (LPE noyau Linux, exploite dans la nature). Les deux corriges par les noyaux PVE a jour. Mise a jour via 'apt update' puis 'apt full-upgrade', suivi d'un reboot sur le noyau patche.


Mise à jour - 2026-07-24 (semaine du 20-24 juillet 2026)

Sécurité & CVE (virtualisation / cloud)
- CVE-2026-53359 "Januscape" : use-after-free dans KVM x86 (shadow-paging subsystem Linux kernel). Vulnérabilité vieille de plusieurs années, rendue publique le 6 juillet 2026. OVHcloud publie un retour d'expérience sur le patching de cette faille à travers des dizaines de milliers de machines. Impact direct sur tous les environnements virtualisés KVM/cloud. Source : blog OVHcloud, 21 juillet 2026.
- July 2026 Patch Tuesday (CrowdStrike) : CVE-2026-57092 - élévation de privilèges critique (CVSS 9.9) dans Microsoft Windows VMSwitch (use-after-free CWE-416). Attaquant authentifié peut élever ses privilèges sur le réseau avec une faible complexité. Source : CrowdStrike, 14 juillet 2026.
- Rappel : CVE-2026-47652 (juin 2026) - RCE critique (CVSS 8.2) dans Windows Hyper-V (heap-based buffer overflow). Contexte permanent de vulnérabilités hyperviseur.

Proxmox VE
- Proxmox VE 9.2 (sorti mai 2026) : introduction du Dynamic Load Balancer pour clusters HA. Migre en direct les VM des noeuds chauds vers les noeuds froids automatiquement (CPU, mémoire temps réel). Noyau Linux 7.0 par défaut. Amélioration majeure du Cluster Resource Scheduler. Source : Proxmox Pulse, 6 juillet 2026.

Hyperscalers & Cloud IA
- Google publie son "2026 State of AI Infrastructure Report" : +80% des organisations doivent mettre à jour leur stack technique pour supporter les agents IA à l'échelle. Source : CIO Dive, 10 juillet 2026.
- NVIDIA annonce un modèle de revenue-sharing et crédit (1er juillet 2026) pour les opérateurs de cloud IA. NVIDIA backstoppe le buildout d'infrastructure GPU (210 000 GPUs) pour les opérateurs capital-constraints. Source : Tech Times, 4 juillet 2026.
- AWS SQS fête ses 20 ans (2006-2026). AWS Weekly Roundup (20 juillet) : One-click Lambda setup, modèles OpenAI GPT-5.6 sur Bedrock. Source : Deven Goratela, 20 juillet 2026.
- Investissements IA hyperscalers confirmés à ~$725B en 2026 (Big-5). L'offre physique de capacité datacenter ne suit pas le rythme. Source : CFA Analysis / Q1 2026 earnings.

Cloud cost optimization & multicloud
- Multi-cloud et hybrid deviennent le nouveau défaut en 2026, notamment pour les équipes déployant des modèles IA. Objectifs : éviter le lock-in, optimiser le placement des données (compute locality, cache economics). Sources : nOps, MegaStorage Cloud, 2026.

Souveraineté des données & cloud européen
- Juin 2026 : la Commission européenne publie le "European Technological Sovereignty Package" - l'initiative la plus ambitieuse d'autonomie numérique européenne. Pièce centrale : le Cloud and AI Development Act (CADA), qui crée des obligations réglementaires, des standards de souveraineté et un plan d'investissement jusqu'en 2036. Source : CSA Research, juin 2026.
- Le EU Data Act et le Digital Omnibus entrent en vigueur en 2026. Les niveaux de cloud souverain (Sovereign Cloud levels) se structurent. Source : Cyso Cloud, 2026.
- La souveraineté numérique devient un enjeu de direction : données, IA, dépendance économique, autonomie stratégique européenne. Sources : eclipso, 13 juillet 2026 / eunews, 20 juillet 2026.

VMware / Broadcom
- La migration VMware vers le cloud s'accélère (de "slow-burn" à "urgent") en 2026. Les changements de licence Broadcom (VCF obligatoire pour nouveaux noeuds sur hyperscaler depuis octobre 2025, transition avant novembre 2026) poussent les clients à évaluer des alternatives. Source : MigrationCost.com, Sangfor, 2026.

Outages
- Aucun outage majeur hyperscaler détecté cette semaine (20-24 juillet 2026).

Sources :
- CVE-2026-53359 (Januscape) OVHcloud : https://blog.ovhcloud.com/cve-2026-53359-januscape-patching-campaign-lessons-learned-from-remediating-a-kvm-flaw-across-tens-of-thousands-of-machines/
- July 2026 Patch Tuesday (CrowdStrike) : https://www.crowdstrike.com/en-us/blog/patch-tuesday-analysis-july-2026/
- Proxmox VE 9.2 Dynamic Load Balancer : https://proxmoxpulse.com/articles/proxmox-dynamic-load-balancer-ha-clusters/
- Google State of AI Infrastructure 2026 : https://www.ciodive.com/topic/cloud/
- NVIDIA revenue-sharing AI cloud : https://www.techtimes.com/articles/319704/20260704/nvidia-revenue-sharing-ai-cloud-debuts-210000-gpus-flywheel-vendor-finance-risk.htm
- AWS Weekly Roundup July 20 : https://devengoratela.com/2026/07/aws-weekly-roundup-one-click-lambda-setup-prompt-openai-gpt-5-6-models-on-bedrock-and-more-july-20-2026/
- Data Center Hardware July 2026 : https://www.datacenterknowledge.com/data-center-hardware/data-center-hardware-highlights-july-2026
- EU Technological Sovereignty Package (CSA) : https://labs.cloudsecurityalliance.org/research/eu-tech-sovereignty-cloud-ai-enterprise-risk-v1-0-csa-styled/
- Souveraineté numérique Europe (eclipso) : https://www.eclipso.de/blog/en/2026/07/13/digital-sovereignty-why-europe-must-now-regain-control-over-its-digital-future/
- Souveraineté Europe (eunews) : https://www.eunews.it/en/2026/07/20/digital-sovereignty-europe-necessity/
- Sovereign Cloud Europe (Luxsure) : https://www.luxsure.fr/en/2026/07/14/sovereign-cloud-can-europe-break-free-from-its-reliance-on-hyperscalers/
- EU Cloud Rules 2026 (Cyso) : https://cyso.cloud/blog/digital-sovereignty-eu-cloud-rules-2026
- VMware replacement 2026 (Sangfor) : https://www.sangfor.com/blog/cloud-and-infrastructure/vmware-replacement-guide-2026
- Broadcom licensing advisory : https://broadcomaudits.com/blog/top-broadcom-advisory-firms/
- VMware to cloud migration cost : https://migrationcost.com/vmware-to-cloud-migration-cost
- Cloud cost optimization guide 2026 : https://multicloudoptimization.com/cloud-cost-optimization-guide/
- Multi-cloud storage cost optimization 2026 : https://megastorage.cloud/multicloud-cost-optimization-storage-architects-2026


Mise à jour - 2026-07-31 (semaine du 27-31 juillet 2026)

Sécurité & CVE (virtualisation / cloud)
- 29 juillet 2026 : VMSA-2026-0006 (Broadcom) - trois vulnérabilités critiques VMware. CVE-2026-59309 : bypass d'authentification (CVSS 9.8, non authentifié, réseau) dans le VMware Directory Service de vCenter, donnant accès au plan de gestion ; CVE-2026-59310 : RCE (CVSS 9.8) ; CVE-2026-47876 : exécution de code guest-to-host via VMXNET3 (CVSS 9.3, potentiel VM escape). Pas de workaround documenté pour les deux premières. Le correctif passe par vSphere 8.0 Update 3k, qui bloque temporairement le chemin d'upgrade vers VCF 9.1. À patcher en priorité sur tout environnement VMware. Sources : Rapid7, CyberSignal, AngrySysOps, 29-30 juillet 2026.
- Contexte : des chaînes d'exploitation de trois vulnérabilités ESXi sont signalées actives en 2026 pour parvenir à un VM escape complet et compromettre l'hyperviseur. Source : vMoreCloud, 2026.

Proxmox VE
- RAS cette semaine : pas de nouvelle version (VE 9.2 avec Dynamic Load Balancer et PBS 4.2 restent les dernières, avril-mai 2026). Rester à jour sur le noyau patché (PinTheft/DirtyFrag).

Hyperscalers & Cloud IA
- Alphabet relève sa guidance capex 2026 à 195-205 Md$ (+15 Md$) ; la croissance cloud de Google Cloud s'accélère, mais les investisseurs sanctionnent les dépenses IA : Amazon, Meta et Microsoft chutent avant leurs résultats trimestriels. Source : CNBC, 28 juillet 2026.
- NVIDIA investit jusqu'à 2,1 Md$ dans IREN : partenariat stratégique pour déployer jusqu'à 5 GW d'infrastructure IA alignée sur l'architecture DSX (le campus Sweetwater 2 GW au Texas en site flagship). IREN acquiert par ailleurs Mirantis pour 625 M$ (pipeline porté à 5,8 GW). Sources : Datacenter Knowledge, Invezz, 28-29 juillet 2026.
- Lambda Labs lève 320 M$ pour étendre son cloud GPU dédié à l'IA. Source : TechHubBox, juillet 2026.

Cloud cost optimization & multicloud
- Pas de nouveauté majeure cette semaine ; les leviers 2026 restent le placement intelligent des données (compute locality, caches) et l'optimisation des coûts LLM (ex. billing attribution sur Amazon Bedrock).

Souveraineté des données & cloud européen
- 16 juillet 2026 : Airbus choisit Scaleway comme fournisseur de cloud souverain après un appel d'offres qui notait explicitement la protection contre les lois extraterritoriales non européennes. L'ensemble Airbus + Scaleway + Mistral forme la première chaîne de défense IA souveraine européenne de bout en bout. Sources : InfoQ, European Cloud, juillet 2026.

VMware / Broadcom
- Rappel du contexte licence 2026 : 100% abonnement, catalogue réduit à 4 bundles (VCF en tête), facturation par cœur avec minimum 16 cœurs/CPU, réseau de partenaires réduit de 4 000+ à ~300. Combiné au VMSA-2026-0006, la pression s'intensifie sur les clients VMware pour accélérer l'évaluation des alternatives (Proxmox, KVM, migration cloud). Sources : Redress Compliance, Schneider.im, 2026.

Outages
- Aucun outage majeur hyperscaler détecté cette semaine (27-31 juillet 2026) : status pages AWS, Azure et GCP nominaux au 30-31 juillet.

Sources :
- VMSA-2026-0006 (Rapid7) : https://www.rapid7.com/blog/post/etr-critical-vmware-vcenter-vulnerabilities-allow-authentication-bypass-and-remote-code-execution-cve-2026-59309-cve-2026-59310/
- Détail CVE vCenter (CyberSignal) : https://www.thecybersignal.com/vmware-vcenter-cve-2026-59309-59310-vm-escape-2026/
- vSphere 8.0 Update 3k (AngrySysOps) : https://angrysysops.com/2026/07/30/vsphere-8-0-update-3k-fixes-critical-cves-but-temporarily-blocks-the-vcf-9-1-upgrade-path/
- ESXi exploité en 2026 (vMoreCloud) : https://vmorecloud.com/vmware-esxi-vulnerability-actively-exploited-in-2026-patch-guidance-for-admins/
- Capex hyperscalers (CNBC) : https://www.cnbc.com/2026/07/28/hyperscalers-face-higher-capex-scrutiny-after-alphabet-report-panned.html
- NVIDIA x IREN (Datacenter Knowledge) : https://www.datacenterknowledge.com/deals/nvidia-places-massive-ai-infrastructure-bet-on-iren-s-5-gw-pipeline
- NVIDIA investit 2,1 Md$ dans IREN (Invezz) : https://www.tradingview.com/news/invezz:7ea93a735094b:0-nvidia-to-invest-up-to-2-1-billion-in-iren-ai-infrastructure-deal/
- IREN acquiert Mirantis (Intellectia) : https://intellectia.ai/news/monitor/iren-acquires-mirantis-for-625m-to-boost-ai-infrastructure
- Lambda Labs 320 M$ (TechHubBox) : https://www.techhubbox.com/lambda-raises-320-million-for-gpu-cloud-focused-on-ai/
- Airbus x Scaleway (InfoQ) : https://www.infoq.com/news/2026/07/airbus-scaleway-sovereign-cloud/
- Airbus x Scaleway (European Cloud) : https://european.cloud/2026/07/airbus-selects-scaleway/
- Broadcom VMware licensing 2026 (Redress) : https://redresscompliance.com/broadcom-vmware-licensing-changes-explained
- VMware licensing 2026 (Schneider.im) : https://www.schneider.im/vmware-by-broadcom-portfolio-simplification-and-transition-to-subscription/

Sources :
- Proxmox vs VMware 2026 : https://tech-insider.org/proxmox-vs-vmware-2026/
- CVE-2026-48567 (CrowdStrike Patch Tuesday juin 2026) : https://www.crowdstrike.com/en-us/blog/patch-tuesday-analysis-june-2026/
- CVE-2026-20253 (CISA KEV) : https://www.cisa.gov/known-exploited-vulnerabilities-catalog
- Pi-hole FTL v6.7 : https://discourse.pi-hole.net/t/pi-hole-ftl-v6-7-web-v6-6-and-core-v6-4-3-released/86679
- Proxmox Roadmap (PinTheft) : https://pve.proxmox.com/wiki/Roadmap
- Proxmox DirtyFrag PSA : https://forum.proxmox.com/threads/dirty-frag-universal-linux-lpe-proxmox-vulnerable-in-the-wild-already.183363/



Mise à jour - 2026-08-07 (semaine du 3-7 août 2026)

Sécurité et CVE (virtualisation / cloud)
- Pas de nouvelle CVE critique cloud/virtualisation publiée cette semaine. La chaîne VMSA-2026-0006 (CVE-2026-59309/59310/47876, vCenter/ESXi) reste le sujet n°1 : articles de rappel The Hacker News et SocRadar début août, confirmant la nécessité du correctif vSphere 8.0 Update 3k. À surveiller : le Patch Tuesday Microsoft du 11 août 2026, où Rapid7 attend la publication de la seconde faille d'une chaîne RCE (partiellement sous embargo depuis juillet). Sources : The Hacker News, SocRadar, Rapid7, août 2026.

Proxmox VE
- 5 août 2026 : support officiel arm64 de Proxmox VE (PVE 9.2) — première seconde architecture CPU supportée après x86-64. Même codebase, mêmes dépôts et même cycle de vie que la version x86-64 (QEMU 11.0, LXC 7.0, ZFS 2.4). Contraintes : hôtes UEFI+ACPI obligatoires, VMs en UEFI AAVMF ; SeaBIOS et une partie des features x86 non supportés. Le portage a été mené avec l'aide de NVIDIA et Supermicro ; Jeff Geerling l'a testé sur plateforme Ampere Altra. Sources : Proxmox, XDA, Jeff Geerling, 5-6 août 2026.
- Proxmox VE 8 : fin de vie au 31 août 2026 — plus aucun patch de sécurité après cette date ; fenêtre ouverte pour migrer vers PVE 9.2 (checklist de mise à niveau disponible). Sources : Everywan, Falcon Internet, juillet-août 2026.
- (Rattrapage) 28 juillet 2026 : Proxmox rejoint l'écosystème NVIDIA Mission Control comme couche de gestion HA pour les AI factories. Source : StorageReview, 28 juillet 2026.

Hyperscalers et Cloud IA
- Résultats T2 2026 : AWS +37 % à 42 Md$ (plus forte croissance en 18 trimestres) ; Amazon franchit pour la première fois 3 000 Md$ de capitalisation (4 août) ; Google Cloud +82 % ; Microsoft relève son capex 2026 à ~220 Md$ (53,1 Md$ de cash capex au T2). Le backlog cloud cumulé des Big Tech atteint ~2 300 Md$ ; le capex hyperscalers 2026 est estimé à plus de 860 Md$ (+80 % sur un an), vers ~1 200 Md$ en 2027 (BofA). Sources : Yahoo Finance, Seeking Alpha, AIM, 247wallst, 28 juillet-4 août 2026.
- Dépenses cloud d'infrastructure : 143 Md$ au T2 2026, +43 % sur un an — plus haut depuis 8 ans (Synergy Research). Sources : The Register, 1er août 2026 / IT Pro, 3 août 2026.
- 4 août 2026 : Volta Infra, nouveau cloud IA, lève 300 M$ à 2,4 Md$ de valorisation (+5 Md$ de financement), tour co-mené par a16z et Altimeter avec participation de NVIDIA et Michael Dell. Sources : Bloomberg, The Next Web, 4 août 2026.
- 4 août 2026 : Runware lance le Sonic Inference Pod — datacenter modulaire portable en un seul conteneur, positionné comme alternative flexible aux campus massifs des hyperscalers. Source : TechCrunch, 4 août 2026.
- 6 août 2026 : un fonds émirati étudie ~6,3 Md$ (1 000 Md¥) pour un datacenter IA au Japon. Source : Bloomberg, 6 août 2026.

Cloud cost optimization et multicloud
- RAS de nouveauté majeure cette semaine. Contexte : la croissance des dépenses (+43 % YoY) et le capex 2026 supérieur à 860 Md$ renforcent la pression FinOps ; le "cloud backlog" de 2 300 Md$ des hyperscalers confirme un marché toujours vendeur côté capacité IA.

Souveraineté des données et cloud européen
- RAS de nouveauté majeure côté Europe cette semaine. Rappel de contexte : Gartner prévoit 80 Md$ de dépenses sovereign cloud IaaS en 2026, avec l'Europe parmi les régions les plus dynamiques (+83 %).

VMware / Broadcom
- Nouveau durcissement licenciel rapporté : le minimum de cœurs facturés par commande passe de 16 à 72 cœurs (en plus du plancher existant de 16 cœurs/CPU), annoncé via le distributeur Arrow et effectif au 10 avril. Conséquence : un serveur 1 processeur / 8 cœurs se facture désormais 72 cœurs. Le sujet enflamme les discussions (Medium, LinkedIn) sur l'impact PME et accélère encore l'évaluation des alternatives (Proxmox, KVM, migration cloud). Sources : IT-Daily, Qual, Medium, août 2026.

Outages
- Aucun outage majeur hyperscaler détecté cette semaine (3-7 août 2026) : status pages AWS, Azure et GCP nominaux au 6-7 août.

Sources :
- Proxmox VE arm64 (annonce officielle) : https://www.proxmox.com/en/about/company-details/press-releases/proxmox-virtual-environment-launches-official-arm64-support
- Proxmox VE arm64 (forum) : https://forum.proxmox.com/threads/proxmox-virtual-environment-now-available-for-64-bit-arm-arm64.185527/
- Proxmox arm64 caveats (XDA) : https://www.xda-developers.com/proxmox-releases-full-support-for-the-arm64-architecture-with-a-few-key-caveats/
- Proxmox arm64 test Ampere Altra (Jeff Geerling) : https://www.jeffgeerling.com/blog/2026/proxmox-ve-arm-official/
- PVE 8 EOL (Everywan) : https://everywan.com/en/blog/proxmox-ve-8-end-of-life-august-2026
- PVE 8 EOL upgrade checklist (Falcon) : https://www.falconinternet.net/blog/proxmox-ve-8-end-of-life-august-2026-upgrade
- Proxmox x NVIDIA Mission Control (StorageReview) : https://www.storagereview.com/news/proxmox-ve-joins-nvidias-mission-control-ecosystem-as-the-ha-layer-for-ai-factories
- VMSA-2026-0006 recap (The Hacker News) : https://thehackernews.com/2026/07/three-critical-vmware-flaws-allow-auth.html
- VMSA-2026-0006 recap (SocRadar) : https://socradar.io/blog/critical-vmware-vcenter-esx-flaws/
- Patch Tuesday août 2026 à surveiller (Rapid7) : https://www.rapid7.com/blog/post/em-patch-tuesday-july-2026/
- Backlog cloud 2 300 Md$ (Yahoo Finance) : https://finance.yahoo.com/technology/article/big-techs-cloud-backlog-just-hit-23-trillion--and-its-feeding-ai-capex-plans-181459457.html
- Hyperscalers post-earnings (Seeking Alpha) : https://seekingalpha.com/article/4929289-4-hyperscalers-one-message-the-ai-trade-isnt-over
- Amazon 3 000 Md$ / AWS +37 % (247wallst) : https://247wallst.com/investing/2026/08/04/bezos-sells-4-billion-in-amazon-stock-as-it-hits-3-trillion-for-first-time-cramer-calls-it-a-buzzkill/
- Capex Microsoft 220 Md$ (AIM) : https://analyticsindiamag.com/global-tech/big-techs-multi-billion-ai-infrastructure-bet-has-an-achilles-heel
- Dépenses cloud +43 % au T2 (The Register) : https://www.theregister.com/off-prem/2026/08/01/enterprise-cloud-infrastructure-uptake-shows-no-sign-of-slowing/5281835
- Dépenses cloud plus haut depuis 8 ans (IT Pro) : https://www.itpro.com/cloud/cloud-computing/cloud-infrastructure-spending-just-hit-an-eight-year-high
- Volta Infra 300 M$ (Bloomberg) : https://www.bloomberg.com/news/articles/2026-08-04/nvidia-dell-back-ai-cloud-startup-volta-at-2-4-billion-value
- Volta Infra (The Next Web) : https://thenextweb.com/news/volta-ai-cloud-300m-nvidia-dell-2-4bn
- Runware Sonic Inference Pod (TechCrunch) : https://techcrunch.com/2026/08/04/is-the-future-of-data-centers-portable-runware-builds-a-pod-to-find-out/
- UAE / Japon 6,3 Md$ (Bloomberg) : https://www.bloomberg.com/news/articles/2026-08-06/uae-fund-weighs-6-3-billion-ai-data-center-investment-in-japan
- Sovereign cloud 80 Md$ 2026 (Gartner) : https://www.gartner.com/en/newsroom/press-releases/2026-02-09-gartner-says-worldwide-sovereign-cloud-iaas-spending-will-total-us-dollars-80-billion-in-2026
- VMware minimum 72 cœurs (IT-Daily) : https://www.it-daily.net/shortnews-en/vmware-licensing-broadcom-raises-core-minimum-to-72-cores
- VMware minimum 72 cœurs (Qual) : https://www.qual.co.uk/vmware-minimum-licensing-72-core/
- VMware 72 cœurs, l'impact PME (Medium) : https://medium.com/weeklycloud/vmwares-new-72-core-minimum-licensing-is-a-mess-here-s-why-it-s-frustrating-everyone-1b8c177d6d7c


Mise à jour - 2026-08-14 (semaine du 10-14 août 2026)

Sécurité et CVE (virtualisation / cloud)
- EXPLOITATION ACTIVE de la chaîne VMware VMSA-2026-0006 (11 août 2026) : The Hacker News rapporte des attaques exploitant CVE-2026-59310 (directory traversal dans vCenter, CVSS 9.8) pour obtenir un accès persistant sur les systèmes ; en parallèle, Defused Cyber (via X) observe un pic de scans contre CVE-2026-59309 (auth bypass du VMware Directory Service/vmdir, CVSS 9.8), typique de tentatives d'exploitation massives. Les correctifs (vSphere 8.0 Update 3k, fin juillet 2026) sont disponibles — patching URGENT pour tout vCenter exposé. Sources : The Hacker News, Cybersecurity News, 11 août 2026.
- Patch Tuesday Microsoft du 11 août 2026 : ~400 vulnérabilités corrigées (394 à 421 selon les décomptes), dont 42 critiques (37 RCE) et 3 zero-days (1 exploitée, 2 divulguées publiquement). Zero-day actif : CVE-2026-68820 — use-after-free dans le driver WinSock afd.sys, élévation de privilèges locale vers SYSTEM, exploitée par le groupe Lazarus (Operation Dream Job, ciblage d'entreprises de défense) avec déploiement du rootkit kernel FudModule (déjà utilisé via CVE-2024-38193). À corriger en priorité sur tous les postes Windows. Autres points notables : EoP SharePoint CVE-2026-62827 et CVE-2026-64921 (CVSS 8.8). C'est la suite attendue du Patch Tuesday de juillet (Rapid7 signalait une faille RCE sous embargo). Sources : BleepingComputer, SecurityWeek, The Hacker News, Talos, 11-12 août 2026.

Proxmox VE
- RAS de nouveauté cette semaine. Rappel : PVE 8 en fin de vie au 31 août 2026 (fenêtre de migration vers 9.2) ; support arm64 officiel depuis le 5 août 2026.

Hyperscalers et Cloud IA
- 10 août 2026 : Mark Zuckerberg annonce ~1 Md$ d'investissement dans les communautés locales où Meta construit ses AI data centers (programme communautaire pour accompagner les implantations). Source : Mazech, 10 août 2026.
- 11 août 2026 : AdaniConneX alloue jusqu'à 30 000 crores (~3,6 Md$) pour le premier lot du hub AI data center de 1 GW de Google à Visakhapatnam (Inde). Source : Channeliam, 11 août 2026.
- Analyses post-résultats (11-12 août) : Google Cloud affiche +82 % YoY, porté par ses puces IA custom (coûts de calcul inférieurs au GPU), tandis qu'Azure "peine à suivre" ; les hyperscalers reculent (~-2 % MSFT/AMZN/META le 12 août) dans un débat marché neoclouds vs hyperscalers. Sources : iBusiness, TMT Breakout, 11-12 août 2026.
- NVIDIA confirme que la plateforme Vera Rubin NVL72 est en production et monte en charge chez CoreWeave, Google Cloud, Microsoft Azure et OCI (H2 2026). Source : NVIDIA Blog, 12 août 2026.
- (Rattrapage) 6 août 2026 : OpenAI discuterait de la location d'un datacenter de 10 GW dans l'Ohio (projet Matador), avec un possible soutien financier de NVIDIA. Source : TechStock², 6 août 2026.

Cloud cost optimization et multicloud
- RAS de nouveauté majeure. Contexte : les synthèses de tendances cloud d'août 2026 (Kloudping, 10 août) confirment la pression FinOps — capex hyperscalers 725-770 Md$ en 2026, contrats multicloud, edge Kubernetes et sécurité cloud en tête des priorités.

Souveraineté des données et cloud européen
- RAS de nouveauté majeure cette semaine. Contexte : contrat-cadre souverain de 180 M€ de la Commission européenne attribué en avril 2026 à 4 consortiums (dont Proximus/Google Cloud) ; AWS European Sovereign Cloud opérationnel depuis janvier 2026.

VMware / Broadcom
- Analyse détaillée des coûts réels de migration hors VMware post-Broadcom : transformation multi-années (licences, outils, formation, re-architecture) avec coûts et risques chiffrés — alimente l'évaluation des alternatives (Proxmox, KVM, cloud). Source : iTechGuides, 10 août 2026.
- Redress Compliance publie un advisory Broadcom à jour le 9 août 2026 sur la négociation des contrats VMware post-acquisition (levier = nombre de cœurs facturés et crédibilité du plan de sortie). Source : Redress, 9 août 2026.

Outages
- Aucun outage majeur hyperscaler détecté cette semaine (10-14 août 2026) : status pages AWS, Azure et GCP nominaux. Dernier incident notable : AWS CloudFront (16 juillet 2026), déjà traité.

Sources :
- Exploitation CVE-2026-59310 (The Hacker News) : https://thehackernews.com/2026/08/attackers-exploit-vmware-vcenter.html
- Scans CVE-2026-59309 (Cybersecurity News) : https://cybersecuritynews.com/hackers-scan-vmware-vcenter-vulnerabilities/
- Patch Tuesday août 2026 (BleepingComputer) : https://www.bleepingcomputer.com/news/microsoft/microsoft-august-2026-patch-tuesday-fixes-400-flaws-3-zero-days/
- Patch Tuesday août 2026 (SecurityWeek) : https://www.securityweek.com/august-2026-patch-tuesday-microsoft-fixes-421-cves-one-exploited-zero-day/
- CVE-2026-68820 / Lazarus (The Hacker News) : https://thehackernews.com/2026/08/lazarus-exploits-windows-zero-day-to.html
- CVE-2026-68820 / FudModule (Cybersecurity News) : https://cybersecuritynews.com/windows-afd-sys-zero-day-exploited/
- CVE-2026-68820 détails (SOC Prime) : https://socprime.com/blog/cve-2026-68820-actively-exploited-windows/
- Patch Tuesday / SharePoint (Talos) : https://blog.talosintelligence.com/microsoft-patch-tuesday-for-august-2026/
- Zuckerberg 1 Md$ communautés (Mazech) : https://mazech.com/2026/08/mark-zuckerberg-is-trying-to-solve-his-ai-data-center-problem-with-a-1-billion-giveaway/
- AdaniConneX / Google Visakhapatnam (Channeliam) : https://channeliam.com/2026/08/11/adani-google-ai-data-center-visakhapatnam/
- Google Cloud +82 % / Azure (iBusiness) : https://ibusiness.news/news/2026-08-11/google-cloud-and-aws-amzn-googl-msft-surge-while-microsoft-azure-struggles-to-keep-pace/
- Neoclouds vs hyperscalers (TMT Breakout) : https://www.tmtbreakout.com/p/eod-wrap-cisco-csco-coherent-cohr
- Vera Rubin NVL72 en production (NVIDIA Blog) : https://blogs.nvidia.com/blog/category/enterprise/
- OpenAI 10 GW Ohio (TechStock²) : https://ts2.tech/en/fermi-frmi-jumps-after-openai-data-center-report-project-matador-lease-bets-return/
- Tendances cloud août 2026 (Kloudping) : https://kloudping.com/cloud-computing-trends-august-2026/
- Coûts de migration VMware (iTechGuides) : https://www.itechguides.com/a-long-costly-road-ahead-for-customers-abandoning-broadcoms-vmware/
- Advisory Broadcom (Redress) : https://redresscompliance.com/vmware-contracts-post-broadcom-acquisition


Mise à jour - 2026-08-21 (semaine du 17-21 août 2026)

Sécurité et CVE (virtualisation / cloud)
- CVE-2026-48806 : bypass du sandbox Twig (moteur de templates PHP) via les clés de mapping dynamiques, permettant des appels non autorisés à __toString() (versions <= 3.26.0 ; correctif en 3.27.0). C'est un bypass résiduel du correctif de CVE-2026-47732 (GHSA-pr2w-4gpj-cpq4). Pertinent pour toute stack web PHP (panneaux d'admin, outils type panel de virtualisation). Source : GitHub Advisory GHSA-5v5v-ww74-355v, BitNinja, 17-19 août 2026.
- (Contexte) StackWarp : faille matérielle AMD (Zen 1 à Zen 5, dont EPYC) affectant la confidentialité des VMs SEV-SNP — rappel que la sécurité cloud dépend aussi de la chaîne matérielle. Disclose janvier 2026, toujours citée dans les analyses cloud d'août 2026. Source : Aviatrix Threat Research Center.

Proxmox VE
- RAS de nouveauté majeure cette semaine. Rappel : PVE 8 en fin de vie au 31 août 2026 (plus de patchs de sécurité après cette date) — checklists de migration vers PVE 9.2 publiées début août (Falcon Internet). Écosystème communautaire actif (ex. PVE 9 sur Raspberry Pi 5).

Hyperscalers et Cloud IA
- 18-19 août 2026 : Pure Storage bondit de +22 % après l'annonce d'un contrat "top-four AI hyperscaler" pour ses baies flash ; Everpure (DirectFlash) décroche son 2e contrat avec un hyperscaler du top 5 (19 août). Le stockage flash haute densité devient un axe de différenciation des datacenters IA. Sources : The Outpost AI, DataCenterDynamics.
- 18 août 2026 : NVIDIA investit 1,5 Md$ dans SB Energy (SoftBank) pour sécuriser l'alimentation électrique de ses infrastructures GPU. Source : The GPU Daily.
- 18 août 2026 : AMD présente Helios, système IA rack-scale intégré (EPYC 9006 6e gén. + GPU Instinct MI455X + réseau Pensando + ROCm), rival direct de la plateforme NVIDIA Vera Rubin/NVL72. Source : Data Center Knowledge, 18 août 2026.
- (Analyse) Jefferies : ~85 % des revenus cloud des hyperscalers US restent non-IA — l'IA ne représente que ~15 % du chiffre d'affaires cloud ; rappel de prudence sur le narratif "tout-IA". Source : BusinessToday, 14 août 2026.

Cloud cost optimization et multicloud
- L'inflation des prix cloud ralentit, mais la consommation (notamment workloads IA) continue de tirer les dépenses vers le haut — la pression FinOps reste forte sur le multicloud. Source : CIO Dive (analyse Tangoe), 17-18 août 2026.

Souveraineté des données et cloud européen
- Les règles de souveraineté des données fragmentées (par pays/opérateur) compliquent les décisions d'architecture cloud et les recrutements — la souveraineté devient une variable stratégique pour les opérateurs télécoms. Source : Hosting Journalist / LinkedIn, mi-août 2026.
- (À venir) OpenNebula organise OneNext 2026 "Europe Sovereignty Event" le 8 octobre 2026 à Madrid : souveraineté au-delà des données (contrôle de la techno, des opérations et de l'infrastructure), architectures ouvertes pour cloud et IA. Source : opennebula.io.

VMware / Broadcom
- 17 août 2026 : Broadcom détaille le programme de VMware Explore 2026 (Las Vegas, 31 août - 3 septembre) — sessions techniques, labs, certifications, axe "Private AI Cloud" ; Explore on Tour dans plusieurs villes à l'automne. Source : GlobeNewswire / Broadcom.
- (Contexte) Le marché continue de décortiquer la négociation des contrats VMware post-Broadcom (tarification basée sur le coût de départ du client plutôt que sur la facture précédente). Source : Redress Compliance, août 2026.

Outages
- Cloudflare : série d'incidents marquants mi-août 2026 — 13 pannes en 8 jours, dont une dégradation R2 (buckets ENAM) et une chute de disponibilité Durable Objects/Workflows (14 août) ; questions sur d'éventuelles pertes de données R2. Série à surveiller (CDN/DNS/edge critiques pour tout le web). Source : shattered.io, août 2026.
- Namecheap : 28 h d'interruption (12-13 août) après un orage à Phoenix ayant coupé le refroidissement de son datacenter RadiusDC — rappel de la fragilité des couches physiques. Source : Topsite Hosters, août 2026.
- 18 août 2026 : panne mondiale des services Google Nest/Home côté cloud. Pas d'outage majeur AWS/Azure/GCP cette semaine (status pages nominaux).

Sources :
- CVE-2026-48806 Twig (GitHub Advisory) : https://github.com/advisories/GHSA-5v5v-ww74-355v
- CVE-2026-48806 (BitNinja) : https://bitninja.com/blog/cve-2026-48806-critical-twig-vulnerability-alert/
- StackWarp AMD SEV-SNP (Aviatrix) : https://aviatrix.ai/threat-research-center/amd-stackwarp-hardware-flaw-2026-cloud-virtualization-exposure/
- PVE 8 EOL / migration (Falcon Internet) : https://www.falconinternet.net/blog/proxmox-ve-8-end-of-life-august-2026-upgrade
- Pure Storage hyperscaler deal (The Outpost AI) : https://theoutpost.ai/news-story/pure-storage-soars-on-landmark-ai-hyperscaler-deal-signaling-shift-in-data-storage-landscape-9119/
- Everpure 2e contrat hyperscaler (DataCenterDynamics) : https://www.datacenterdynamics.com/en/news/everpure-secures-contract-from-top-five-hyperscaler-for-its-flash-storage-offering/
- NVIDIA / SB Energy 1,5 Md$ (The GPU Daily) : https://thegpu.ai/p/gpu-daily-2026-08-18
- AMD Helios (Data Center Knowledge) : https://www.datacenterknowledge.com/data-center-hardware/data-center-hardware-highlights-august-2026
- 85 % revenus hyperscalers non-IA (BusinessToday) : https://www.businesstoday.in/technology/story/the-ai-reality-check-85-of-hyperscalers-cloud-revenue-is-still-non-ai-549289-2026-08-14
- Inflation cloud / coûts IA (CIO Dive) : https://www.ciodive.com/news/hyperscaler-inflation-slows-cloud-consumption-grows-tangoe/740270/
- Souveraineté fragmentée (Hosting Journalist) : https://www.linkedin.com/posts/hostingjournalist-com_fragmented-data-sovereignty-rules-raise-compliance-activity-7450252028632764416-V0Pe
- OneNext 2026 Madrid (OpenNebula) : https://opennebula.io/techdays/europe-sovereignty-event/
- VMware Explore 2026 (GlobeNewswire) : https://www.globenewswire.com/news-release/2026/08/17/3346137/19933/en/vmware-explore-2026-brings-technical-sessions-labs-and-certs-to-it-practitioners-arming-them-for-the-private-ai-cloud-era.html
- Négociation contrats VMware (Redress) : https://redresscompliance.com/vcf-negotiation-escalation-ladder-timing
- Cloudflare 13 pannes / R2 (shattered.io) : https://shattered.io/cloudflare-outage-august-2026/
- Namecheap outage Phoenix (Topsite Hosters) : https://topsitehosters.com/blog/namecheap-outage-august-2026-what-happened/
- Google Nest/Home outage (SeminarsOnly) : https://seminarsonly.com/news/is-google-home-down-outage-status/

Mise à jour - 2026-09-04 (semaine du 31 août - 4 septembre 2026)

Sécurité et CVE (virtualisation / cloud)
- VMware vCenter CVE-2026-59309 et CVE-2026-59310 (CVSS 9.8) toujours activement exploitées : Rapid7 et SecurityWeek confirment que CVE-2026-59310 (directory traversal dans le Syslog server vCenter) est dans le collimateur des attaquants, avec exploitation par un APT lié à la Chine déployant un ransomware dérivé de Babuk dans les 72h suivant la divulgation du patch (Vici Security, août 2026). Le patch de fin juillet (vSphere 8.0 Update 3k) reste URGENT pour tout vCenter exposé.
- VMM Escape Vulnerability (Glasswing) : bypass d'isolation de l'hyperviseur, classe de vulnérabilité la plus sévère en environnement virtualisé cloud/entreprise car elle invalide tous les contrôles de sécurité au-dessus de la couche hyperviseur (Decryption Digest, juillet 2026).
- SAP Commerce Cloud CVE-2026-58231 exploitée dans les 72h suivant la divulgation du correctif.

Proxmox VE
- ANNONCE MAJEURE (2 septembre 2026) : Proxmox Server Solutions GmbH étend son support entreprise au 24/7 (effectif au 19 octobre 2026) ET lance Proxmox North America Inc. (Kingston, Ontario, Canada) — nouvelle filiale dédiée aux ventes, account management et support technique pour les fuseaux horaires Amériques. Trois niveaux de support : Community (gratuit), Standard (8/5, 500 EUR/CPU/an) et Premium (24/7, 2h de réponse, 1100 EUR/CPU/an). Cela supprime un des freins historiques à l'adoption de Proxmox en entreprise : l'absence de support 24/7 officiel. Source : Proxmox Press Release, 2 sept. 2026 ; Virtualization Howto, 3 sept. 2026.
- (Rappel) Proxmox VE for ARM64 disponible depuis le 5 août 2026 ; PVE 9.2 avec Dynamic Load Balancer depuis mai 2026 ; PVE 8 en fin de vie au 31 août 2026 (fenêtre de migration maintenant fermée).

Hyperscalers et Cloud IA
- 2 septembre 2026 : Le CEO de NVIDIA, Jensen Huang, presse les ministres du G20 de traiter la capacité de calcul IA et les datacenters comme des infrastructures nationales critiques. Il souligne l'engagement de NVIDIA de 500 Md$ dans la production technologique domestique. Source : TechXplore, 2 sept. 2026.
- 3 septembre 2026 : Jensen Huang confirme que Hugging Face restera une plateforme ouverte pour tout l'écosystème IA. Source : Gizmodo, 3 sept. 2026.
- Les hyperscalers (Alphabet, Amazon, Meta, Microsoft, Oracle) sont sur une trajectoire de capex combiné de 775-800 Md$ en 2026 (+64 % sur 2025). Le rapport Q2 d'Alphabet (hausse de la prévision capex) a fait chuter les actions des autres hyperscalers fin juillet. Source : CNBC, 28 juillet 2026.
- Jefferies (août 2026) : ~85 % des revenus cloud des hyperscalers US restent non-IA — l'IA ne représente que ~15 % du chiffre d'affaires cloud.

Cloud cost optimization et multicloud
- Cloud Security Alliance publie une synthèse des meilleures techniques d'optimisation des coûts cloud en 2026 : combinaison de pratiques FinOps continues, d'insights AI-driven et de smart resource management. Points clés : rightsizing des instances, optimisation des tiers de stockage, automatisation des workflows. Source : CSA, 12 juin 2026.
- Les guides 2026 (CloudZero, OpsioCloud, Growin) confirment la tendance : la maturité multi-cloud exige désormais discipline architecturale et précision financière, notamment pour les workloads GPU intensifs.

Souveraineté des données et cloud européen
- La Commission européenne publie (1er juin 2026) un "Sovereign Cloud Framework" détaillé — outil d'évaluation des prestataires de cloud souverain pour les marchés publics, en réponse à l'intérêt massif des administrations et entreprises IT. Le cadre s'inscrit dans l'EU Cloud and AI Development Act (CADA) présenté au Q1 2026. Source : European Commission, 1er juin 2026.
- Analyse LinkedIn (Claraz) : la souveraineté cloud européenne en 2026 oscille entre aspiration et réalité — les couches légales, techniques et opérationnelles progressent mais restent fragmentées entre États membres.

VMware / Broadcom
- VMware Explore 2026 (Las Vegas, 31 août - 3 septembre 2026) : 400+ sessions techniques, hands-on labs, certifications, centré sur VMware Cloud Foundation (VCF) comme socle du "Private AI Cloud".
- ANNONCES MAJEURES de VMware Explore :
  1. VMware Private AI Cloud — nouvelle offre permettant aux entreprises de scaler l'IA de manière cost-effective avec sécurité renforcée et gouvernance on-premise. Le cloud privé devient "operating layer" pour l'IA d'entreprise.
  2. VMware AI Factory — infrastructure automation incluant des VCF AI ReadyNodes certifiés par Dell, Cisco, Lenovo, Supermicro ; permet un contrôle total sur l'AI tokenomics (coûts d'inférence).
  3. VCF 9.1.1 — nouvelles capacités AI et Kubernetes, assistant conversationnel IA pour workflows quotidiens, durcissement de la sécurité.
  4. vSphere 9.1 certifié NVIDIA-Certified Hypervisor — les workloads AI/HPC sur VCF sont certifiés pour fonctionner à performance quasi-native (bare metal).
- Sources : VMware Blogs, 3 sept. 2026 ; NextPlatform, 1er sept. 2026 ; StorageNewsletter, 2 sept. 2026 ; The Cube Research, 3 sept. 2026.
- (Contexte) Licences perpétuelles VMware supprimées, remplacées par bundles d'abonnement VCF avec licensing par cœur physique (min. 16 cœurs/socket). Pénalité de 20 % pour renouvellement tardif. Source : Redress Compliance, 2026.

Outages
- 1er septembre 2026 : Panne GCP us-central1-b — 15 services Google Cloud impactés pendant 4h08m (dégradation réseau, perte de paquets). Touché : Compute Engine, GKE, BigQuery, Cloud Storage, Cloud SQL. Cause : incident réseau dans la zone us-central1-b. Source : shattered.io, Google Cloud Status Dashboard.
- (Rappel) Cloudflare : série de 13 pannes en 8 jours mi-août 2026 (R2, Durable Objects/Workflows).


Compléments - Veille approfondie du 04/09/2026 (sujets supplémentaires)

Investissements Datacenters & Hyperscalers (été 2026)
- Google augmente sa prévision de capex 2026 à 195-205 Md$ (+15 Md$ supplémentaires), confirmant une accélération sans précédent des investissements IA/Cloud. Le pipeline des datacenters n'a jamais été aussi fort : commandes records, campus multi-gigawatts annoncés partout dans le monde. Source : Data Centre News (Substack), 24 juillet 2026.
- OpenAI annonce un datacenter de 20 Md$ en Géorgie (Effingham County). Source : Data Centre News, 24 juillet 2026.
- MGX (Émirats) injecte 5 Md$ dans un développeur américain de datacenters. Source : Data Centre News, 24 juillet 2026.
- Pure DC lève 1,3 Md€ supplémentaires pour son campus AI européen. Source : Data Centre News, 24 juillet 2026.
- Microsoft va financer l'expansion européenne de Mistral AI via un deal multi-milliards. Source : Data Centre News, 24 juillet 2026.
- Fluidstack (cloud IA) lève 830 M$ en Série A. Source : Data Centre News, 24 juillet 2026.
- Meta/Anthropic en discussions pour un deal datacenter allant jusqu'à 10 Md$. Source : Data Centre News, 24 juillet 2026.
- IREN signe 2,8 Md$ de contrats avec des développeurs AI majeurs, relève son objectif ARR 2026 à +4 Md$. Source : Data Centre News, 24 juillet 2026.

IA Hardware - Course aux puces (juillet-août 2026)
- NVIDIA Blackwell Ultra confirmé : double la capacité mémoire HBM3e du B100 standard, crucial pour les context windows des modèles frontier. Nouveaux détails sur l'architecture Rubin (prévue 2027) avec interconnect fabric améliorant le scaling multi-GPU. Source : Skycrumbs, 28 juillet 2026.
- AMD Instinct MI400 : production limitée démarrée, performances compétitives avec Blackwell sur inference/fine-tuning à des prix attractifs pour les hyperscalers cherchant à diversifier leur supply chain. ROCm progresse mais reste en retard sur CUDA. Source : Skycrumbs, 28 juillet 2026.
- Google TPU v6 (Trillium) : désormais plus largement disponible via Google Cloud. Source : Skycrumbs, 28 juillet 2026.
- AWS Trainium 3 : disponibilité limitée en juillet pour clients sélectionnés. Amélioration significative du software tooling, prix attractif pour les startups AI. Source : Skycrumbs, 28 juillet 2026.
- Course à l'inference : Groq, Cerebras et SambaNova gagnent du terrain avec des puces spécialisées inference (latence <100ms). Le shift de l'entraînement vers l'inférence est la tendance clé de mi-2026. Source : Skycrumbs, 28 juillet 2026.
- Contrainte GPU 2024-2025 s'atténue : les délais H100/B100 se réduisent, le marché spot se normalise, mais la demande hyperscaler reste élevée. Source : Skycrumbs, 28 juillet 2026.

CVE et Sécurité (compléments)
- Le hub CyberUpdates365 recense les CVE critiques 2026 : VMware ESXi sandbox escape, Adobe ColdFusion CVE-2026-48282 (RCE actif), SharePoint CVE-2026-45659 (RCE non authentifié), LiteLLM Critical RCE (AI infrastructure), BeyondTrust CVE-2026-40138 (auth bypass IAM), Cisco ASA Zero-Day RCE (nation-state actors), Splunk CVE-2026-20253. Source : CyberUpdates365, 15 juillet 2026 (mis à jour 29 juillet).
- Proxmox PSA-2026-00014-1 : correctif de sécurité pour les API endpoints VNC — permettait à des attaquants privilégiés de détourner les sessions VNC et deviner le mot de passe VNC. Source : Proxmox Roadmap, juillet 2026.

Souveraineté des données et cloud européen (compléments)
- Mistral AI : poussée souveraine française avec 1,4 Md$ dédiés aux datacenters européens, en ligne avec la vision Macron. Prévisions : 1 Md€ de revenus en 2026, nouvelles acquisitions. Source : GlobalCodeMaster, juillet 2026.
- Startups canadiennes migrent vers des fournisseurs cloud européens (LifeinCloud) pour naviguer les lois strictes sur la souveraineté des données et les risques géopolitiques. Source : Noah News, 2026.
- Analyse Curious Minds : la souveraineté est une question de juridiction légale, pas de localisation des serveurs — implications majeures pour les stratégies cloud européennes. Source : Curious Minds, 2026.

Cloud Cost Optimization
- HCL Software : comment les plateformes FinOps pilotées par l'IA transforment la gestion des coûts cloud en 2026 — rightsizing multicloud automatisé (AWS, Azure, GCP). Source : HCL Software Blog, 2026.
- ServiceNow Cloud+ (CCM) : positionné comme leader FinOps pour 2026, avec contrôles budgétaires proactifs SaaS et AI. Source : ServiceNow Community, 2026.

Outages Cloud (compléments - août 2026)
- Août 2026 : 55% d'uptime seulement sur les services trackés. 4 jours sans aucune panne majeure. Grosse panne Microsoft 365 fin août. Source : isinternetup.com, août 2026.
- Axis Intelligence : 9 outages AWS, Azure, GCP, Cloudflare et DENIC recensés en août 2026 avec Diagnostic Lag Ratio pour chaque. Source : Axis Intelligence, 9 août 2026.

Licences VMware/Broadcom (précisions)
- Le modèle de licensing VMware/Broadcom s'est stabilisé en 2025 sans nouveau changement annoncé pour 2026. Les licences perpétuelles définitivement remplacées par abonnements VCF par cœur physique (min. 16 cœurs/socket). Pénalité de 20% pour renouvellement tardif introduite. Le mode déconnecté (air-gapped) reste supporté : pas de vérification d'activation cloud requise tant que l'abonnement est valide, mais VCF 9.0 introduit un mode connecté optionnel pour faciliter le reporting d'usage. Source : Redress Compliance, 2026 ; Schneider.im, 15 juin 2026 ; Acronis, 26 mars 2026 ; Stormagic, 19 mai 2026.

Mise à jour - 2026-09-18

Périmètre : actualités publiées ou signalées entre le 11 et le 18 septembre 2026.

## Hyperscalers et infrastructure cloud
- **AWS — extension d’Amazon Elastic VMware Service (EVS)** : AWS annonce la disponibilité d’Amazon EVS dans des régions supplémentaires. Cette extension facilite les stratégies de migration VMware vers AWS, mais ne supprime pas les enjeux de coûts de licence, de capacité et de dépendance à l’écosystème Broadcom.
- **AWS — capacité GPU** : les instances EC2 P6-B200 sont annoncées dans la région Asie-Pacifique (Hyderabad), ce qui augmente l’accès régional aux GPU NVIDIA Blackwell pour les charges d’entraînement et d’inférence. La tendance confirme la course à la capacité IA plutôt qu’une simple course aux fonctionnalités cloud.

## IA, GPU et data centers
- **Cerebras** prévoit six data centers d’inférence IA en Amérique du Nord et en Europe, équipés de milliers de systèmes CS-3. Le positionnement met l’accent sur le débit d’inférence et montre que l’offre cloud IA se diversifie au-delà des instances GPU généralistes.
- **Civo et Era4** annoncent une offre de cloud IA souverain au Royaume-Uni, combinant l’infrastructure de data centers d’Era4 et la plateforme CivoStack. Pour les organisations européennes, la souveraineté devient un critère d’architecture et de localisation, pas uniquement une clause contractuelle.

## Sécurité, CVE et virtualisation
- **Microsoft Patch Tuesday de septembre** : Microsoft a corrigé 974 vulnérabilités, un volume record selon The Register. Même si toutes ne concernent pas directement le cloud, la pression de patching sur les environnements Windows, hyperviseurs et plans de management reste élevée.
- **CVE-2026-85046 (Chrome)** : Google a indiqué qu’un exploit était présent dans la nature lors de la correction du 3 septembre. Les postes d’administration et bastions utilisés pour piloter les environnements cloud doivent être traités comme des composants critiques.
- Aucun nouvel avis critique VMware/Proxmox clairement confirmé et publié pendant la fenêtre du 11–18 septembre n’a été retenu ; les résultats trouvés renvoient principalement aux annonces et correctifs d’août ou du début septembre.

## Résilience et coûts
- Aucun incident AWS/Azure/GCP majeur, précisément daté dans la fenêtre du 11–18 septembre, n’a été confirmé par les résultats consultés. Les tableaux de statut des fournisseurs restent la référence opérationnelle ; il faut éviter de déduire une panne à partir de signalements agrégés sans post-mortem.
- **Point FinOps** : l’extension régionale des GPU et des services VMware augmente le choix, mais aussi la complexité de réservation, de placement des workloads et de suivi des coûts. Priorités recommandées : budgets par produit, attribution des coûts IA, extinction automatique des environnements non productifs et comparaison régulière des coûts de sortie réseau.

À retenir : la semaine confirme trois axes structurants : expansion géographique des capacités IA, montée en puissance des offres cloud souveraines européennes et nécessité de renforcer le patching des plans d’administration. La disponibilité de nouvelles régions ne doit pas masquer les contraintes de coûts, de licences et de résilience.

Sources :
- AWS, Amazon EVS disponible dans des régions supplémentaires : https://aws.amazon.com/about-aws/whats-new/2026/09/amazon-evs-available-in-additional-regions/
- AWS, EC2 P6-B200 à Hyderabad : https://aws.amazon.com/about-aws/whats-new/2026/09/amazon-ec2-p6-b200-instances-available-asia-pacific-hyderabad/
- Cerebras, six data centers IA en Amérique du Nord et en Europe : https://www.datacenterdynamics.com/en/news/cerebras-plans-six-new-ai-data-centers-in-north-america-and-europe/
- Civo/Era4, cloud IA souverain au Royaume-Uni : https://www.datacenterdynamics.com/en/news/civo-and-era4-launch-sovereign-ai-cloud-offering-in-the-uk/
- The Register, Patch Tuesday Microsoft de septembre 2026 : https://www.theregister.com/security/2026/09/09/microsoft-breaks-patch-tuesday-record-with-974-cve-deluge/
- AWS, actualités et annonces : https://aws.amazon.com/new/
- Google Cloud Service Health : https://status.cloud.google.com/incidents.json

Sources :
- VMware vCenter CVE (SecurityWeek) : https://www.securityweek.com/critical-vmware-vcenter-vulnerability-in-attackers-crosshairs/
- VMware vCenter exploitation APT (Vici Security) : https://www.vicisecurity.com/blog/critical-flaws-exploited-within-days-august-2026-patch-window/
- VMM Escape Glasswing (Decryption Digest) : https://www.decryptiondigest.com/blog/vmm-escape-cve-2026-glasswing-hypervisor-security
- Proxmox 24/7 Support + North America (Proxmox) : https://www.proxmox.com/en/about/company-details/press-releases/proxmox-24-7-support-and-proxmox-north-america/
- Proxmox 24/7 analyse (Virtualization Howto) : https://www.virtualizationhowto.com/2026/09/proxmox-just-removed-one-of-its-biggest-weaknesses/
- NVIDIA G20 (TechXplore) : https://techxplore.com/news/2026-09-nvidia-boss-g20-ministers-ai.html
- NVIDIA Hugging Face (Gizmodo) : https://gizmodo.com/nvidia-ceo-says-hugging-face-will-remain-an-open-platform-for-the-entire-ai-ecosystem-2000806742
- Hyperscaler capex scrutiny (CNBC) : https://www.cnbc.com/2026/07/28/hyperscalers-face-higher-capex-scrutiny-after-alphabet-report-panned.html
- Cloud cost optimization 2026 (CSA) : https://cloudsecurityalliance.org/blog/2026/06/12/top-cloud-cost-optimization-techniques-in-2026-for-maximum-roi
- EU Sovereign Cloud Framework (European Commission) : https://commission.europa.eu/news-and-media/news/sovereign-cloud-framework-explained-2026-06-01_en
- EU cloud sovereignty analysis (LinkedIn) : https://www.linkedin.com/pulse/european-cloud-sovereignty-2026-reality-vs-aspiration-claraz--9ikee
- VMware Explore Private AI Cloud (NextPlatform) : https://www.nextplatform.com/cloud/2026/09/01/vmware-intros-private-ai-cloud-ai-factory-as-workloads-shift-to-on-prem/5293559
- VMware Explore AI Factory (StorageNewsletter) : https://www.storagenewsletter.com/2026/09/02/vmware-explore-2026-broadcom-introduces-vmware-private-ai-cloud-enabling-enterprises-to-scale-ai-cost-effectively-operate-more-securely-and-innovate-rapidly/
- VMware AI Factory VCF 9.1.1 (VMware Blogs) : https://blogs.vmware.com/cloud-foundation/2026/09/03/explore-2026-vmware-ai-factory-and-other-new-ai-innovations-in-vcf/
- VCF 9.1.1 AI Kubernetes (VMware Blogs) : https://blogs.vmware.com/cloud-foundation/2026/09/03/new-ai-and-kubernetes-private-cloud-operations-capabilities-in-vmware-cloud-foundation-9-1-1/
- VMware Explore wrap-up (The Cube Research) : https://thecuberesearch.com/vmware-explore-2026-wrap-up-private-cloud-becomes-the-operating-layer-for-enterprise-ai/
- GCP us-central1-b outage (shattered.io) : https://shattered.io/gcp-us-central1-b-outage-15-services-2026/
- GCP incident details (Google Cloud Status) : https://status.cloud.google.com/incidents/J5ia5t9p3g9Q5Wi7r8Ev
- Broadcom VMware licensing (Redress) : https://redresscompliance.com/broadcom-vmware-licensing-changes-explained
- Data Centre News - Weekly Review 24/07/2026 (Substack) : https://datacentrenews.substack.com/p/weekly-data-centre-news-24072026
- AI Hardware July 2026 (Skycrumbs) : https://skycrumbs.com/blog/ai-hardware-news-july-2026
- Critical CVE 2026 Hub (CyberUpdates365) : https://cyberupdates365.com/cve-vulnerabilities-2026-enterprise-security-hub/
- Proxmox Roadmap - PSA-2026-00014 : https://pve.proxmox.com/wiki/Roadmap
- Mistral AI souveraineté France (GlobalCodeMaster) : https://globalcodemaster.com/frances-sovereign-ai-surge-mistral-ais-dollar14b-european-data-centre-push-and-macrons-vision
- Startups canadiennes vers cloud européen (Noah News) : https://noah-news.com/canadian-startups-turn-to-european-cloud-providers-to-navigate-data-sovereignty-and-compliance/
- Data sovereignty analysis (Curious Minds) : https://curiousminds.info/technology-ai/sovereignty-is-a-pipe-not-a-passport-2/
- AI FinOps Cloud Cost 2026 (HCL) : https://www.hcl-software.com/blog/myxalytics/how-ai-driven-finops-platforms-will-transform-cloud-cost-management-in-2026
- ServiceNow Cloud+ FinOps (ServiceNow Community) : https://www.servicenow.com/community/cloud-cost-management-articles/cloud-is-here-and-servicenow-ccm-is-leading-finops-into-2026/ta-p/3458789
- Cloud Outages August 2026 (isinternetup) : https://www.isinternetup.com/outages/2026/august
- Cloud Outage Tracker 2026 (Axis Intelligence) : https://axis-intelligence.com/cloud-outage-tracker/
- VMware licensing 2026 (Redress Compliance) : https://redresscompliance.com/broadcom-vmware-licensing-changes-explained
- VMware licensing guide (Schneider.im) : https://www.schneider.im/vmware-by-broadcom-portfolio-simplification-and-transition-to-subscription/
- VMware licensing cloud providers (Acronis) : https://www.acronis.com/en/blog/posts/vmware-licensing-changes/
- VMware licensing stabilization (Stormagic) : https://stormagic.com/company/blog/vmware-licensing-changes/
