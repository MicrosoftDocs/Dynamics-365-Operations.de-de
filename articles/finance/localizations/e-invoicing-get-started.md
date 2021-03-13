---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 07954c5c96f390bc651794f8b6c61f2a1a17ab8b
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111219"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung erleichtern.

In der folgenden Tabelle sind die Funktionen für die elektronische Rechnungsstellung und die Geschäftsdokumente aufgeführt, auf die sie angewendet werden können.

| Funktionsname                         | Geschäftsdokument |
|--------------------------------------|-------------------|
| Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Brasilianisches NF-e (BR)                  | <p>Steuerdokument Modell 55</p><p>Korrekturschreiben</p> |
| Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente |
| Brasilianisches NFS-e São Paulo (BR)       | Dienst Steuerdokumente |
| Elektronische Rechnungen für Dänemark (DK)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Ägypten (EG)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Estland (EE)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Finnland (FI)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Frankreich (FR)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Deutschland (DE)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| FatturaPA (IT)                       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Mexikanische CFDI Interfactura (MX)       | <p>Verkaufsrechnung</p><p>Lieferschein</p><p>Lagerumlagerung</p><p>Zahlungsergänzung</p> |
| Elektronische Rechnungen für die Niederlande (NL)        | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Norwegen (NO)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen für Spanien (ES)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |
| Elektronische Rechnungen im PEPPOL-Format            | <p>Verkaufsrechnung</p><p>Projektrechnung</p> |

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:

- Konfigurieren Sie Ihren Regulatory Configuration Service (RCS) und Ihre Microsoft Dynamics 365 Finance- oder Dynamics 365 Supply Chain Management-Umgebung zur Übermittlung an das Add-On für die elektronische Rechnungsstellung.
- Erstellen Sie eine Dienst-Umgebung, und veröffentlichen Sie sie im Add-On für die elektronische Rechnungsstellung. Weitere Informationen finden Sie unter [Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md).
- Erstellen Sie eine verbundene Anwendung. Weitere Informationen finden Sie unter [Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md).
- Erstellen Sie einen Konfigurationsanbieter für Ihre Organisation. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Eine elektronische Rechnungsstellungsfunktion über den Microsoft-Konfigurationsanbieter importieren 

1. Melden Sie sich bei Ihrem RCS-Konto (Regulatory Configuration Service) an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie **Importieren** und anschließend **Synchronisieren** aus.
4. Filtern Sie die Spalte **Konfigurationsanbieter** nach dem Begriff **Microsoft**.
5. Wählen Sie den Namen einer elektronischen Rechnungsstellungsfunktion aus der Tabelle am Anfang dieses Themas und anschließend **Importieren** aus.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Eine elektronische Rechnungsstellungsfunktion unter Ihrem Organisationsanbieter erstellen

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereiches **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
2. Wählen Sie **Hinzufügen** > **Auf vorhandener Funktion basierend** aus, und geben Sie im Feld **Name** den Namen der elektronischen Rechnungsstellungsfunktion ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung der Funktion ein.
4. Wählen Sie im **Basisfunktionsfeld** die importierte elektronische Rechnungsstellungsfunktion des Microsoft-Konfigurationsanbieters aus.
5. Wählen Sie **Funktion erstellen**.

## <a name="configure-the-electronic-invoicing-feature"></a>Die elektronische Rechnungsstellungsfunktion konfigurieren

Je nach Land oder Region benötigt die elektronische Rechnungsstellungsfunktion möglicherweise eine zusätzliche Konfiguration. Informationen zu den spezifischen Schritten finden Sie in der Dokumentation „Erste Schritte“, die für Ihr Land oder Ihre Region verfügbar ist.

## <a name="configure-the-application-setup"></a>Anwendungseinrichtung konfigurieren

1. Wählen Sie die zuvor erstellte elektronische Rechnungsstellungsfunktion aus.
2. Überprüfen Sie auf der Registerkarte **Version**, ob die **Entwurf**-Version ausgewählt ist.
3. Wählen Sie auf der Registerkarte **Einrichtungen** **Anwendungseinrichtung** aus.

    > [!NOTE]
    > Überprüfen Sie, ob die Konfigurationsanbietereinstellung auf **Aktiv** für Ihre Organisation festgelegt ist. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Wählen Sie **Funktionseinrichtung** und anschließend **Verbundene Anwendung** aus.
5. Wählen Sie im Abschnitt **Elektronische Dokumenttypen** die Option **Hinzufügen** aus.
6. Wählen Sie für jedes von der Funktion unterstützte Geschäftsdokument **Tabellenname** aus, und geben Sie einen Wert gemäß folgender Tabelle ein.

    | Funktionsname                         | Geschäftsdokument | Name der Tabelle |
    |--------------------------------------|-------------------|------------|
    | Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Brasilianisches NF-e (BR)                  | <p>Steuerdokument</p><p>Korrekturschreiben</p> | Steuerdokument |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente | Steuerdokument |
    | Brasilianisches NFS-e São Paulo (BR)       | Dienst Steuerdokumente | Steuerdokument |
    | Elektronische Rechnungen für Dänemark (DK)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Ägypten (EG)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Estland (EE)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Finnland (FI)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Frankreich (FR)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Deutschland (DE)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | FatturaPA (IT)                       | <p>Verkaufsrechnung</p><p>Projektrechnung | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Mexikanische CFDI Interfactura (MX)       | <p>Verkaufsrechnung</p><p>Lieferschein</p><p>Lagerumlagerung</p><p>Zahlungsergänzung</p> | Debitorenrechnungserfassung |
    | Elektronische Rechnungen für die Niederlande (NL)        | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Norwegen (NO)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Spanien (ES)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen im PEPPOL-Format            | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |

7. Wählen Sie für jedes von der Funktion unterstützte Geschäftsdokument **Kontext** aus, und geben Sie einen Wert gemäß folgender Tabelle ein.

    | Funktionsname                         | Geschäftsdokument | Kontext |
    |--------------------------------------|-------------------|---------|
    | Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Brasilianisches NF-e (BR)                  | <p>Steuerdokument</p><p>Korrekturschreiben</p> | <p>Kontextmodell Debitorenrechnung – Kontext Steuerdokument</p><p>Kontextmodell Debitorenrechnung – Kontext FD-Korrekturschreiben</p> |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente| Kontextmodell Debitorenrechnung – Kontext Steuerdokument |
    | Brasilianisches NFS-e São Paulo (BR)       | Dienst Steuerdokumente| Kontextmodell Debitorenrechnung – Kontext Steuerdokument |
    | Elektronische Rechnungen für Dänemark (DK)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Ägypten (EG)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Estland (EE)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Finnland (FI)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Frankreich (FR)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Deutschland (DE)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | FatturaPA (IT)                       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Mexikanische CFDI Interfactura (MX)       | <p>Verkaufsrechnung</p><p>Lieferschein</p><p>Lagerumlagerung</p><p>Zahlungsergänzung</p> | Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung |
    | Elektronische Rechnungen für die Niederlande (NL)        | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Norwegen (NO)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Spanien (ES)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen im PEPPOL-Format            | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |

8. Wählen Sie für jedes von der Funktion unterstützte Geschäftsdokument **Geschäftsdokumentzuordnung** aus, und geben Sie einen Wert gemäß folgender Tabelle ein.

    | Funktionsname                         | Geschäftsdokument | Geschäftsdokumentzuordnungen |
    |--------------------------------------|-------------------|---------------------------|
    | Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Brasilianisches NF-e (BR)                  | <p>Steuerdokument</p><p>Korrekturschreiben</p> | <p>Steuerdokumentzuordnung – Zuordnung von Steuerdokumenten</p><p>Steuerdokumentzuordnung – Zuordnung von Korrekturschreiben</p> |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente | Steuerdokumentzuordnung – Zuordnung von Steuerdokumenten |
    | Brasilianisches NFS-e São Paulo (BR)       | Dienst Steuerdokumente | Steuerdokumentzuordnung – Zuordnung von Steuerdokumenten |
    | Elektronische Rechnungen für Dänemark (DK)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Ägypten (EG)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Estland (EE)     | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Finnland (FI)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Frankreich (FR)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Deutschland (DE)       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | FatturaPA (IT)                       | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Mexikanische CFDI Interfactura (MX)       | <p>Verkaufsrechnung</p><p>Lieferschein</p><p>Lagerumlagerung</p><p>Zahlungsergänzung</p> | Rechnungsmodellzuordnung – Debitorenrechnung |
    | Elektronische Rechnungen für die Niederlande (NL)        | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Norwegen (NO)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Spanien (ES)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen im PEPPOL-Format            | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |

Je nach Land oder Region benötigt die elektronische Rechnungsstellungsfunktion möglicherweise eine zusätzliche Konfiguration. Informationen zu spezifischen Schritten finden Sie in der Dokumentation „Erste Schritte“, die für Ihr Land oder Ihre Region verfügbar ist.

## <a name="deploy-the-electronic-invoicing-feature"></a>Die elektronische Rechnungsstellungsfunktion bereitstellen

1. Wählen Sie auf der Registerkarte **Versionen** die Funktionsversion für die elektronische Rechnungsstellung aus, die Sie bereitstellen möchten.
2. Wählen Sie **Status ändern** \> **Abgeschlossen**.
3. Wählen Sie **Status ändern** \> **Veröffentlichen** aus.
4. Wählen Sie **Bereitstellen** aus.
5. Stellen Sie die Option **In verbundener Anwendung bereitstellen** auf **Ja** ein.
6. Wählen Sie auf der Seite **Anwendung verbinden** die Verbindung aus, die Ihrer Instanz von Finance oder Supply Chain Management zugeordnet ist.
7. Stellen Sie die Option **In Service-Umgebung bereitstellen** auf **Ja** ein.
8. Wählen Sie im Feld **Service-Umgebung** das Add-On „Service-Umgebung“ für die elektronische Rechnungsstellung aus, in der Sie die elektronische Rechnungsstellungsfunktion bereitstellen möchten.
9. Wählen Sie im Feld **Startdatum** das Datum aus, an dem die elektronische Rechnungsstellungsfunktion im Add-On für die elektronische Rechnungsstellung wirksam werden soll.
10. Wählen Sie **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Die elektronische Rechnungsstellungsfunktion in Finance oder Supply Chain Management aktivieren

1. Melden Sie sich bei Finance oder Supply Chain Management an, und vergewissern Sie sich, dass Sie die richtige juristische Person aufgerufen haben.
2. Navigieren Sie zu **Organisationsverwaltung** \> **Einrichtung** \> **Parameter elektronischer Dokumente**.
3. Wählen Sie auf der Registerkarte **Funktionen** die in der folgenden Tabelle aufgeführte Funktionsreferenz oder -referenzen aus, um die elektronische Rechnungsstellungsfunktion für Finance oder Supply Chain Management zu aktivieren.

    | Funktionsname                         | Land/Region  | Funktionsreferenz |
    |--------------------------------------|-----------------|-------------------|
    | Elektronische Rechnungen für Österreich (AT)    | Österreich         | EUR-00023 |
    | Elektronische Rechnungen für Belgien (BE)      | Belgien         | EUR-00023 |
    | Brasilianisches NF-e (BR)                  | Brasilien          | BR-00053 |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Brasilien          | BR-00095 |
    | Brasilianisches NFS-e São Paulo (BR)       | Brasilien          | BR-00095 |
    | Elektronische Rechnungen für Dänemark (DK)       | Dänemark         | <p>EUR-00023</p><p>DK-00001</p> |
    | Elektronische Rechnungen für die Niederlande (NL)        | Die Niederlande | EUR-00023 |
    | Elektronische Rechnungen für Ägypten (EG)     | Ägypten           | EG-00008 |
    | Elektronische Rechnungen für Estland (EE)     | Estland         | EUR-00023 |
    | Elektronische Rechnungen für Finnland (FI)      | Finnland         | EUR-00023 |
     Elektronische Rechnungen für Frankreich (FR)       | Frankreich           | EUR-00023 |
    | Elektronische Rechnungen für Deutschland (DE)       | Deutschland         | EUR-00023 |
    | Mexikanische CFDI Interfactura (MX)       | Mexiko          | <p>MX-00010</p><p>MX-00016</p> |
    | Elektronische Rechnungen für Norwegen (NO)    | Norwegen          | <p>EUR-00023</p><p>NO-00010</p> |
    | Elektronische Rechnungen für Spanien (ES)      | Spanien           | <p>EUR-00023</p><p>ES-00025</p> |
    | Elektronische Rechnungen für Italien (IT)      | Italien           | <p>EUR-00023</p><p>IT-00036</p> |
    | Elektronische Rechnungen im PEPPOL-Format            | Europa          | EUR-00023 |

4. Wählen Sie **Speichern** aus.

## <a name="issue-electronic-invoices"></a>Elektronische Rechnungen ausstellen

1. Navigieren Sie zu **Organisationsverwaltung** \> **Periodisch** \> **Elektronische Dokumente** \> **Elektronische Dokumente übermitteln**.
2. Wählen Sie im Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus.
3. Wählen Sie **Hinzufügen** aus, um dem Abfragefilter einen Tabellennamen hinzuzufügen.
4. Wählen Sie die Tabelle aus, die die Rechnungen enthält.

    > [!NOTE]
    > Der Tabellenname muss in der Tabelle im Abschnitt [Anwendungseinrichtung konfigurieren](#configure-the-application-setup) weiter oben in diesem Thema aufgeführt sein.

5. Wählen Sie in der Tabelle den Feldnamen aus, den Sie abfragen möchten.
6. Geben Sie den Tabellen- und den Feldnamen für die Kriterien ein, nach denen abgefragt werden soll.
7. Wiederholen Sie die Schritte 5 und 6, um der Abfrage weitere Felder und Kriterien hinzuzufügen, und wählen Sie anschließend **OK** aus.
8. Wählen Sie **OK**.

## <a name="view-submission-logs"></a>Anzeigen von Übermittlungsprotokollen

1. Navigieren Sie zu **Organisationsverwaltung** \> **Periodisch** \> **Elektronische Dokumente** \> **Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Feld **Dokumenttyp** die Tabelle aus, die die Rechnungen enthält.

    > [!NOTE]
    > Der Tabellenname muss in der Tabelle im Abschnitt [Anwendungseinrichtung konfigurieren](#configure-the-application-setup) weiter oben in diesem Thema aufgeführt sein.

3. Wählen Sie im Raster eine Rechnung und anschließend **Abfragen** \> **Übermittlungsdetails** aus.

Je nach Land oder Region benötigt die elektronische Rechnungsstellungsfunktion möglicherweise eine zusätzliche Konfiguration. Informationen zu spezifischen Schritten finden Sie in der Dokumentation „Erste Schritte“, die für Ihr Land oder Ihre Region verfügbar ist.

## <a name="related-topics"></a>Verwandte Themen

- [Informationen zum Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Brasilien](e-invoicing-bra-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Mexiko](e-invoicing-mex-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien](e-invoicing-ita-get-started.md)
- [Elektronische Rechnungen für Kunden in Ägypten](emea-egy-e-invoices.md)
