---
title: Erste Schritte mit der Steuerberechnung
description: In diesem Thema wird erläutert, wie Steuerberechnungen eingerichtet werden.
author: wangchen
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0ab9c0cf974114c4fa9b673e5601e138acef534d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685910"
---
# <a name="get-started-with-tax-calculation"></a>Erste Schritte mit der Steuerberechnung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den ersten Schritten mit der Steuerberechnung. Zunächst werden Sie in diesem Thema durch die allgemeinen Konfigurationsschritte in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) und Dynamics 365 Finance sowie Dynamics 365 Supply Chain Management geführt. 

Die Einrichtung besteht aus drei Hauptschritten.

1. Installieren Sie in LCS das Add-In "Steuerberechnung".
2. Richten Sie in RCS die Steuerberechnungsfunktion ein. Diese Einrichtung ist nicht für jede juristische Person spezifisch. Es kann von juristischen Personen in Finance und Supply Chain Management gemeinsam genutzt werden.
3. Richten Sie in Finance und Supply Chain Management die Steuerberechnungsparameter nach juristischer Person ein.

## <a name="high-level-design"></a>Allgemeines Design

### <a name="runtime-design"></a><a name="runtime"></a> Design zur Laufzeit

Die folgende Abbildung zeigt das allgemeine Laufzeit-Design einer Steuerberechnung. Da die Steuerberechnung in mehrere Dynamics 365-Apps integriert werden kann, verwendet die Abbildung die Integration mit Finance als Beispiel.

1. In Finance wird eine Transaktion erstellt, z. B. ein Kundenauftrag oder eine Bestellung.
2. Finance verwendet automatisch die Standardwerte der Mehrwertsteuergruppe und der Artikel-Mehrwertsteuergruppe.
3. Wenn die Schaltfläche **Mehrwertsteuer** auf der Transaktion ausgewählt wird, wird die Steuerberechnung ausgelöst. Finance sendet dann die Nutzlast an den Steuerberechnungsdienst.
4. Der Steuerberechnungsservice gleicht die Nutzlast mit vordefinierten Regeln in der Steuerfunktion ab, um gleichzeitig eine genauere Mehrwertsteuergruppe und Artikelumsatzsteuergruppe zu finden.

    - Wenn die Nutzlast mit der **Anwendbarkeit der Steuergruppe**-Matrix übereinstimmt, überschreibt sie den Mehrwertsteuergruppenwert mit dem übereinstimmenden Steuergruppenwert in der Anwendbarkeitsregel. Andernfalls wird weiterhin der Mehrwertsteuergruppenwert aus Finance verwendet.
    - Wenn die Nutzlast mit der **Element-Steuerkennzeichen-Anwendbarkeit**-Matrix übereinstimmt, überschreibt sie den Element-Mehrwertsteuergruppenwert mit dem übereinstimmenden Element-Steuergruppenwert in der Anwendbarkeitsregel. Andernfalls wird weiterhin der Element-Mehrwertsteuergruppenwert aus Finance verwendet.

5. Der Steuerberechnungsdienst legt die finalen Steuercodes über die Schnittmenge einer Mehrwertsteuergruppe und einer Element-Mehrwertsteuergruppe fest.
6. Der Steuerberechnungsdienst berechnet die Steuern basierend auf den endgültigen Steuercodes, die er ermittelt hat.
7. Der Steuerberechnungsdienst gibt das Steuerberechnungsergebnis an Finance zurück.

![Laufzeitdesign der Steuerberechnung.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Allgemeine Konfiguration

Die folgenden Schritte bieten einen allgemeinen Überblick über den Konfigurationsprozess für den Steuerberechnungsservice.

1. Installieren Sie im LCS-Projekt das Add-In **Steuerberechnung**.
2. Richten Sie in RCS die **Steuerberechnungsfunktion** ein.
3. Richten Sie in RCS die **Steuerberechnungsfunktion** ein:

    1. Wählen Sie die Steuerberechnungsversion aus.
    2. Erstellen Sie die Steuercodes.
    3. Erstellen Sie eine Steuergruppe.
    4. Eine Artikelsteuergruppe erstellen.
    5. Optional: Legen Sie eine Steuergruppenanwendbarkeit an, wenn Sie die standardmäßige Mehrwertsteuergruppe überschreiben möchten, die aus den Debitoren- oder Kreditorenstammdaten eingegeben wird.
    6. Optional: Legen Sie eine Artikelgruppenanwendbarkeit an, wenn Sie die standardmäßige Artikelsteuergruppe überschreiben möchten, die aus den Artikelstammdaten eingegeben wird.

4. Vervollständigen und veröffentlichen Sie die Funktion **Steuerberechnung** in RCS.
5. Wählen Sie in Finance die veröffentlichte Funktion **Steuerberechnung** aus.

Nachdem Sie diese Schritte ausgeführt haben, werden die folgenden Setups automatisch von RCS mit Finance synchronisiert.

- Mehrwertsteuercodes
- Mehrwertsteuergruppen
- Artikel-Mehrwertsteuergruppen

Die verbleibenden Themen enthalten zusätzliche Details zu den Konfigurationsschritten.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die verbleibenden Vorgehensweisen in diesem Thema abschließen können, müssen die folgenden Voraussetzungen erfüllt sein:<!--TO HERE-->

- Sie müssen Zugriff auf Ihr LCS-Konto haben, und Sie müssen ein LCS-Projekt bereitstellen, das über eine Umgebung der Stufe 2 oder höher verfügt, die Dynamics 365 Version 10.0.21 oder höher ausführt.
- Sie müssen eine RCS-Umgebung für Ihre Organisation erstellen und Sie müssen Zugriff auf Ihr Konto haben. Weitere Informationen über das Erstellen einer RCS-Umgebung finden Sie unter [Regulatory Configuration Service Übersicht](rcs-overview.md).
- Die folgenden Funktionen müssen im Arbeitsbereich **Funktionsverwaltung** Ihrer bereitgestellten Finance- oder Supply Chain Management-Umgebung aktiviert sein, je nach Ihren geschäftlichen Anforderungen:

    - Dienst für Steuerberechnungen
    - Mehrere MwSt.-Registrierungsnummern unterstützen
    - Steuer im Umlagerungsauftrag

- Die folgenden Funktionen müssen im Arbeitsbereich **Funktionsverwaltung** Ihrer bereitgestellten RCS Umgebung aktiviert sein.

    - Globalisierungsfunktionen

- Die folgenden Rollen sollten den Benutzer\*innen in Ihrer RCS-Umgebung entsprechend zugewiesen werden:

    - Entwickler für elektronische Berichterstellung
    - Entwickler der Globalisierungsfunktion
    - Steuermodul-Entwickler
    - Funktionaler Berater für Steuermodul
    - Steuerdienstentwickler

## <a name="set-up-tax-calculation-in-lcs"></a>Steuerberechnung in LCS einrichten

1. Bei [LCS](https://lcs.dynamics.com) anmelden
2. Schließen Sie die Einrichtung für die Microsoft Power Platform-Integration ab. Weitere Informationen finden Sie unter [Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Wählen Sie eine Ihrer bereitgestellten Umgebungen aus und wählen Sie dann **Ein neues Add-In installieren**.
4. Wählen Sie **Steuerberechnung**.
5. Lesen Sie die allgemeinen Geschäftsbedingungen, stimmen Sie ihnen zu und wählen Sie **Installieren** aus.

## <a name="set-up-tax-calculation-in-rcs"></a>Steuerberechnung in RCS einrichten

Die Schritte in diesem Abschnitt beziehen sich nicht auf eine bestimmte juristische Person. Sie müssen dieses Verfahren nur einmal ausführen und können es in jeder juristischen Person in RCS ausführen.

1. Melden Sie sich bei [RCS](https://marketing.configure.global.dynamics.com/) an.
2. Fügen Sie im Arbeitsbereich **Elektronische Berichterstattung** einen neuen Konfigurationsanbieter hinzu. Verwenden Sie Ihren Firmennamen als Namen des Anbieters. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Wählen Sie den Konfigurationsanbieter aus, den Sie gerade erstellt haben, und wählen Sie dann **Aktivieren** aus.
4. Wählen Sie den **Microsoft**-Konfigurationsanbieter und dann **Repositorys** aus.
5. Wählen Sie im Feld **Typ** **Global** aus.
6. Wählen Sie **Öffnen**.
7. Gehen Sie zu **Steuerdatenmodell**, erweitern Sie den Dateibaum und wählen Sie dann **Steuerkonfiguration** aus.
8. Wählen Sie die richtige [Steuerkonfigurationsversion](global-tax-calcuation-service-overview.md#versions), basierend auf Ihrer Finance-Version, und wählen Sie dann **Importieren**.
9. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** die Funktion **Funktionen**, wählen Sie die Kachel **Steuerberechnung** und wählen Sie dann **Hinzufügen**.
10. Wählen Sie eine der folgenden Funktionstypen aus:

    - **Neue Funktion** – Erstellen Sie eine Funktionseinrichtung mit leerem Inhalt.
    - **Auf vorhandener Funktion basierend** – Erstellen Sie eine Funktion aus einer vorhandenen Funktion und kopieren Sie den Inhalt aus der vorhandenen Funktionseinrichtung.

11. Geben Sie einen Namen und eine Beschreibung für die neue Funktion ein und wählen Sie **Funktion erstellen**.

    Nachdem die Funktion erstellt wurde, wird automatisch eine Entwurfsversion erstellt. Sie können **Diese Version abrufen** wählen, um die Entwurfsversion auf eine beliebige abgeschlossene Version zurückzusetzen.

12. Wählen Sie die Entwurfsversion der Funktion aus und wählen Sie dann **Bearbeiten**. Die Seite **Einrichtung der Steuerberechnung** wird ausgefüllt.
13. Wählen Sie **Konfigurationsversion**. Sie sollten die Konfigurationsversion sehen, die Sie in Schritt 8 importiert haben.

    Microsoft bietet eine Standardkonfiguration für die Steuerberechnung. Diese Konfiguration deckt die meisten Anforderungen für das Verhalten bei der Steuerberechnung ab. Es wird basierend auf Marktrückmeldungen aktualisiert. Wenn Sie die Konfiguration erweitern müssen, um bestimmte Anforderungen zu erfüllen, lesen Sie [So erstellen Sie eine Erweiterung im Steuerdienst](./tax-service-add-data-fields-tax-integration-by-extension.md) für Informationen zum Generieren und Auswählen Ihrer eigenen Steuerkonfiguration.

14. Nachdem Sie **Konfigurationsversion** gewählt haben, erscheinen mehrere zusätzliche Registerkarten. Folgen Sie der hier gezeigten Reihenfolge, um die Einrichtung der obligatorischen Registerkarten abzuschließen.

    **Pflichtige Einrichtung**

    - **Steuercodes** - Pflegen Sie die Stammdaten für Steuercodes. Alle Steuercodes, die auf dieser Registerkarte erstellt werden, werden automatisch mit Finance synchronisiert, wenn Sie die aktuelle Version aktivieren.
    - **Steuerkennzeichen** - Definieren Sie die Steuerkennzeichen-Stammdaten und die Steuerkennzeichen unter der Gruppe.
    - **Element-Steuerkennzeichen** - Definieren Sie die Artikel-Steuerkennzeichen-Stammdaten und die Steuerkennzeichen unter der Gruppe.

    **Optionale Einstellungen**

    - **Steuerkennzeichen Anwendbarkeit** - Definieren Sie eine Matrix, die das Steuerkennzeichen bestimmt. Wenn keine Anwendbarkeitsregeln in dieser Matrix mit dem steuerpflichtigen Beleg aus Dynamics 365 übereinstimmen, verwendet die Steuerberechnung den Standardwert in der Zeile des steuerpflichtigen Belegs.
    - **Element-Steuerkennzeichen-Anwendbarkeit** - Definieren Sie eine Matrix, die das Element-Steuerkennzeichen bestimmt. Wenn keine Anwendbarkeitsregeln in dieser Matrix mit dem steuerpflichtigen Beleg aus Dynamics 365 übereinstimmen, verwendet die Steuerberechnung den Standardwert in der Zeile des steuerpflichtigen Belegs.
    - **Anwendbarkeit der Steuerregistrierungsnummer des Debitors** - Wenn Sie mehrere Steuerregistrierungsnummern für einen Debitor haben, kann Tax Calculation automatisch die richtige Steuerregistrierungsnummer ermitteln. Definieren Sie in der Matrix auf dieser Registerkarte die Regeln, nach denen die Bestimmung erfolgen soll. Andernfalls verwenden Finance und Supply Chain Management weiterhin die Standardsteuerregistrierungsnummer für steuerpflichtige Dokumente für Verkaufstransaktionen.
    - **Anwendbarkeit der Steuerregistrierungsnummer des Kreditors** - Wenn Sie mehrere Steuerregistrierungsnummern für einen Kreditor haben, kann die Steuerberechnung automatisch die richtige Steuerregistrierungsnummer ermitteln. Definieren Sie in der Matrix auf dieser Registerkarte die Regeln, nach denen die Bestimmung erfolgen soll. Andernfalls verwenden Finance und Supply Chain Management weiterhin die Standardsteuerregistrierungsnummer für steuerpflichtige Dokumente für Kauftransaktionen.
    - **Listencode-Anwendbarkeit** - Bestimmen Sie automatisch den Wert des Feldes **Listencode** durch flexiblere und konfigurierbare Regeln. Definieren Sie in der Matrix auf dieser Registerkarte die Regeln, nach denen die Bestimmung erfolgen soll. Andernfalls verwenden Finance und Supply Chain Management weiterhin den Standardcode für steuerpflichtige Dokumente.

14. Wählen Sie auf der **Steuercode**-Registerkarte **Hinzufügen** aus, und geben Sie den Steuercode und eine Beschreibung ein.
15. Wählen Sie **Steuerkomponente** aus. Die Steuerkomponente ist eine Gruppe von Methoden, die in der vorherigen Version der ausgewählten Steuerkonfiguration definiert wurden. Folgende Steuerkomponenten sind verfügbar:

    - Nach Nettobetrag
    - Nach Bruttobetrag
    - Nach Menge
    - Nach Marge
    - Steuer auf Steuern

16. Wählen Sie **Speichern** aus. Je nach ausgewählter Steuerkomponente werden weitere Felder verfügbar.
17. Verwenden Sie die folgenden Optionen, um die Art des Steuercodes zu identifizieren:

    - Ist befreit
    - Ist Gebrauchsteuer
    - Ist Verlagerung der Steuerschuld
    - Von der Basisbetragsberechnung ausschließen

    Für ein Nutzungssteuerszenario legen Sie einen einzelnen Steuercode fest, der einen positiven Steuersatz hat, und markieren ihn als **Ist Nutzungssteuer**.

    Richten Sie für ein Steuerschuldumkehr-Szenario zwei Steuercodes ein, von denen eines einen positiven Steuersatz und das andere einen negativen Steuersatz bei gleichem Steuersatzwert aufweist. Markieren Sie den negativen Steuercode als **Ist Verlagerung der Steuerschuld**. Weitere Informationen zur Steuerschuldumkehr-Lösung in Finance finden Sie unter [Mechanismus zur Verlagerung der Steuerschuld für USt./GST-Regelung](emea-reverse-charge.md).

    Für einige Steuerarten, die von der Berechnung des Steuerbasisbetrags für Transaktionen inklusive Preis ausgeschlossen werden sollen (z.B. Zoll in einigen Ländern oder Regionen), markieren Sie das Kontrollkästchen **Aus der Basisbetragsberechnung ausschließen**. Weitere Informationen zu diesem Parameter finden Sie unter [Steuer zusätzlich zum Preis berechnen, wenn Preise inklusive Steuern aktiviert ist](global-exclude-from-tax-base-amount-calculation.md).

    Verwalten Sie die Steuersätze und die Steuerbetragsgrenzen für diesen Steuercode.

18. Wiederholen Sie Schritt 14 bis 17, um alle anderen Steuercodes, die Sie benötigen, hinzuzufügen.
19. Wählen Sie auf der Registerkarte **Steuerklasse** die Spalte **Steuerklasse** aus, fügen Sie sie als Eingabebedingung in die Matrix ein und fügen Sie dann Zeilen hinzu, um die Stammdaten der Steuerklasse zu pflegen.

    Hier ist ein Beispiel.

    | Steuergruppe    | Steuercodes           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. Wählen Sie auf der Registerkarte **Postensteuerkennzeichen** die Spalte **Postensteuerkennzeichen**, fügen Sie sie der Matrix als Eingabebedingung hinzu und fügen Sie dann Zeilen hinzu, um die Postensteuerkennzeichen-Stammdaten zu pflegen.

    Hier ist ein Beispiel.

    | Element-Steuerkennzeichen | Steuercodes                                    |
    | -------------- | -------------------------------------------- |
    | Vollständig           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Reduziert        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. Wählen Sie auf der Registerkarte **Steuerkennzeichen** die Spalten aus, die zur Bestimmung des richtigen Steuerkennzeichens erforderlich sind, und wählen Sie dann **Hinzufügen**. Geben Sie Werte für jede Spalte ein oder wählen Sie sie aus. Das Feld **Steuerkennzeichen** wird die Ausgabe dieser Matrix sein. Wenn diese Registerkarte nicht konfiguriert ist, wird die Mehrwertsteuergruppe in der Zeile der Transaktion verwendet.

    Hier ist ein Beispiel.

    | Geschäftsprozess | Lieferung von | Lieferung an | Steuergruppe    |
    | ---------------- | --------- | ------- | ------------ |
    | Verk.            | DEU       | DEU     | DEU_Domestic |
    | Verk.            | DEU       | FRA     | DEU_EU       |
    | Vertrieb            | BEL       | BEL     | BEL_Domestic |
    | Vertrieb            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Wenn die Standard-Mehrwertsteuergruppe in Ihren steuerpflichtigen Belegzeilen korrekt ist, lassen Sie diese Matrix leer. Weitere Informationen finden Sie im Abschnitt [Design zur Laufzeit](#runtime) in diesem Thema.

22. Wählen Sie auf der Registerkarte **Anwendbarkeit des Steuerkennzeichens** die Spalten aus, die zur Bestimmung des richtigen Steuerkennzeichens erforderlich sind, und wählen Sie dann **Hinzufügen**. Geben Sie Werte für jede Spalte ein oder wählen Sie sie aus. Das Feld **Element Steuerkennzeichen** wird die Ausgabe dieser Matrix sein. Wenn diese Registerkarte nicht konfiguriert ist, wird die Mehrwertsteuergruppe des Elements in der Zeile der Transaktion verwendet.

    Hier ist ein Beispiel.

    | Artikelcode | Artikelsteuergruppe |
    | --------- | -------------- |
    | D0001     | Vollständig           |
    | D0003     | Reduziert        |

    > [!NOTE]
    > Wenn die standardmäßige Artikel-Mehrwertsteuergruppe in Ihren steuerpflichtigen Belegzeilen korrekt ist, lassen Sie diese Matrix leer. Weitere Informationen finden Sie im Abschnitt [Design zur Laufzeit](#runtime) in diesem Thema.

    Weitere Informationen darüber, wie Steuerkennzeichen in der Steuerberechnung ermittelt werden, finden Sie unter [Ermittlungslogik für Mehrwertsteuergruppen und Artikelsteuerkennzeichen](global-sales-tax-group-determination.md).

23. Legen Sie die Anwendbarkeit von Debitor-Steuerregistrierungsnummern, Kreditor-Steuerregistrierungsnummern und Listencodes basierend auf den Geschäftsanforderungen fest.
24. Klicken Sie auf **Speichern** und schließen Sie die Seite.
25. Wählen Sie **Status ändern** \> **Abgeschlossen**. Nachdem der Status in **Abgeschlossen** geändert wurde, kann die Version nicht mehr bearbeitet werden.
26. Wählen Sie **Status ändern** \> **Veröffentlichen** aus. Diese Version der Steuerfunktionseinrichtung wird in das globale Repository übertragen und ist für jede juristische Person in Finance sichtbar.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Einrichten der Steuerberechnung in Dynamics 365

Nachdem Sie die Einrichtung in RCS abgeschlossen haben, verfügen Sie über eine veröffentlichte Version der Steuerfunktion. Führen Sie die folgenden Schritte aus, um die Steuerberechnung in Finance einzurichten.

Die Einrichtung in diesem Abschnitt erfolgt nach juristischer Person. Sie müssen sie für jede juristische Person konfigurieren, für die Sie die Steuerberechnung in Finance aktivieren möchten.

1. Gehen Sie in Finance auf **Steuern** \> **Einrichtung** \> **Steuerkonfiguration** \> **Steuerberechnungsparameter**.
2. Legen Sie auf der Registerkarte **Allgemein** die folgenden Felder fest:

    - **Steuerberechnungsdienst aktivieren** - Aktivieren Sie dieses Kontrollkästchen, um die Steuerberechnung für die juristische Entität zu aktivieren. Wenn es für die aktuelle juristische Person nicht aktiviert ist, verwendet die juristische Person weiterhin das vorhandene Steuermodul, um die Steuer zu ermitteln und zu berechnen.
    - **Funktionseinrichtung** – Wählen Sie eine veröffentlichte Steuerfunktionseinrichtung und Version für die juristische Person aus. Weitere Informationen zum Einrichten und Vervollständigen einer veröffentlichten Steuerfunktion finden Sie im vorherigen Abschnitt dieses Themas.
    - **Geschäftsprozess** – Wählen Sie die zu aktivierenden Geschäftsprozesse aus.

3. Definieren Sie auf der Registerkarte **Berechnung** die erwartete Rundungsregel für die juristische Person. Weitere Informationen über die Rundungslogik finden Sie unter [Steuerberechnungs-Rundungsregeln](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Definieren Sie auf der Registerkarte **Fehlerbehandlung** die erwartete Fehlerbehandlungsmethode für die juristische Person. Es stehen drei Optionen zur Verfügung:

    - Nein
    - Achtung
    - Fehler

    Sie können für jeden Ergebniscode im Abschnitt **Details** eine Fehlerbehandlungsmethode festlegen. Alternativ, wenn einige Ergebniscodes nicht vom Steuerberechnungsdienst synchronisiert werden, können Sie im Abschnitt **Allgemein** eine Standardmethode festlegen.

5. Auf der Registerkarte **Mehrfache MwSt.-Registrierung** können Sie MwSt.-Erklärung, EU-Verkaufsliste und Intrastat separat einschalten, um unter einem Szenario mit mehreren MwSt.-Registrierungen zu arbeiten. Weitere Informationen über Steuerberichte für mehrere MwSt.-Registrierungen finden Sie unter [Berichterstattung für mehrere MwSt.-Registrierungen](emea-reporting-for-multiple-vat-registrations.md).
6. Speichern Sie die Einrichtung und wiederholen Sie die vorherigen Schritte für jede zusätzliche juristische Entität. Wenn eine neue Version veröffentlicht wird und Sie möchten, dass sie angewendet wird, legen Sie das Feld **Einrichtung der Funktion** auf der Registerkarte **Allgemein** der Seite **Steuerberechnungsparameter** fest (siehe Schritt 2).
