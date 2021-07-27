---
title: Erste Schritte mit der elektronischen Rechnungsstellung
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 65944c3b73d5cecc8c86087729bcf8d2354c8f20
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6340154"
---
# <a name="get-started-with-electronic-invoicing"></a>Erste Schritte mit der elektronischen Rechnungsstellung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung erleichtern. Dieses Thema führt Sie durch die allgemeinen Konfigurationsschritte in Regulatory Configuration Services (RCS) und Dynamics 365 Finance und enthält die Schritte, die Sie ausführen müssen, um Geschäftsdokumente einzureichen und die Verarbeitungsergebnisse zu überprüfen.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:

- Konfigurieren Sie Ihre Microsoft Dynamics Lifecycle Services (LCS)-, Regulatory Configuration Service (RCS)- und Microsoft Dynamics 365 Finance- oder Dynamics 365 Supply Chain Management-Umgebung. Weitere Informationen finden Sie unter [Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md).
- Erstellen Sie einen Konfigurationsanbieter für Ihre Organisation. Weitere Informationen finden Sie unter [Einen Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Eine elektronische Rechnungsstellungsfunktion über den Microsoft-Konfigurationsanbieter importieren 

1. Melden Sie sich bei Ihrem RCS-Konto (Regulatory Configuration Service) an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie **Importieren** und anschließend **Synchronisieren** aus.
4. Filtern Sie die Spalte **Konfigurationsanbieter** nach dem Begriff **Microsoft**.
5. Wählen Sie den Namen einer elektronischen Rechnungsstellungsfunktion aus der Tabelle am Anfang dieses Themas und anschließend **Importieren** aus.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Eine elektronische Rechnungsstellungsfunktion unter Ihrem Organisationsanbieter erstellen

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
2. Wählen Sie **Hinzufügen** > **Auf vorhandener Funktion basierend** aus, und geben Sie im Feld **Name** den Namen der elektronischen Rechnungsstellungsfunktion ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung der Funktion ein.
4. Wählen Sie im **Basisfunktionsfeld** die importierte elektronische Rechnungsstellungsfunktion des Microsoft-Konfigurationsanbieters aus.
5. Wählen Sie **Funktion erstellen**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Länderspezifische Konfiguration für die elektronische Rechnungsstellungsfunktion

Je nach Land oder Region benötigt die elektronische Rechnungsstellungsfunktion möglicherweise eine spezielle Konfiguration. 

Informationen zu den spezifischen Schritten finden Sie in der Dokumentation „Erste Schritte“, die für Ihr Land oder Ihre Region verfügbar ist.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Importieren von Modellzuordnungskonfigurationen für elektronische Berichterstellung

1. Wählen Sie in RCS den Arbeitsbereich **Elektronische Berichterstellung** aus.
2. Wählen Sie aus der Liste der **Microsoft**-Konfigurationsanbieter **Repositorys** aus.
3. Wählen Sie **Global** und im Aktionsbereich **Öffnen** aus.
4. Importieren Sie die Modellzuordnungskonfigurationen gemäß der folgenden Tabelle nach Funktionsname.

| Funktionsname                         | Konfiguration der Modellzuordnung |
|--------------------------------------|-----------------------------|
| Elektronische Rechnungen für Österreich (AT)    | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Belgien (BE)      | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Brasilianisches NF-e (BR)                  | <p>Kontextmodell Debitorenrechnung</p><p>Steuerdokumente</p><p>Antwortnachrichtenmodell</p> |
| Brasilianisches NFS-e ABRASF Curitiba (BR) | <p>Kontextmodell Debitorenrechnung</p><p>Steuerdokumente</p><p>Antwortnachrichtenmodell</p> |
| Elektronische Rechnungen für Dänemark (DK)       | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Ägypten (EG)     | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p><p>Antwortnachrichtenmodell</p> |
| Elektronische Rechnungen für Estland (EE)     | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Finnland (FI)       | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Frankreich (FR)       | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Deutschland (DE)       | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| FatturaPA (IT)                       | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Mexikanische CFDI Interfactura (MX)       | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p><p>Antwortnachrichtenmodell</p> |
| Elektronische Rechnungen für die Niederlande (NL)        | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Norwegen (NO)    | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen für Spanien (ES)      | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |
| Elektronische Rechnungen im PEPPOL-Format            | <p>Kontextmodell Debitorenrechnung</p><p>Rechnungsmodell</p> |


## <a name="configure-the-application-setup"></a>Anwendungseinrichtung konfigurieren

1. Wählen Sie die zuvor erstellte elektronische Rechnungsstellungsfunktion aus.
2. Wählen Sie auf der Registerkarte **Einrichtungen** **Anwendungseinrichtung** aus.
3. Wählen Sie im Feld **Anwendung verbinden** die Verbindung aus, die Ihrer Instanz von Finance oder Supply Chain Management zugeordnet ist.
4. Wählen Sie im Abschnitt **Elektronische Dokumenttypen** die Option **Hinzufügen** aus.
5. Wählen Sie einen **Tabellenname** aus, und geben Sie einen Wert gemäß folgender Tabelle ein.

    | Funktionsname                         | Geschäftsdokument | Name der Tabelle |
    |--------------------------------------|-------------------|------------|
    | Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Debitorenrechnungserfassung</p><p>Projektrechnung</p> |
    | Brasilianisches NF-e (BR)                  | <p>Steuerdokument</p><p>Korrekturschreiben</p> | Steuerdokument |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente | Steuerdokument |
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

7. Für jeden Tabellennamen, den Sie erstellen, wählen Sie einen Kontextwert gemäß folgender Tabelle aus und geben ihn ein.

    | Funktionsname                         | Geschäftsdokument | Kontext |
    |--------------------------------------|-------------------|---------|
    | Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Kontextmodell Debitorenrechnung – Kontext Debitorenrechnung</p><p>Kontextmodell Debitorenrechnung – Kontext Projektrechnung</p> |
    | Brasilianisches NF-e (BR)                  | <p>Steuerdokument</p><p>Korrekturschreiben</p> | <p>Kontextmodell Debitorenrechnung – Kontext Steuerdokument</p><p>Kontextmodell Debitorenrechnung – Kontext FD-Korrekturschreiben</p> |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente| Kontextmodell Debitorenrechnung – Kontext Steuerdokument |
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

8. Wählen Sie gemäß folgender Tabelle für jeden Tabellennamen und Kontext einen Geschäftsdokumentzuordnungswert aus, und geben Sie ihn ein.

    | Funktionsname                         | Geschäftsdokument | Geschäftsdokumentzuordnungen |
    |--------------------------------------|-------------------|---------------------------|
    | Elektronische Rechnungen für Österreich (AT)    | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Elektronische Rechnungen für Belgien (BE)      | <p>Verkaufsrechnung</p><p>Projektrechnung</p> | <p>Rechnungsmodellzuordnung – Debitorenrechnung</p><p>Rechnungsmodellzuordnung – Projektrechnung</p> |
    | Brasilianisches NF-e (BR)                  | <p>Steuerdokument</p><p>Korrekturschreiben</p> | <p>Steuerdokumentzuordnung – Zuordnung von Steuerdokumenten</p><p>Steuerdokumentzuordnung – Zuordnung von Korrekturschreiben</p> |
    | Brasilianisches NFS-e ABRASF Curitiba (BR) | Dienst Steuerdokumente | Steuerdokumentzuordnung – Zuordnung von Steuerdokumenten |
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


## <a name="country-specific-configuration-of-application-setup"></a>Länderspezifische Konfiguration der Anwendungseinrichtung

Je nach Land oder Region benötigt die Anwendungseinrichtung möglicherweise eine spezielle Konfiguration. 

Informationen zu den spezifischen Schritten finden Sie in der Dokumentation „Erste Schritte“, die für Ihr Land oder Ihre Region verfügbar ist.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Bereitstellen der Funktion für die elektronische Rechnungsstellung in der Service-Umgebung

1. Wählen Sie auf der Registerkarte **Versionen** die Funktionsversion für die elektronische Rechnungsstellung aus, die Sie bereitstellen möchten.
2. Wählen Sie **Status ändern** \> **Abgeschlossen**.
3. Wählen Sie **Status ändern** \> **Veröffentlichen** aus.
4. Wählen Sie **Bereitstellen** aus.
5. Stellen Sie die Option **In verbundener Anwendung bereitstellen** auf **Nein** ein.
6. Stellen Sie die Option **In Service-Umgebung bereitstellen** auf **Ja** ein.
7. Wählen Sie im Feld **Service-Umgebung** die Service-Umgebung für die elektronische Rechnungsstellung aus, in der Sie die elektronische Rechnungsstellungsfunktion bereitstellen möchten.
8. Wählen Sie im Feld **Startdatum** das Datum aus, an dem die Funktion für die elektronische Rechnungsstellung in der elektronischen Rechnungsstellung wirksam werden soll.
9. Wählen Sie **OK**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Bereitstellen der Funktion für die elektronische Rechnungsstellung in der verbundenen Anwendung

1. Wählen Sie auf der Registerkarte **Versionen** eine Funktionsversion für die elektronische Rechnungsstellung aus, die Sie bereitstellen möchten.
4. Wählen Sie **Bereitstellen** aus.
5. Stellen Sie die Option **In verbundener Anwendung bereitstellen** auf **Ja** ein.
6. Wählen Sie im Feld **Anwendung verbinden** die Verbindung aus, die Ihrer Instanz von Finance oder Supply Chain Management zugeordnet ist.
7. Stellen Sie die Option **In Service-Umgebung bereitstellen** auf **Nein** ein.
10. Wählen Sie **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Die elektronische Rechnungsstellungsfunktion in Finance oder Supply Chain Management aktivieren

1. Melden Sie sich bei Finance oder Supply Chain Management an, und vergewissern Sie sich, dass Sie die richtige juristische Person aufgerufen haben.
2. Navigieren Sie zu **Organisationsverwaltung** \> **Einrichtung** \> **Parameter elektronischer Dokumente**.
3. Wählen Sie auf der Registerkarte **Funktionen** die länder-/regionenspezifische Funktion aus, um die Funktion für die elektronische Rechnungsstellung für Finanzen oder Supply Chain Management zu aktivieren. Die folgende Tabelle enthält eine Liste der Funktionen für die elektronische Rechnungsstellung, die für bestimmte Länder/Regionen verfügbar sind. 

    | Funktionsname                                          | Land/Region  |
    |-------------------------------------------------------|-----------------|
    | Elektronische Rechnungen für Österreich (AT)                     | Österreich         |
    | Elektronische Rechnungen für Belgien (BE)                       | Belgien         |
    | Elektronische Rechnung CFDI für Mexiko (MX)                  | Mexiko          |
    | Elektronische Rechnungen für Dänemark (DK)                        | Dänemark         |
    | Elektronische Rechnungen für die Niederlande (NL)                         | Die Niederlande |
    | Elektronische Rechnungen für Ägypten (EG)                      | Ägypten           |
    | Elektronische Rechnungen für Estland (EE)                      | Estland         |
    | Elektronische Rechnungen für Finnland (FI)                       | Finnland         |
    | Elektronische Rechnungen für Frankreich (FR)                        | Frankreich          |
    | Elektronische Rechnungen für Deutschland (DE)                        | Deutschland         |
    | Elektronische Rechnungen für Italien (IT)                       | Italien           |
    | NF-e Federal – Elektronische Rechnungen für Brasilien (BR)      | Brasilien          |
    | NFS-e – elektronische Rechnung für brasilianischen Dienst (Stadt)   | Brasilien          |
    | Elektronische Rechnungen für Norwegen (NO)                     | Norwegen          |
    | Elektronische Rechnungen im PEPPOL-Format                             | Global          |
    | Elektronische Rechnungen für Spanien (ES)                       | Spanien           |

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


## <a name="related-topics"></a>Verwandte Themen

- [Informationen zur elektronischen Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md)
- [Erste Schritte mit der elektronischen Rechnungsstellung für Brasilien](e-invoicing-bra-get-started.md)
- [Erste Schritte mit der elektronischen Rechnungsstellung für Mexiko](e-invoicing-mex-get-started.md)
- [Erste Schritte mit der elektronischen Rechnungsstellung für Italien](e-invoicing-ita-get-started.md)
- [Elektronische Rechnungen für Debitoren in Ägypten](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
