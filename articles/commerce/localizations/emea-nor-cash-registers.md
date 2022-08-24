---
title: Kassenfunktionalität für Norwegen
description: Dieser Artikel bietet einen Überblick über die in Norwegen verfügbaren Registrierkassenfunktionen Microsoft Dynamics 365 Commerce, und bietet Richtlinien zum Einrichten der Funktionalität.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 42eda805646dbb30b40528254a3137102e3075e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292735"
---
# <a name="cash-register-functionality-for-norway"></a>Kassenfunktionalität für Norwegen

[!include[banner](../includes/banner.md)]

Dieser Artikel bietet einen Überblick über die in Norwegen verfügbaren Registrierkassenfunktionen in Dynamics 365 Commerce. Es enthält auch Richtlinien zum Einrichten der Funktionalität. Die Funktionalität besteht aus folgenden Teilen:

- Gemeinsame Point-of-Sale (POS)-Funktionen, die Kunden in allen Ländern oder Regionen zur Verfügung stehen. Beispiele hierfür sind eine Option, mit der Sie verhindern können, dass eine Kopie eines Kassenbons mehr als einmal gedruckt wird.
- Norwegen-spezifische Funktionen, wie z. B. digitale Signaturen für Verkaufstransaktionen.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Übersicht über Kassenfunktionalität für Norwegen

### <a name="common-pos-features"></a>Allgemeine POS-Funktionen

Informationen zu allgemeinen POS-Szenarien und Funktionen, die für Debitoren in allen Ländern oder Regionen verfügbar sind, finden Sie in den [Hilfe-Ressourcen für Dynamics 365 Retail](../index.md).

Die folgenden POS-Lokalisierungsfunktionen, die zuvor implementiert und Kunden in allen Ländern oder Regionen zur Verfügung gestellt wurden, können jetzt speziell für Norwegen verwendet werden:

- **Drucken Sie Textfelder auf einem Beleg in großer Schriftgröße.** Sie können die **Schriftgröße** Parameter im Quittungsformat-Designer verwenden, um anzugeben, dass die große Schriftgröße für ein Feld im Quittungsformat verwendet werden soll. (Die große Schriftgröße ist ungefähr doppelt so groß wie die übliche Schriftgröße.) Mit diesem Parameter können Sie beispielsweise das Kennzeichen „Kopie“ auf einer Kopie eines Kassenbons in großen Zeichen drucken.
- **Registrieren Sie das Drucken von Belegkopien im POS-Audit-Ereignisprotokoll.** Sie können den **Prüfung** Parameter im POS-Funktionsprofil verwenen, um das Drucken von Belegkopien und die Registrierung anderer POS-Prüfereignisse zu ermöglichen. Die Audit-Ereignisse werden in der Kanaldatenbank und in der Zentrale registriert. Sie können die Prüfungsereignisse auf der Seite **Prüfungsereignisse** anzeigen.
- **Verhindern Sie, dass eine Kopie einer Quittung mehr als einmal gedruckt wird.** Wenn der **Prüfung** Parameter im POS-Funktionsprofil aktiviert ist, steuert die **Drucken von Belegkopien zulassen** POS-Berechtigung, ob Kopien von Belegen gedruckt werden können. Es gibt auch eine Option, mit der Sie verhindern können, dass eine Kopie eines Kassenbons mehr als einmal gedruckt wird.

Darüber hinaus wurde die folgende POS-Funktion für Norwegen implementiert, aber Kunden in allen Ländern oder Regionen zur Verfügung gestellt:

- **Registrieren Sie zusätzliche Ereignisse im POS-Audit-Ereignisprotokoll.** Wenn der **Prüfung** Parameter im POS-Funktionsprofil aktiviert ist, werden die folgenden Ereignisse im POS-Audit-Ereignisprotokoll registriert:

    - Preisüberprüfung
    - MwSt.-Überschreibung
    - Korrekturen der Zeilenmengen
    - Clearing von Transaktionen aus der Kanaldatenbank

### <a name="norway-specific-pos-features"></a>Norwegen-spezifische POS_Funktionen

Die folgenden Norwegen-spezifischen POS-Funktionen werden aktiviert, wenn der **ISO-Code** Parameter im POS-Funktionsprofil auf **Nein** festgelegt ist.

#### <a name="digital-signing-of-sales-transactions"></a>Digitales Signieren von Verkaufstransaktionen

Jeder Verkaufsvorgang wird digital signiert. Gleichzeitig mit dem Abschluss der Transaktion wird die Signatur erstellt und im POS-Transaktionsjournal aufgezeichnet. Die Signatur steht auch im Journal zur Verfügung, das zu Revisionszwecken exportiert wird.

Es werden nur Transaktionen für Barverkäufe unterzeichnet. Hier sind einige Beispiele für Transaktionen, die vom Signiervorgang ausgeschlossen sind:

- Vorauszahlungen (Debitorenkonto-Einzahlung)
- Vorauszahlungen für Kundenaufträge (Kundenauftragsanzahlung)
- Eine Geschenkkarte ausstellen
- Nichtverkaufstransaktionen (Gleitkomma-Eintrag, Ausschreibung usw.)

Die signierten Daten sind eine Textzeichenfolge, die aus den folgenden Datenfeldern besteht. Die Datenfelder sind durch Semikolons getrennt.

1. Vorherige Unterschrift für denselben POS (Eine Null \[**0**\] wird für die erste Transaktion verwendet.)
2. Transaktionsdatum
3. Transaktionsuhrzeit
4. Sequenzielle signierte Transaktionsnummer
5. Transaktionsbetrag inklusive Steuern
6. Transaktionsbetrag exklusive Steuern

Der digitale Signaturprozess verwendet einen RSA-1024-Bit-Schlüssel mit einer SHA-1-Hash-Funktion (RSA-SHA1-1024). Zum Signieren wird ein Zertifikat verwendet, das auf der Commerce Scale Unit installiert ist. Die eindeutige Kennung des Zertifikats (Speicherbedarf) wird zusammen mit der Signatur erfasst.

Die Signatur wird zusammen mit den Transaktionsdaten in der Storedatenbank und der Zentrale (HQ)-Datenbank gespeichert. Sie können die Transaktionssignatur zusammen mit den Transkationsdaen, die für die Erstellung verwendet wurden, auf der Seite **Steuertransaktionen** im Inforegister **Storetransaktionen** anzeigen.

#### <a name="receipts"></a>Eingänge

Belege für Norwegen können zusätzliche Informationen enthalten, die mithilfe von benutzerdefinierten Feldern implementiert wurden:

- **Belegtitel** – Sie können einem Belegformat-Layout ein Feld hinzufügen, um die Art des Belegs zu identifizieren. Ein Verkaufsbeleg enthält beispielsweise den Text Kaufbeleg.
- **Unterschriebene Transaktionssequenznummer** – Die fortlaufende Nummer einer unterschriebenen Transaktion kann auf dem Beleg erscheinen, um einen gedruckten Beleg mit einer digitalen Signatur in der Datenbank zu verknüpfen.
- **Eingangssummen** – Benutzerdefinierte Felder für Eingangssummen schließen Nichtverkaufsbeträge von den Gesamttransaktionsbeträgen aus. Nichtverkaufsbeträge beinhalten Beträge für die folgenden Operationen:

    - Vorauszahlungen (Debitorenkonto-Einzahlung)
    - Vorauszahlungen für Kundenaufträge (Kundenauftragsanzahlung)
    - Eine Geschenkkarte ausstellen
    - Aufladen einer Geschenkkarte

#### <a name="x-and-z-reports"></a>X- und Z-Berichte

Die in den X- und Z-Berichten enthaltenen Informationen basieren auf den norwegischen Anforderungen. Beispielsweise **Gesamte Barverkäufe** Beträge umfassen nur Beträge für Barverkaufstransaktionen und schließen die Ausgabe von Geschenkkarten und Vorauszahlungen aus. Außerdem werden die Gesamtbarverkäufe pro Artikelgruppe und Zahlungsmethode aufgeführt. Darüber hinaus werden kumulative **Gesamtumsatz** und **Gesamterträge** Beträge gepflegt und gedruckt.

#### <a name="saf-t-cash-register-audit-file"></a>SAF-T-Bargelderfassung-Protokolldatei

Sie können das POS-Transaktionsjournal in der vordefinierten Standard-Protokolldatei – Steuern (SAF-T) Barregisterformat exportieren. Die Protokolldatei enthält Informationen über die Organisation, relevante Stammdaten (wie Artikelgruppen, Artikel und Steuercodes), Transaktionsdaten für Barverkäufe zusammen mit Unterschriften für diese Transaktionen, Daten zu Nichtverkaufsereignissen und Berichtsdaten zum Ende des Datums.

Die Protokolldatei kann für die folgenden Szenarien exportiert werden:

- Pro Store
- Alle Shops
- Pro Terminal
- Alle Terminals

Sie können auch einen Bericht von einer juristischen Person im Namen einer anderen juristischen Person senden. In diesem Fall müssen Sie den Export von der ausführenden juristischen Person aus durchführen und die meldende juristische Person als Absender der Meldung angeben.

Das Registrierkassenformat SAF-T wird in der Zentrale durch die Verwendung von [Elektronische Berichterstattung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) implementiert. 

## <a name="setting-up-commerce-for-norway"></a>Einrichten von Commerce für Norwegen

In diesem Abschnitt werden die Retail-Einstellungen beschrieben, die für Norwegen spezifisch und empfohlen sind. Weitere Informationen finden Sie in den [Hilfe-Ressourcen für Dynamics 365 Retail](../index.md).

Um die Norwegen-spezifischen Funktionen zu verwenden, müssen Sie diese Aufgaben ausführen:

- Legen Sie das Feld **Land/Region** auf **NOR** (Norwegen) als primäre Adresse für die juristische Person fest.
- Legen Sie das Feld **ISO-Code** im Feld **NO** (Norwegen) im POS-Funktionsprofil der einzelnen Stores in Norwegen auf Norwegen fest.

Sie müssen auch die folgenden Einstellungen für Norwegen angeben.

### <a name="set-up-the-legal-entity"></a>Legen Sie die juristische Entität fest

Stellen Sie sicher, dass der Name der juristischen Person angegeben ist. Dieser Name wird auf X- und Z-Berichten gedruckt.

Geben Sie zusätzlich im Inforegister **Bankkontoinformationen** im Feld **Routingzahl** die Organisationszahl ein.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Mehrwertsteuer (MwSt.) gemäß norwegischen Anforderungen einrichten


Sie müssen Mehrwertsteuercodes, Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen erstellen. Sie müssen auch Mehrwertsteuerinformationen für Produkte und Dienstleistungen einrichten. Weitere Informationen dazu, wie die Mehrwertsteuer in [Mehrwertsteuerüberblick](../../finance/general-ledger/indirect-taxes-overview.md) eingerichtet und verwendet wird.

Sie müssen auch Mehrwertsteuergruppen angeben und die Option **Preise inklusive Umsatzsteuer** für Stores aktivieren, die sich in Norwegen befinden.

### <a name="set-up-functionality-profiles"></a>Einrichten von Funktionsprofilen

Sie müssen die Überwachung aktivieren und die Belegnummerierung einrichten.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Aktualisieren Sie POS-Berechtigungsgruppen und individuelle Berechtigungseinstellungen für Storearbeitskräfte

Legen Sie die **Drucken der Quittungskopie zulassen** Erlaubnis auf einen geeigneten Wert fest:

- **Immer zulassen** – Der Operator kann eine Kopie eines Kassenbons mehrmals ausdrucken.
- **Nur einmal zulassen** – Der Operator kann eine Kopie eines Kassenbons nur einmal ausdrucken.
- **Nur einmal zulassen und nur wenn HQ DB verfügbar ist** – Der Operator kann eine Kopie einer Quittung nur einmal ausdrucken und nur, wenn die HQ-Datenbank über Commerce Data Exchange: Echtzeit-Service, damit das System überprüfen kann, ob zuvor in keinem Geschäft Kopien des Kassenbons gedruckt wurden, verfügbar ist.
- **Nie** – Der Operator kann nie eine Kopie eines Kassenbons ausdrucken.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurieren Sie benutzerdefinierte Felder, damit sie in Belegformate für Verkaufsbelege verwendet werden können

Fügen Sie auf der Seite **Sprachentext** die folgenden Datensätze für die Beschriftungen der benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass **Sprachen-ID**, **Text-ID** und **Text**-Werte, die in der Tabelle angezeigt werden, nur Beispiele sind. Sie können sie ändern, damit sie Ihre Anforderungen erfüllen.

| Sprachkennung | Text                   | Textkennung |
|-------------|------------------------|---------|
| en-US       | Zugangsname          | 900011  |
| en-US       | Ist Geschenkkarte           | 900012  |
| en-US       | Gesamt (Umsatz)          | 900013  |
| en-US       | Steuer gesamt (Mehrwertsteuer)      | 900014  |
| en-US       | Gesamtbetrag mit Steuern (Umsatz) | 900015  |
| en-US       | Steuerbetrag (Umsatz)     | 900016  |
| en-US       | Bargeldbuchungskennung    | 900017  |

Fügen Sie auf der Seite **Benutzerdefinierte Felder** die folgenden Datensätze für die benutzerdefinierten Felder für Bonlayouts hinzu. Beachten Sie, dass die Werte für **Untertitelrext-ID** den Werten **Textkennung** entsprechen müssen, die Sie auf der Seite **Sprachentext** angegeben haben.

| Name                            | Typ    | Textkennung Titel |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Zugang | 900011          |
| IsGiftCard                      | Zugang | 900012          |
| SalesTotalExt                   | Zugang | 900013          |
| TaxTotalExt                     | Zugang | 900014          |
| TotalWithTaxExt                 | Zugang | 900015          |
| AmountPerTaxExt                 | Zugang | 900016          |
| CashTransactionSequentialNumber | Zugang | 900017          |

> [!NOTE]
> Es ist wichtig, dass Sie die richtigen benutzerdefinierten Feldnamen angeben, wie in der vorherigen Tabelle aufgeführt. Ein falscher benutzerdefinierter Feldname führt zu fehlenden Daten in Belegen.

### <a name="configure-receipt-formats"></a>Bonformate konfigurieren

Sofern notwending ändern Sie für jedes erforderliche Format den Wert des Felds **Druckverhalten** auf **Immer drucken**.

In Designer für Bonformat fügen Sie die folgenden benutzerdefinierten Felder den entsprechenden Bonabschnitten hinzu. Beachten Sie, dass die Feldnamen den Sprachtexten entsprechen, die Sie im vorherigen Abschnitt definiert haben.

1. Header:

    - **Belegtitel** – Dieses Feld identifiziert die Art des Kassenbons.
    - **Bargeldtransaktions-ID** – Dieses Feld druckt die fortlaufende Nummer der signierten Bargeldtransaktion.

2. Positionen:

    - **Ist Geschenkkarte** – Dieses Feld markiert die Quittungszeile im Zusammenhang mit dem Vorgang Geschenkkarte ausstellen oder Zu Geschenkkarte hinzufügen.

3. Fußzeile:

    - **Summe (Verkauf)** – Dieses Feld druckt den Beleg des Gesamt-Barverkaufsbetrags. Der Betrag enthält keine Steuer. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
    - **Gesamtsteuer (Verkauf)** – Dieses Feld druckt den Gesamtsteuerbetrag für Barverkäufe des Belegs. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
    - **Summe mit Steuer (Verkauf)** – Dieses Feld druckt den Beleg des Gesamt-Barverkaufsbetrags. Der Betrag enthält Steuer. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.
    - **Steuerbetrag (Verkauf)** – Dieses Feld druckt den Gesamtsteuerbetrag für Barverkäufe pro Steuercode. Vorauszahlungen und Geschenkkartenvorgänge werden ausgeschlossen.

Weitere Informationen zum Arbeiten mit Belegformaten finden Sie unter [Einrichten und Entwerfen von Bonformaten](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>Konfigurieren Sie das Exportformat SAF-T Registrierkasse

Die Konfiguration der SAF-T Registrierkasse steht zum Download bereit unter Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen importieren](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Sie müssen die folgenden Konfigurationen herunterladen:

- **Einzelhandelskanal data.Version.1** – Die Datenmodellkonfiguration.
- **DMM Einzelhandelskanal data.Version.1.14** – Die Datenmzuordnungsmodellkonfiguration.
- **NO SAF T Registrierkasse.Version.1.20** – Die Formatkonfiguration.

Nachdem Sie die Konfigurationen importiert haben, wählen Sie auf der **Handelsparameter** Seite, auf der **Elektronische Dokumente** Registerkarte, im **SAF-T Registrierkassen-Exportformat** m Feld den Namen der importierten Formatkonfiguration aus.

Außerdem müssen Sie die erforderlichen Stammdaten vordefinierten SAF-T-Standardcodes zuordnen. Weitere Informationen finden Sie in der SAF-T-Registrierkassendokumentation, die von der norwegischen Steuerbehörde bereitgestellt wird. Um die Zuordnung zu erstellen, müssen Sie das neue **Feld AF-T Registrierkassencode** auf den folgenden Seiten festlegen.

- Artikelgruppen
- Zahlungsmethoden
- Mehrwertsteuercodes

### <a name="configure-channel-components"></a>Kanal-Komponenten konfigurieren

Um die Norwegen-spezifische Funktionalität zu aktivieren, müssen Sie Kanalkomponenten konfigurieren. Weitere Informationen finden Sie unter [Bereitstellungsrichtlinien](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
