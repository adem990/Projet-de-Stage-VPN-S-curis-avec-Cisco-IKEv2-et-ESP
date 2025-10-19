# 🔒 Projet de Stage – VPN Sécurisé avec Cisco, IKEv2 et ESP

[![Stage](https://img.shields.io/badge/Stage-2024%2F2025-blue)](https://www.sii.tn)  
[![Technologies](https://img.shields.io/badge/Technologies-Cisco%20%7C%20GNS3%20%7C%20Wireshark-blueviolet)]  
[![Licence](https://img.shields.io/badge/Licence-Propre-brightgreen)]  

---

## 📌 Présentation du Projet

Ce projet a pour objectif la **conception, configuration et analyse d’un tunnel VPN sécurisé** entre deux sites distants, utilisant :  

- **IPsec avec IKEv2 et ESP**  
- **Routeurs Cisco**  
- **GNS3 pour la simulation réseau**  
- **Wireshark pour l’analyse et la validation de sécurité**  

Réalisé dans le cadre d’un stage chez **S.I.I (Service d’Intelligence Informatique)**, il démontre l’application concrète des concepts de réseaux et cybersécurité dans un environnement professionnel.

---

## 🎯 Objectifs

1. Comprendre les concepts de **VPN et protocoles de sécurité**.  
2. Configurer un **tunnel VPN sécurisé** sur routeurs Cisco.  
3. Tester le tunnel via **GNS3 et commandes Cisco**.  
4. Vérifier le trafic VPN avec **Wireshark** :  
   - Authentification des pairs (IKEv2)  
   - Chiffrement des données (ESP)  
5. Développer des compétences pratiques avancées en **réseaux et cybersécurité**.

---

## 🛠️ Technologies et Outils

| Catégorie         | Technologie / Outil             |
|------------------|--------------------------------|
| Routeurs          | Cisco IOS                      |
| VPN               | IPsec, IKEv2, ESP              |
| Simulation Réseau | GNS3                           |
| Analyse Réseau    | Wireshark                      |
| Documentation     | UML, PDF                       |

---

## 📂 Structure du Projet

VPN-Stage/
│
├─ Configurations/
│ ├─ Router1.cfg # Configuration routeur 1
│ ├─ Router2.cfg # Configuration routeur 2
│
├─ Wireshark/
│ ├─ Capture_Figure2.png # Vérification IKEv2 SA
│ ├─ Capture_Figure3.png # Paquet chiffré ESP
│ ├─ Capture_Figure4.png # Capture complète Wireshark
│
├─ Documentation/
│ ├─ Rapport_Stage.pdf # Rapport complet du stage
│ ├─ Diagrammes_UML.pdf # Schémas réseau et diagrammes
│
└─ README.md

yaml
Copier le code

---

## 🚀 Instructions d’Exécution

### 1. Préparer l’environnement
- Installer **GNS3** et créer une topologie avec deux routeurs Cisco.  
- Importer les configurations `Router1.cfg` et `Router2.cfg`.

### 2. Vérifier le VPN
- Depuis chaque routeur, exécuter :  
```bash
show crypto ikev2 sa
show crypto ipsec sa
Confirmer que le tunnel VPN est actif.

3. Tests de Connectivité
Utiliser ping pour vérifier la communication entre les réseaux internes des deux sites via le tunnel VPN.

4. Analyser le trafic avec Wireshark
Lancer une capture sur le réseau VPN.

Filtrer les paquets :

IKEv2 : udp.port == 500

ESP : esp

Vérifier que les paquets sont chiffrés et que l’authentification est valide.

📷 Figures et Captures
Figure 2 – Vérification de crypto ikev2 sa

Montre la négociation IKEv2 et l’authentification réussie entre les routeurs.

Figure 3 – Paquet ESP chiffré

Les paquets apparaissent chiffrés, confirmant la confidentialité des données en transit.

Figure 4 – Capture complète Wireshark

Illustration globale du trafic VPN sécurisé entre les deux sites.

✅ Résultats Attendus
Tunnel VPN opérationnel et sécurisé.

Authentification IKEv2 confirmée.

Trafic chiffré ESP vérifié.

Communication stable entre les réseaux locaux.

Documentation complète et analyse de trafic validée.

📚 Références
Cisco IPsec & IKEv2 Documentation

Wireshark User Guide

GNS3 Network Simulation



