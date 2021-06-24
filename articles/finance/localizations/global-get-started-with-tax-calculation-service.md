---
title: Erste Schritte mit der Steuerberechnung
description: In diesem Thema wird erläutert, wie Steuerberechnungen eingerichtet werden.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e72b81d4a109db2dd8b4c6ca2ca0b030220e25f3
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216718"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Erste Schritte mit der Steuerberechnung (Vorschau)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dieses Thema enthält Informationen zu den ersten Schritten mit der Steuerberechnung. Zunächst werden Sie durch die Konfigurationsschritte in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) und Dynamics 365 Finance sowie Dynamics 365 Supply Chain Management geführt. Anschließend wird der allgemeine Prozess für die Verwendung der Steuerberechnungsfunktion für Transaktionen in Finance und Supply Chain Management überprüft.

Die Einrichtung besteht aus vier Hauptschritten:

1. Installieren Sie in LCS die Steuerberechnung.
2. Richten Sie in RCS die Steuerberechnungsfunktion ein. Diese Einrichtung ist nicht für jede juristische Person spezifisch. Es kann von juristischen Personen in Finance und Supply Chain Management gemeinsam genutzt werden.
3. Richten Sie in Finance und Supply Chain Management die Steuerberechnungsparameter nach juristischer Person ein.
4. Erstellen Sie in Finance und Supply Chain Management Transaktionen wie Aufträge und verwenden Sie die Steuerberechnung, um Steuern zu ermitteln und zu berechnen.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Vorgehensweisen in diesem Thema abschließen können, müssen die folgenden Voraussetzungen erfüllt sein:

- Sie haben Zugriff auf Ihr LCS-Konto und haben ein LCS-Projekt mit einer Tier 2-Umgebung (oder höher) bereitgestellt, in der Dynamics 365 Version 10.0.18 mit [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) oder höher ausgeführt wird.
- Sie haben Zugriff auf Ihr RCS-Konto.
- Sie haben Microsoft kontaktiert, um das Flighting in Ihrer bereitgestellten Finance- oder Supply Chain Management-Umgebung zu aktivieren.

## <a name="set-up-tax-calculation-in-lcs"></a>Steuerberechnung in LCS einrichten

1. Bei [LCS](https://lcs.dynamics.com) anmelden
2. Schließen Sie die Einrichtung für die Microsoft Power Platform-Integration ab. Weitere Informationen finden Sie unter [Übersicht über Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Wählen Sie eine Ihrer bereitgestellten Nichtproduktionsumgebungen aus und wählen Sie dann **Neues Add-In installieren**.
4. Wählen Sie **Steuerberechnung (Vorschau)**.
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
8. Wählen Sie die neueste Version aus und wählen Sie dann **Importieren**.
9. Gehen Sie zurück zum Arbeitsbereich **Globalisierungsfunktionen (Vorschau)**, wählen Sie **Funktionen** aus, wählen Sie die Kachel **Steuerberechnung** und dann **Hinzufügen** aus.
10. Wählen Sie eine der folgenden Funktionstypen aus:

    - **Neue Funktion** – Erstellen Sie eine Funktionseinrichtung mit leerem Inhalt.
    - **Auf vorhandener Funktion basierend** – Erstellen Sie eine Funktion aus einer vorhandenen Funktion und kopieren Sie den Inhalt aus der vorhandenen Funktionseinrichtung.

11. Geben Sie einen Namen und eine Beschreibung für die neue Funktion ein und wählen Sie **Funktion erstellen**.

    Nachdem die Funktion erstellt wurde, wird automatisch eine Entwurfsversion erstellt.

12. Wählen Sie die Entwurfsversion der Funktion aus und wählen Sie dann **Bearbeiten**. Die Seite **Einrichtung der Steuerberechnung** wird ausgefüllt.
13. Wählen Sie **Konfigurationsversion**. Sie sollten die Konfigurationsversion sehen, die Sie in Schritt 8 importiert haben.

    Microsoft bietet eine Standardsteuerkonfiguration für das Steuerberechnungs-Add-In. Diese Konfiguration deckt die meisten Anforderungen für das Verhalten bei der Steuerberechnung ab. Es wird basierend auf Marktrückmeldungen aktualisiert. Wenn Sie die Konfiguration erweitern müssen, um bestimmte Anforderungen zu erfüllen, lesen Sie [So erstellen Sie eine Erweiterung im Steuerdienst](./tax-service-add-data-fields-tax-integration-by-extension.md) für Informationen zum Generieren und Auswählen Ihrer eigenen Steuerkonfiguration.

    Nachdem Sie **Konfigurationsversion** ausgewählt haben, werden mehrere zusätzliche Registerkarten angezeigt:

    - **Steuercode** – Diese Registerkarte ist obligatorisch. Sie wird verwendet, um Masterdaten für Steuercodes zu pflegen. Alle Steuercodes, die auf dieser Registerkarte erstellt werden, werden automatisch mit Finance synchronisiert, wenn Sie die aktuelle Version der Steuerfunktionseinrichtung in der juristischen Person aktivieren.
    - **Anwendbarkeit von Steuercodes** – Diese Registerkarte ist obligatorisch. Sie wird verwendet, um eine Matrix zu definieren, die den Steuercode, die Steuergruppe und die Artikelsteuergruppe bestimmt. Der ermittelte Steuercode wird zur Berechnung des Steuerbetrags verwendet. Die Werte der Felder **Steuercode**, **Steuergruppe** und **Artikelsteuergruppe** werden an Finance zurückgegeben.
    - **Anwendbarkeit der Debitor-Steuerregistrierungsnummer** – Diese Registerkarte ist optional. Wenn Sie mehrere Steuerregistrierungsnummern für einen Debitor haben, kann die Steuerberechnung automatisch die richtige Steuerregistrierungsnummer ermitteln. In der Matrix auf dieser Registerkarte definieren Sie die Regeln, nach denen die Bestimmung vorgenommen wird. Andernfalls verwenden Finance und Supply Chain Management weiterhin die Standardsteuerregistrierungsnummer für steuerpflichtige Dokumente für Verkaufstransaktionen.
    - **Anwendbarkeit der Kreditoren-Steuerregistrierungsnummer** – Diese Registerkarte ist optional. Wenn Sie mehrere Steuerregistrierungsnummern für einen Lieferanten haben, kann die Steuerberechnung automatisch die richtige Steuerregistrierungsnummer ermitteln. In der Matrix auf dieser Registerkarte definieren Sie die Regeln, nach denen die Bestimmung vorgenommen wird. Andernfalls verwenden Finance und Supply Chain Management weiterhin die Standardsteuerregistrierungsnummer für steuerpflichtige Dokumente für Kauftransaktionen.
    - **Anwendbarkeit des Listencodes** – Diese Registerkarte ist optional. Es kann helfen, den Wert im Feld **Listencode** durch flexiblere und konfigurierbare Regeln automatisch zu bestimmen. In der Matrix auf dieser Registerkarte können Sie die Regeln definieren, nach denen die Bestimmung vorgenommen wird. Andernfalls verwenden Finance und Supply Chain Management weiterhin den Standardcode für steuerpflichtige Dokumente.

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
    - Ist Verbrauchssteuer (USA)
    - Ist Verlagerung der Steuerschuld
    - Von der Basisbetragsberechnung ausschließen

    Richten Sie für ein Verbrauchssteuer (USA)-Szenario einen einzelnen Steuercode mit einem positiven Steuersatz ein und markieren Sie es als **Ist Verbrauchssteuer (USA)**.

    Richten Sie für ein Steuerschuldumkehr-Szenario zwei Steuercodes ein, von denen eines einen positiven Steuersatz und das andere einen negativen Steuersatz bei gleichem Steuersatzwert aufweist. Markieren Sie den negativen Steuercode als **Ist Verlagerung der Steuerschuld**. Weitere Informationen zur Steuerschuldumkehr-Lösung in Finance finden Sie unter [Mechanismus zur Verlagerung der Steuerschuld für USt./GST-Regelung](emea-reverse-charge.md).
    
    Wählen Sie für einige Steuertypen, die bei der Berechnung des Steuerbasisbetrags für preisbezogene Transaktionen ausgeschlossen werden sollten, wie z. B. Zoll in einigen Ländern, das Kontrollkästchen **Von der Basisbetragsberechnung ausschließen** aus.

    Verwalten Sie die Steuersätze und die Steuerbetragsgrenzen für diesen Steuercode.

18. Wiederholen Sie Schritt 14 bis 17, um alle anderen Steuercodes, die Sie benötigen, hinzuzufügen.
19. Wählen Sie auf der Registerkarte **Anwendbarkeit von Steuercodes** die Spalten aus, die zur Ermittlung des richtigen Steuercodes erforderlich sind, und wählen Sie dann **Hinzufügen** aus.
20. Geben Sie Werte für jede Spalte ein oder wählen Sie sie aus. Die Felder **Steuercode**, **Steuergruppe** und **Artikelsteuergruppe** werden in der Matrix ausgegeben.
21. Wiederholen Sie die Schritte 19 bis 20, um die Anwendbarkeit von Debitor-Steuerregistrierungsnummern, Kreditor-Steuerregistrierungsnummern und Listencodes festzulegen.
22. Klicken Sie auf **Speichern** und schließen Sie die Seite.
23. Wählen Sie **Status ändern** \> **Abgeschlossen**. Nachdem der Status in **Abgeschlossen** geändert wurde, kann die Version nicht mehr bearbeitet werden.
24. Wählen Sie **Status ändern** \> **Veröffentlichen** aus. Diese Version der Steuerfunktionseinrichtung wird in das globale Repository übertragen und ist für jede juristische Person in Finance sichtbar.

## <a name="dynamics-365-setup"></a>Dynamics 365-Einrichtung

Nachdem Sie die Einrichtung in RCS abgeschlossen haben, wie im vorherigen Abschnitt beschrieben, haben Sie eine veröffentlichte Version der Steuerfunktion. Führen Sie die folgenden Schritte aus, um die Steuerberechnung in Finance einzurichten.

Die Einrichtung in diesem Abschnitt erfolgt nach juristischer Person. Sie müssen sie für jede juristische Person konfigurieren, für die Sie die Steuerberechnung in Finance aktivieren möchten.

1. Gehen Sie in Finance zu **Steuer** \> **Einrichtung** \> **Steuerkonfiguration** \> **Steuerberechnung einrichten (Vorschau)**.
2. Legen Sie auf der Registerkarte **Allgemein** die folgenden Felder fest:

    - **Steuerberechnung aktivieren** – Aktivieren Sie dieses Kontrollkästchen, um die Steuerberechnung für die juristische Person zu aktivieren. Wenn es für die aktuelle juristische Person nicht aktiviert ist, verwendet die juristische Person weiterhin das vorhandene Steuermodul, um die Steuer zu ermitteln und zu berechnen.
    - **Funktionseinrichtung** – Wählen Sie eine veröffentlichte Steuerfunktionseinrichtung und Version für die juristische Person aus. Weitere Informationen zum Einrichten und Vervollständigen einer veröffentlichten Steuerfunktion finden Sie im vorherigen Abschnitt dieses Themas.
    - **Geschäftsprozess** – Wählen Sie die zu aktivierenden Geschäftsprozesse aus.
    - **Anpassung des Steuerkennzeichens aktivieren** – Setzen Sie diese Option auf **Ja**, um Steuercodeanpassungen auf der Mehrwertsteuerseite zu aktivieren.

3. Definieren Sie auf der Registerkarte **Berechnung** die erwartete Rundungsregel für die juristische Person.
4. Definieren Sie auf der Registerkarte **Fehlerbehandlung** die erwartete Fehlerbehandlungsmethode für die juristische Person. Für jeden Ergebniscode stehen drei Optionen zur Verfügung:

    - Nr.
    - Achtung
    - Fehler

5. Speichern Sie die Einrichtung.
6. Wiederholen Sie die Schritte 1 bis 5 für jede weitere juristische Person.

## <a name="transaction-processing"></a>Verarbeiten von Buchungen

Nachdem Sie alle Einrichtungsvorgänge abgeschlossen haben, können Sie die Steuerberechnung verwenden, um die Steuer in Finance zu ermitteln und zu berechnen. Die Schritte zur Verarbeitung von Transaktionen bleiben unverändert. Die folgenden Transaktionen werden in Finance Version 10.0.18 unterstützt:

- Verkaufsprozess

    - Verkaufsangebot
    - Auftrag
    - Bestätigung
    - Kommissionierliste
    - Lieferschein
    - Verkaufsrechnung
    - Gutschrift
    - Rücklieferung
    - Kopfgebühr
    - Positionsgebühr

- Kaufprozess

    - Bestellung
    - Bestätigung
    - Zugangsliste
    - Produktzugang
    - Einkaufsrechnung
    - Kopfgebühr
    - Positionsgebühr
    - Gutschrift
    - Rücklieferung
    - Bestellanforderung
    - Belastung pro Bestellanforderungsposition
    - Angebotsanforderung
    - Kopfgebühr für Angebotsanforderung
    - Belastung pro Angebotsanforderungsposition

- Bestandsprozess

    - Umlagerungsauftrag – versenden
    - Umlagerungsauftrag – empfangen
