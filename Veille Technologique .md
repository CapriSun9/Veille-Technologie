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

