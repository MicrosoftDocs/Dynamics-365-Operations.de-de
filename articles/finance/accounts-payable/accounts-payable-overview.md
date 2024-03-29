---
title: Kreditorenkonten konfigurieren – Übersicht
description: In diesem Artikel werden die Seiten beschrieben, die Sie verwenden, um die grundlegenden und optionalen Funktionen für Kreditorenkonten einzurichten. Er beschreibt zudem die Einrichtungsschritte, die Sie durchführen müssen, bevor Sie damit beginnen, die Kreditoren einzurichten.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bce5da0c9593bcfcfb9589f8fe7e09b8acd63726
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906531"
---
# <a name="configure-accounts-payable-overview"></a>Kreditorenkonten konfigurieren – Übersicht

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Seiten beschrieben, die Sie verwenden, um die grundlegenden und optionalen Funktionen für Kreditorenkonten einzurichten. Er beschreibt zudem die Einrichtungsschritte, die Sie durchführen müssen, bevor Sie damit beginnen, die Kreditoren einzurichten.

## <a name="prerequisites-for-accounts-payable-setup"></a>Voraussetzungen für die Einstellungen von Kreditoren

Die folgenden Einstellungen müssen abgeschlossen werden, bevor Sie Kreditoren einrichten können:

-   Im Hauptbuch:
    -   Wenn Sie Zahlungserfassungen verwenden möchten, müssen Sie Zahlungserfassungen einrichten.
    -   Wenn Sie Wechselkursregulierungen ausführen möchten, müssen Sie die Währungscodes auf der Seite **Währungen**, die Wechselkurstypen auf der Seite **Wechselkurstyp** und die Währungswechselkurse auf der Seite **Währungswechselkurse** einrichten.
-   Richten Sie Bankkonten zur Verwendung mit Zahlungsmethoden unter "Bargeld- und Bankverwaltung" ein.

## <a name="setup-pages-for-accounts-payable"></a>Seiten für Kreditorenkonten einrichten

Verwenden Sie die folgenden Seiten, um die grundlegenden Funktionen von Kreditoren für jede juristische Person einzurichten. Die Seiten sind in der empfohlenen Einrichtungsreihenfolge aufgeführt. Erstellen Sie aus den ersten erstellten Datensätzen Vorlagen, um das Verfahren zu erleichtern. Eine Vorlage umfasst normalerweise Werte in einer Vielzahl von Feldern, die die Funktionen widerspiegeln, die die Organisation für einen bestimmten Kreditorentyp implementieren möchte.
1.  Legen Sie auf der Seite **Zahlungsbedingungen**, die Zahlungsbedingungen fest, die Sie Aufträgen, Bestellungen, Debitoren und Kreditoren zuweisen wollen und die die Fälligkeitsdaten bestimmen. Weitere Informationen finden Sie unter [Kreditorenzahlungsübersicht definieren](tasks/define-vendor-payment-fees.md).
2.  Erstellen und pflegen Sie auf der Seite **Zahlungsmethoden – Kreditoren** Informationen zu der Art, wie die Organisation ihre Kreditoren bezahlt.
3.  Erstellen und pflegen Sie auf der Seite **Kreditorengruppen** Kreditorengruppen, die wichtige Parameter für Buchung, Ausgleich und Zahlung, die Berichterstellung und Planung gemeinsam haben.
4.  Definieren Sie auf der Seite **Kreditorenbuchungsprofile**, wie Kreditorenbuchungen im Hauptbuch gebucht werden.
5.  Richten Sie Standardeinstellungen auf der Seite **Kreditorenkontenparameter** ein, die angewendet werden, wenn keine spezifischere Einstellung angegeben wurde, sowie Parameter für verschiedene Arten von Funktionalität und die verschiedenen Nummernkreise für Kreditorenkonten.
6.  Legen Sie auf der Seite **Formulareinstellungen** das Format für verschiedene Dokumente fest, die sich auf Kreditoren beziehen und in der Organisation verwendet werden, um Belege von Kreditoren zu verfolgen und Gründe für den Zahlungsfluss an Kreditoren einzugeben.
7.  Erstellen und pflegen Sie auf der Seite **Kreditoren** die Kreditorenkonten, einschließlich der Steuerbehörden, bei denen Ihre Organisation die Mehrwertsteuer meldet.

## <a name="optional-setup-pages-for-accounts-payable"></a>Optionale Einrichtungsseiten für Kreditorenkonten
Neben den grundlegenden Funktionen, können Sie weitere Funktionen für Kreditoren einrichten.

Die Seiten für zusätzliche Einstellungen sind nach Funktionen geordnet.

**Richtlinien**
-   Richten Sie auf der Seite **Kreditorenrechnungsrichtlinie** Kreditorenrechnungsrichtlinien ein.

**Rechnungsabgleich**

-   Richten Sie auf der Seite **Rechnungssummentoleranzen** Toleranzen für Rechnungssummen ein.
-   Richten Sie auf der Seite **Abgleichsrichtlinie** zweiseitige und dreiseitige Abgleichsrichtlinien ein.
-   Richten Sie auf der Seite **Preistoleranzen** Toleranzen für Preise je Einheit ein.
-   Richten Sie auf der Seite **Preistoleranzgruppen für Artikel** Toleranzgruppen für Artikelpreise ein.
-   Richten Sie auf der Seite **Preistoleranzgruppen für Kreditoren** Toleranzgruppen für Kreditorenpreise ein.
-   Richten Sie auf der Seite **Toleranzen für Belastungen** Toleranzen für Belastungen ein.

**Workflow**

-   Richten Sie auf der Seite **Kreditorenkontenworkflows** die Workflowkonfigurationen für Erfassungsgenehmigungen und Bestellanforderung ein.

**Ursachen**

-   Richten Sie auf der Seite **Ursachen für Kreditoren** Ursachencodes ein.

**Belastungen**

-   Richten Sie auf der Seite **Belastungscodes** Codes für die Belastungen ein, die in Bestellungen verwendet werden.
-   Auf der Seite **Gruppe für Kreditorenbelastungen** können Sie Belastungsgruppen für Kreditoren erstellen und verwalten.
-   Auf der Seite **Gruppen für Artikelbelastungen** können Sie Belastungsgruppen für Artikel erstellen und verwalten.
-   Definieren Sie auf der Seite **Auto-Belastungen** Belastungen, die Aufträgen automatisch zugeordnet werden.

**Zusätzliche Artikel**

-   Auf der Seite **Zusätzliche Artikelgruppen – Kreditor**, erstellen und verwalten Sie zusätzliche Artikelgruppen für Kreditoren.
-   Auf der Seite **Zusätzliche Artikelgruppen – Bestand**, erstellen und verwalten Sie zusätzliche Artikelgruppen für Artikel.

**Verteilung**

-   Auf der Seite **Lieferbedingungen** erstellen und pflegen Sie die Bedingungen für den Transport eines Artikels vom Verkäufer zum Einkäufer.
-   Auf der Seite **Liefermodi** erstellen und pflegen Sie die Transportmethoden, die beim Liefern eines Auftrags vom Verkäufer an den Käufer verwendet werden.
-   Auf der Seite **Bestimmungsortcodes** erstellen und pflegen Sie Kennungen und Beschreibungen für Lieferziele.

**Formulare**

-   Erstellen Sie auf der Seite **Formularhinweise** den Standardtext, der auf verschiedenen Seiten angezeigt wird.
-   Richten Sie auf der Seite **Sortierparameter für Formulare** die Sortierreihenfolgen für Anforderungen, Eingangslisten, Lieferscheine und Rechnungen ein.
-   Richten Sie auf der Seite **Druckverwaltungseinstellungen** Druckverwaltungsinformationen für Originale und Kopien von Seiten ein.

**Zahlungen**

-   Richten Sie auf der Seite **Skonto** die Bedingungen für den Erhalt von Skonti ein, und verwalten Sie diese. Die Skontocodes sind mit Kreditoren verknüpft und werden auf Bestellungen angewendet.
-   Auf der Seite **Zahlungspläne** richten Sie die Zahlungspläne ein, die verwendet werden, um Teilzahlungen an Kreditoren zu verwalten.
-   Legen Sie auf der Seite **Zahlungstage** die Zahlungstage fest, die zur Berechnung von Fälligkeitsdaten verwendet werden, und geben Sie Zahlungstage für einen bestimmten Wochentag oder bestimmten Tag im Monat an.
-   Erstellen und pflegen Sie auf der Seite **Zahlungsgebühr** Zahlungsgebühren, die den Kreditoren zugeordnet sind.
-   Erstellen und verwalten Sie auf der Seite **Zahlungsanweisungen** Zahlungsanweisungen.

**Statistik**

-   Richten Sie auf der Seite **Zahlungsfristdefinitionen** benutzerdefinierte Intervalle zum Analysieren der Fälligkeitsverteilung von Kreditorenkonten ein.
-   Erstellen Sie auf der Seite **Branche** die Branchencodes (LOB-Codes), die den Kreditoren zugewiesen sind.

**Steuererklärung (US 1099)**

-   Überprüfen und aktualisieren Sie auf der Seite **1099 Felder** die Mindestbeträge, die dem Internal Revenue Service (IRS) auf Grundlage der neuesten IRS-Anforderungen gemeldet werden müssen.

## <a name="optional-setup-for-other-modules"></a>**Optionaler Setup für andere Module**
**Organisationsverwaltung**

-   Richten Sie auf der Seite **Nummernkreise** die Nummernkreisgruppen für Rechnungsnummern ein.
-   Richten Sie auf den folgenden Seiten Adressdaten ein:
    -   **Adresseinstellungen**
    -   **NAF-Codes**
    -   **Postleitzahlen importieren**

**Hauptbuch**

-   Richten Sie auf der Seite **Finanzdimensionen** Finanzdimensionen ein.
-   Richten Sie auf den folgenden Seiten Steuerinformationen ein:
    -   **Mehrwertsteuercodes**
    -   **Mehrwertsteuergruppen**
    -   **Artikel-Mehrwertsteuergruppen**
    -   **Kontengruppe**
    -   **Mehrwertsteuer-Befreiungscodes**
    -   **Umsatzsteuerzuständigkeiten**
    -   **Mehrwertsteuer-Behörden**
    -   **Mehrwertsteuer-Abrechnungszeiträume**

**Bargeld- und Bankverwaltung**

-   Richten Sie auf der Seite **Zahlungszweckcodes** den **Code für die Zentralbank** ein.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
