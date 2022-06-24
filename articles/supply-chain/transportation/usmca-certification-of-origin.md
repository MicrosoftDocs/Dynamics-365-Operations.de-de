---
title: USMCA-Ursprungszertifizierung
description: Mit dieser Funktion können Sie die vom USMCA-Abkommen (United States-Mexico-Canada Agreement) vorgeschriebenen Ursprungszeugnisse drucken.
author: Weijiesa
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 2a87e1aa27085f1b4821d27cece782dffbcd2096
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851361"
---
# <a name="usmca-certification-of-origin"></a>USMCA-Ursprungszertifizierung

[!include [banner](../includes/banner.md)]

Mit dieser Funktion können Sie die vom USMCA-Abkommen (United States-Mexico-Canada Agreement) vorgeschriebenen Ursprungszeugnisse drucken.

Das *USMCA-Ursprungszertifizierung* enthält die für die Deklaration erforderlichen Mindestdatenelemente. Einige Datenelemente können vor dem Druck vorausgefüllt werden, während andere nach dem Druck manuell ausgefüllt werden müssen. Um eine Zollpräferenzbehandlung zu erhalten, muss das Dokument ausgefüllt sein und sich zum Zeitpunkt der Anmeldung im Besitz des Importeurs befinden. Das Dokument kann vom Importeur, Exporteur oder Hersteller ausgefüllt werden.

Sie können das Dokument für eine einzelne Sendung von der Seite **Alle Sendungen** Liste oder von der Seite **Sendungsdetails** drucken.

Der Zugriff auf das Dokument ist nur möglich, wenn das Land auf der primären Adresse für die juristische Entität die Vereinigten Staaten ist.

Abhängig von der Auswahl des Dokumentendrucks kann das Dokument mit Daten aus Ihrem System vorausgefüllt sein. Es ist möglich, Daten im gedruckten Dokument zu ändern oder hinzuzufügen, indem Sie das gedruckte Dokument in ein bearbeitbares Format exportieren, z. B. Microsoft Word. Nach dem Export können Sie alle erforderlichen Änderungen vornehmen, bevor eine Erklärung abgegeben wird.

## <a name="turn-on-the-usmca-feature"></a>Einschalten der USMCA-Funktion

Bevor Sie die USMCA-Funktion verwenden können, muss sie in Ihrem System eingeschaltet werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Transportverwaltung*
- **Name der Funktion:** *USMCA-Ursprungszeugnis*

## <a name="document-content"></a>Inhalt des Dokuments

Das USMCA-Ursprungsbeglaubigungsdokument enthält die folgenden Datenelemente:

- Adresselemente
- Rolle der bescheinigenden Partei
- Einzelne Sendung
- Rechnungen
- Rahmenperiode
- Artikeldetails
- Unterschrift des Zertifizierers
- Anzahl von Seiten

Weitere Informationen zu jedem dieser Elemente und wie ihre Werte ermittelt werden, finden Sie in den übrigen Abschnitten dieses Artikels.

## <a name="print-a-usmca-certification-of-origin-document"></a>Drucken eines USMCA-Ursprungsbeglaubigungsdokuments

Um eine USMCA-Ursprungszertifizierung für eine Sendung zu drucken, gehen Sie wie folgt vor:

1. Führen Sie einen der folgenden Schritte aus:
    - Gehen Sie zu **Transportverwaltung>Sendungen > Alle Sendungen** und wählen Sie die Sendung aus, für die Sie das Dokument drucken möchten.
    - Öffnen Sie die Seite **Sendungsdetails** für die Sendung, für die Sie das Dokument drucken möchten (es gibt mehrere Möglichkeiten, hierher zu gelangen, u. a. über die Seite **Alle Sendungen**).
1. Öffnen Sie im Aktivitätsbereich die Registerkarte **Sendungen** und wählen Sie in der Gruppe **Drucken** die Option **USMCA-Ursprungszertifizierung**.
1. Die Dialogbox **Ursprungszertifizierung** wird geöffnet. Nehmen Sie die in den folgenden Unterkapiteln beschriebenen Einstellungen vor und wählen Sie dann **OK**, um das Dokument zu erzeugen.
1. Es öffnet sich eine Vorschau des Dokuments. Verwenden Sie die Befehle im Aktivitätsbereich, um das Dokument nach Bedarf zu drucken oder zu exportieren.

### <a name="certifying-party"></a>Zertifizierende Partei

Verwenden Sie die Dropdown-Liste **Beglaubigende Partei**, um die Art der Partei zu bestimmen, die das Dokument druckt. Geben Sie an, ob es sich bei der zertifizierenden Partei um den *Exporteur*, *Exporteur und Hersteller*, *Hersteller* oder *Importeur* handelt; oder lassen Sie das Feld leer, wenn es sich bei der zertifizierenden Partei um keine dieser Optionen handelt. Die von Ihnen gewählte Option bestimmt, was in den Adressbereichen des Dokuments gedruckt wird.

Der **Beglaubiger**, den Sie wählen, wird in das gedruckte Dokument aufgenommen.

Das Dokument kann sowohl für eingehende als auch für ausgehende Sendungen gedruckt werden. Wählen Sie *Importeur* als **Beglaubigende Partei** nur für eingehende Sendungen.

Die folgende Tabelle beschreibt die Arten von Informationen, die im Dokument enthalten sind, basierend auf der **Beglaubigenden Partei**, die Sie wählen.

| Zertifizierende&nbsp;Partei | Beschreibung |
|---|---|
| *\[Leer\]* | Fügt dem Dokument die folgenden Details hinzu:<ul><li>**Zertifizierer-Details**: Verwendet die Adressdetails für das Versandlager, falls verfügbar; andernfalls verwendet es die Adresse des Versandstandorts, falls verfügbar; andernfalls verwendet es die Adresse der juristischen Entität (Firma), die in Supply Chain Management ausgewählt wurde.</li><li>**Exporteur-Details**: Leer</li><li>**Hersteller-Details**: Leer</li><li>**Details zum Importeur**: Leer</li><ul>|
| *Exporteur* | Fügt dem Dokument die folgenden Details hinzu:<ul><li>**Zertifizierer-Details**: Verwendet die Adressdetails für das Versandlager, falls verfügbar; andernfalls verwendet es die Adresse des Versandstandorts, falls verfügbar; andernfalls verwendet es die Adresse der juristischen Entität (Firma), die in Supply Chain Management ausgewählt wurde.</li><li>**Details zum Exporteur**: Verwendet die Adressdetails für die juristische Entität.</li><li>**Hersteller-Details**: Leer</li><li>**Einzelheiten des Importeurs**: Verwendet das Rechnungskonto für den zugehörigen Auftrag.</li><ul>|
| *Exporteur und Produzent* | Fügt dem Dokument die folgenden Details hinzu:<ul><li>**Zertifizierer-Details**: Verwendet die Adressdetails für das Versandlager, falls verfügbar; andernfalls verwendet es die Adresse des Versandstandorts, falls verfügbar; andernfalls verwendet es die Adresse der juristischen Entität (Firma), die in Supply Chain Management ausgewählt wurde.</li><li>**Details zum Exporteur**: Verwendet die Adressdetails für die juristische Entität.</li><li>**Hersteller-Details**: Verwendet die Adressdetails für die juristische Entität.</li><li>**Einzelheiten des Importeurs**: Verwendet das Rechnungskonto für den zugehörigen Auftrag.</li><ul>|
| *Importeur* | Fügt dem Dokument die folgenden Details hinzu:<ul><li>**Zertifizierer-Details**: Verwendet die Adressdetails für das Versandlager, falls verfügbar; andernfalls verwendet es die Adresse des Versandstandorts, falls verfügbar; andernfalls verwendet es die Adresse der juristischen Entität (Firma), die in Supply Chain Management ausgewählt wurde.</li><li>**Exporteur-Details**: Leer</li><li>**Hersteller-Details**: Leer</li><li>**Importeur-Details**: Verwendet die Adressdetails für die juristische Entität.</li><ul>|
| *Produzent* | Fügt dem Dokument die folgenden Details hinzu:<ul><li>**Details zum Zertifizierer**: Verwendet die Adressdetails für das Versandlager, falls verfügbar; andernfalls wird die Adresse des Versandstandorts verwendet, falls verfügbar; andernfalls wird die Adresse der juristischen Entität verwendet, die in Supply Chain Management ausgewählt wurde.</li><li>**Exporteur-Details**: Leer</li><li>**Hersteller-Details**: Verwendet die Adressdetails für die juristische Entität.</li><li>**Importeur-Details**: Leer</li><ul>|

### <a name="has-various-producers"></a>Hat verschiedene Produzenten

Die Dropdown-Liste **Zertifizierende Partei** steuert den Text, der für die Herstellerangaben im Dokument verwendet werden soll. Wählen Sie eine der folgenden Optionen:

- *Verschiedene Hersteller* - Druckt den Text „Verschiedene“ in den Herstellerdetails.
- *Auf Anfrage erhältlich* - Drucken Sie den Text „Auf Anfrage bei den Einfuhrbehörden erhältlich“ in den Herstellerdetails.

Wenn die **Bescheinigende Partei** auf *Exporteur und Hersteller* oder *Hersteller* festgelegt ist, dann wird die Einstellung **Hat verschiedene Hersteller** außer Kraft gesetzt, und die Adressdetails des Herstellers entsprechen denen des Zertifizierers.

### <a name="blanket-period"></a>Rahmenperiode

Verwenden Sie die Einstellungen **Pauschalzeitraum von** und **Pauschalzeitraum bis**, um einen Pauschalzeitraum festzulegen, in dem das Dokument mehrere Sendungen identischer Waren abdeckt, auch wenn das Dokument nur für eine Sendung gedruckt wird. Sie können die Daten des Blankozeitraums ohne Einschränkungen festlegen, und er wird dem Dokument hinzugefügt. Sie können diese Einstellungen auch leer lassen oder sie in der Vergangenheit festlegen.

### <a name="is-single-shipment"></a>Ist einzelne Sendung

Legen Sie im Dialogfeld **Herkunftszertifikat** **Ist Einzelsendung** auf eine der folgenden Möglichkeiten fest:

- *Ja* - Fügt „Einzelsendung: Ja“ neben der Rechnungsnummer.
- *Nein* - Fügt nichts hinzu.

## <a name="other-information-included-in-the-document"></a>Andere im Dokument enthaltene Informationen

Zusätzlich zu den optionalen Elementen, die Sie über das Dialogfeld **Ursprungszeugnis** auswählen, enthält das USMCA-Ursprungszeugnis die Informationen und benutzerdefinierten Felder, die in den folgenden Unterabschnitten zusammengefasst sind. Einige dieser Informationen müssen manuell eingegeben werden, nachdem Sie das Dokument erzeugt haben.

### <a name="invoice-number"></a>Rechnungsnummer

Die IDs von Verkaufsrechnungen, die sich auf Sendungen beziehen, werden auf dem Dokument gedruckt, unabhängig von der Pauschalperiode. Die Rechnungsnummern werden unabhängig von der Auswahl **Ist Einzelsendung** gedruckt.

### <a name="item-details"></a>Artikeldetails

Der Beleg enthält mehrere Abschnitte, in denen spezifische Element-Details aufgelistet sind, nämlich

- **SKU-Nummer**: Druckt die Artikelnummer des freigegebenen Produkts.

- **Beschreibung**: Druckt entweder die Beschreibung oder den Namen für das freigegebene Produkt. Wenn eine Beschreibung in der Sprache des Benutzers vorhanden ist, wird diese gedruckt. Wenn keine solche Beschreibung existiert, dann wird der Name in der Sprache des Benutzers gedruckt. Wenn dieser Name nicht vorhanden ist, wird der Name des Elements gedruckt.

- **Harmonisiertes System (HS) Zolltarif-Klassifizierung**: Druckt den dem Produkt zugeordneten Harmonisierten Tarifschema. Sie können diese Zeitpläne festlegen, indem Sie zu **Transportverwaltung \> Einrichten \> Transportstandard \> Harmonisierte Zolltarifzeitpläne** gehen.

- **Herkunftskriterium:** Bei der ersten Freigabe des Dokuments müssen Sie die Daten in diesem Abschnitt manuell eingeben.

- **Herkunftsland:** Druckt das Herkunftsland, das Sie unter **Produktinformationsmanagement \> Einrichten \> Produktkonformität \> Herkunftsland** anwenden (siehe auch [Herkunftsland](../pim/country-of-origin.md)). Der ISO-Code für das Herkunftsland wird basierend auf dem Bestimmungsland/der Bestimmungsregion in der Lieferadresse der Sendung und dem Element gedruckt. Wenn keine Herkunftslanddaten festgelegt wurden, wird dieser Wert auf die Einstellung zurückgesetzt, die unter **Produktfreigabe \> Außenhandel \> Herkunft** zu finden ist. Wenn immer noch keine Herkunftslanddaten gefunden werden, dann müssen Sie das Herkunftsland nach dem Erzeugen des Dokuments manuell eingeben.

### <a name="certifier-signature-and-date"></a>Unterschrift und Datum des Zertifizierers

Dies müssen Sie nach dem Erzeugen des Dokuments manuell eingeben.

### <a name="consists-of-number-of-pages"></a>Besteht aus Anzahl der Seiten

Der Benutzer, der die Zertifizierung unterschreibt, muss die Anzahl der Seiten (zur Überprüfung) nach dem Generieren des Dokuments manuell eingeben.

### <a name="page-numbers"></a>Seitennummern

Die aktuelle Seite und die Anzahl der Seiten werden am unteren Rand des Dokuments gedruckt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]