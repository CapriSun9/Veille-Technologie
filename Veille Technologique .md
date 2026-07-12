# Veille-Technologie


Fin 2025 – grandes annonces cloud
3 novembre 2025 : OpenAI signe un accord d’infrastructure cloud d’environ 38 milliards de dollars avec AWS pour du compute IA à grande échelle.
​

5 novembre 2025 : Microsoft, Google, AWS, Oracle, SAP, Snowflake renforcent leurs partenariats croisés pour l’IA, montrant une forte interconnexion entre hyperscalers.
​

10 décembre 2025 : Microsoft annonce une première “AI superfactory” à Atlanta, reliant plusieurs datacenters avec des centaines de milliers de GPU et des exaoctets de stockage.
​

Fin décembre 2025 : plusieurs analyses parlent d’un “retour” de l’on‑prem en 2026 comme complément du cloud pour les workloads critiques, et d’un “tipping point” du cloud public (article du 26 janvier 2025, série d’analyses).
​

2025 – Sécurité et virtualisation
Fin mars 2025 : les architectures Zero Trust sont décrites comme en train de devenir un standard dans les environnements virtualisés pour limiter les mouvements latéraux entre VM et containers.
​

Toute l’année 2025 : montée en puissance des solutions de virtualisation type VMware, Hyper‑V et alternatives KVM/Proxmox, avec un focus sur la sécurité, l’isolation et la micro‑segmentation réseau.
​

Début 2026 – Coûts, IA et GPU
1ᵉʳ janvier 2026 : des articles indiquent que les coûts cloud deviennent le 2ᵉ poste de dépense IT des entreprises moyennes, juste derrière le personnel, surtout à cause des workloads IA et de la variabilité mensuelle des factures.
​

5 janvier 2026 : CoreWeave annonce l’adoption de la plateforme NVIDIA Rubin pour son cloud IA, avec des déploiements prévus en 2026, ce qui renforce la course aux GPU spécialisés.
​

5 janvier 2026 : plusieurs synthèses de “7 tendances cloud 2026” insistent sur l’optimisation d’infrastructures pour l’IA (GPU, réseau, stockage) et l’essor de clouds spécialisés (neoclouds).
​
21 janvier & 5 mars 2026 : Cisco corrige une critique zero‑day (CVE‑2026‑20045) et 48 vulnérabilités , dont deux CVSS 10/10, touchant les équipements réseaux indispensables aux architectures cloud/hybrides.

2–3 février 2026 : panne Azure de plus de 10 heures affectant VMs, AKS, Managed Identities et pipelines CI/CD, en raison d'une mauvaise configuration de comptes de stockage Microsoft.

5 mai 2026 : une faille cPanel critique (CVSS 9.8) menace plus d' un million de sites , avec exploitation active – renforce l'idée de ne jamais exposer directement un panel d'administrateur.

Mai 2026 : une extension malveillante provoque le vol de secrets GitHub, AWS, Kubernetes, Docker , affectant plusieurs milliers de dépôts privés, montrant que la supply chain dev devient un point clé de la sécurité cloud.

Toute la période : pénurie structurelle de mémoire DRAM liée à l'IA (HBM), augmentation des coûts serveurs, besoin d'optimiser la densité VM et le placement des workloads (on‑prem + cloud + neoclouds IA).
2025–2026 : les analyses sur la souveraineté des données soulignent un rééquilibrage régional, avec une opportunité pour les acteurs cloud européens et les clouds locaux alignés RGPD.
​
Outages, souveraineté et multicloud
Année 2025 (plusieurs dates) : gros outages AWS/Azure/GCP et de services SaaS provoquent des interruptions touchant des millions d’utilisateurs, mettant en avant la fragilité systémique et les dépendances en chaîne (DNS, paiements, sécurité, etc.).
Fin 2025 – début 2026 : de plus en plus d’architectures recommandent un modèle hybride/multicloud (on‑prem + plusieurs clouds) pour réduire le risque d’un seul point de défaillance et reprendre le contrôle des coûts.


Mise a jour - juillet 2026
Virtualisation & couts
Ete 2026 : comparatif Proxmox VE vs VMware post-Broadcom - Proxmox VE estime a ~1 000 EUR/an contre 45 000 EUR+/an pour VMware (licence Broadcom). Renforce l'interet de l'open source pour les homelabs et PME, axe cle de mon projet Proxmox.

Securite & CVE (cloud / cyber)
Juin 2026 : CVE-2026-48567 - Azure HorizonDB, elevation de privileges, CVSS 10.0 (Patch Tuesday juin 2026).
2026 : CVE-2026-20253 - Splunk Enterprise, authentification manquante sur fonction critique, ajoutee au catalogue CISA KEV (exploitation active). Souligne l'importance du patch management et de la supervision des logs.

Sources :
- Proxmox vs VMware 2026 : https://tech-insider.org/proxmox-vs-vmware-2026/
- CVE-2026-48567 (CrowdStrike Patch Tuesday juin 2026) : https://www.crowdstrike.com/en-us/blog/patch-tuesday-analysis-june-2026/
- CVE-2026-20253 (CISA KEV) : https://www.cisa.gov/known-exploited-vulnerabilities-catalog
