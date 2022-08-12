---
title: Commerce Scale Unit (Cloud) initialisieren
description: Diese Artikel erklärt, wie Sie die Commerce Scale Unit (Cloud) in Microsoft Dynamics 365 Commerce initialisieren.
author: jashanno
ms.date: 07/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 93fbf2893fecc7b731f946797907bce4f8448309
ms.sourcegitcommit: 8032d6275e6d9994ef9759ee16e743b483f7689e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183362"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Unit (Cloud) initialisieren

[!include[banner](../includes/banner.md)]

Diese Artikel erklärt, wie Sie die Commerce Scale Unit (Cloud) in Microsoft Dynamics 365 Commerce initialisieren.

Wenn Sie eine Tier-2 Sandbox- oder Produktionsumgebung mit der Anwendungsversion 8.1.2.x oder höher verwenden, müssen Sie die Commerce Scale Unit (Cloud) initialisieren, bevor Sie die Funktionalität des Einzelhandelskanals entweder für Point of Sale (POS) Vorgänge oder für E-Commerce Vorgänge, die Retail Server in der Cloud verwenden, nutzen können. Bei der Initialisierung wird eine Commerce Scale Unit (Cloud) bereitgestellt.

> [!IMPORTANT]
> Für bestehende Debitor, die die Einzelhandelskanäle in der Cloud nutzen, verlangen wir, dass Sie Ihre Einzelhandelskanäle auf die Verwendung von Commerce Scale Unit aktualisieren, um eine kontinuierliche und ununterbrochene Unterstützung für Ihr Unternehmen sicherzustellen. Neue Umgebungen, die ohne Commerce Scale Unit bereitgestellt werden, erhalten keine Qualitäts- und Service-Updates mehr für in der Cloud gehostete Einzelhandelskanal-Komponenten. Für Debitor, die ausschließlich Commerce Scale Unit (self-hosted) verwenden, besteht kein Handlungsbedarf. Wenden Sie sich an Ihren Microsoft FastTrack Solution Architect, wenn Sie eine Erweiterung benötigen.

## <a name="prerequisites"></a>Voraussetzungen

1. Stellen Sie eine Tier-2 Sandbox- oder Produktionsumgebung mit der Version 8.1.2.x oder höher bereit.
2. Sie können bis zu 2 Commerce Scale Uniten pro Umgebung selbst bereitstellen. Wenn Sie mehr als 2 Commerce Scale Units pro Umgebung benötigen, erstellen Sie in Microsoft Dynamics Lifecycle Services (LCS) eine Support-Anfrage und geben Sie **Anfrage für zusätzliche Commerce Scale Unit** ein und geben Sie die Umgebungs-ID, die Anzahl der Commerce Scale Units und die gewünschten Rechenzentrumsregionen an. Die Anfrage wird innerhalb von fünf Geschäftstagen abgeschlossen. Wenn Sie nicht mehr als 2 Commerce Scale Units pro Umgebung benötigen, brauchen Sie keine Support-Anfrage zu erstellen. 
3. Sie müssen über die Berechtigungen des Projektbesitzers in Lifecycle Services verfügen, bevor Sie Commerce Scale Unit initialisieren können.
4. Stellen Sie sicher, dass die Konfigurationsschlüssel für Einzelhandelslizenzen in Ihrer Umgebung aktiviert sind. Weitere Informationen finden Sie unter [Lizenzcodes und Konfigurationsschlüssel Bericht](../sysadmin/license-codes-configuration-keys-report.md). Sie müssen die folgenden Schlüssel aktiviert haben, um Commerce Scale Unit zu verwenden.

    - RetailBasic
    - RetaileCommerce - Wenn Sie planen, E-Commerce für Dynamics 365 Commerce zu verwenden.
    - RetailGiftCard - Wenn Sie vorhaben, Geschenkkarten zu verwenden.
    - RetailInvent - Wenn Sie vorhaben, Bestand zu verwenden.
    - RetailModernPos - Wenn Sie beabsichtigen, Point of Sale (POS) zu verwenden.
    - RetailReplenishment - Wenn Sie planen, Wiederbeschaffungen zu verwenden.
    - RetailScheduler
    - RetailStores - Wenn Sie vorhaben, POS zu verwenden.


## <a name="region-availability"></a>Regionale Verfügbarkeit
Die Commerce Scale Unit steht in den folgenden Regionen zum Bereitstellen zur Verfügung.

| Globaler Standort | Region              | Verfügbarkeit        | Kommentare                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERICAS        | USA, Osten             | Allgemein verfügbar |  Keine Kommentare.                         |
| AMERICAS        | USA, Osten 2           | Allgemein verfügbar |  Keine Kommentare.                          |
| AMERICAS        | USA, Norden-Mitte    | Begrenzte Kapazität    |  Keine Kommentare.                            |
| AMERICAS        | USA, Süden-Mitte    | Begrenzte Kapazität    |  Keine Kommentare.                            |
| AMERICAS        | USA, Mitte          | Allgemein verfügbar |  Keine Kommentare.                            |
| AMERICAS        | USA, Westen             | Allgemein verfügbar |  Keine Kommentare.                            |
| AMERICAS        | USA, Westen 2           | Allgemein verfügbar |  Keine Kommentare.                            |
| AMERICAS        | Kanada, Mitte      | Begrenzte Kapazität    |  Keine Kommentare.                            |
| AMERICAS        | Kanada, Osten         | Begrenzte Kapazität    |   Keine Kommentare.                           |
| AMERICAS        | USA, Westen-Mitte     | Begrenzte Kapazität    |   Keine Kommentare.                           |
| APAC            | Australien, Osten      | Allgemein verfügbar |   Keine Kommentare.                           |
| APAC            | Asien, Südosten      | Kapazität eingeschränkt | Keine Bereitstellungen zugelassen.    |
| APAC            | Japan, Osten          | Allgemein verfügbar |  Keine Kommentare.                            |
| APAC            | Japan, Westen          | Allgemein verfügbar |   Keine Kommentare.                           |
| APAC            | Australien, Südosten | Allgemein verfügbar |   Keine Kommentare.                           |
| APAC            | Asien, Osten           | Begrenzte Kapazität    |   Keine Kommentare.                           |
| APAC            | Indien Süd         | Kapazität eingeschränkt | Keine Bereitstellungen zugelassen.    |
| APAC            | Indien Zentral       | Begrenzte Kapazität    | Erfordert einen Genehmigungsprozess. |
| EMEA            | Europa, Westen         | Begrenzte Kapazität    | Zur Zeit nicht in LCS verfügbar. |
| EMEA            | Europa, Norden        | Begrenzte Kapazität    | Zur Zeit nicht in LCS verfügbar. |
| EMEA            | Vereinigtes Königreich (United Kingdom), Süden            | Allgemein verfügbar |    Keine Kommentare.                          |
| EMEA            | Vereinigtes Königreich (United Kingdom), Westen             | Allgemein verfügbar |    Keine Kommentare.                          |
| Schweiz     | Schweiz, Norden   | Begrenzte Kapazität    | Erfordert einen Genehmigungsprozess. |
| VAE             | VAE, Norden           | Begrenzte Kapazität    | Erfordert einen Genehmigungsprozess. |

Die Bereitstellungskapazität in Regionen mit begrenzter Kapazität ist extrem eingeschränkt. Anträge auf Bereitstellen werden von Fall zu Fall geprüft. Wenn Sie einen zwingenden geschäftlichen Bedarf für die Bereitstellung in Regionen mit begrenzter Kapazität haben, können Sie eine Supportanfrage stellen, um auf die Warteliste gesetzt zu werden. Bereiche mit eingeschränkter Kapazität erlauben derzeit keine Bereitstellung von Commerce Scale Units. 

![Karte mit der Verfügbarkeit der Region](media/Commerce-Scale-Unit-Region-Availability.png "Zuordnung der Verfügbarkeit von Regionen").

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Initialisieren Sie die Commerce Scale Unit als Teil der Bereitstellung einer neuen Umgebung

Bitte stellen Sie sicher, dass die Zentralverwaltung verfügbar ist. Dies ist erforderlich, um die Scale-Unit bei der Zentralverwaltung während des Initialisierungsprozesses zu registrieren. Es wird nicht empfohlen, eine Scale-Unit zu initialisieren, wenn die Zentralverwaltung gewartet wird, da sie während des Wartungsprozesses nicht mehr verfügbar sein könnte.

1. Stellen Sie sicher, dass die Umgebung der Zentralverwaltung verfügbar ist und sich nicht im [Wartungsmodus](../sysadmin/maintenance-mode.md) befindet.
2. Wählen Sie in LCS auf der Seite mit den Umgebungsdetails **Umgebungsfunktionen \> Commerce**.
3. Wählen Sie auf der Seite Commerce Einrichtung bereitstellen **Initialisieren**.
4. Wählen Sie die Version der Commerce Scale Unit, die initialisiert werden soll.
5. Wählen Sie eine Region, in der die Commerce Scale Unit initialisiert werden soll.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigurieren Sie die Channels für die Verwendung der Commerce Scale Unit

Nachdem die Commerce Scale Unit bereitgestellt wurde, müssen Sie sicherstellen, dass Ihre Kanäle so konfiguriert sind, dass sie die Datenbank für diese Einheit verwenden. 

Um Ihre Kanäle für die Verwendung der Commerce Scale Unit-Datenbank zu konfigurieren, gehen Sie wie folgt vor.

1. Gehen Sie in der Commerce-Zentralverwaltung zu **Handel und commerce \> Einrichtung der Zentrale \> Commerce Scheduler \> Channel-Datenbank**.
1. Wählen Sie im linken Fensterbereich eine Channel-Datenbank aus.
1. Wählen Sie auf der Registerkarte **Einzelhandelskanal** die Option **Hinzufügen** und wählen Sie dann Ihren Einzelhandelskanal in der Dropdown-Liste aus.
1. Wählen Sie **Hinzufügen** und wählen Sie dann Ihren Online-Kanal in der Dropdown-Liste. 

Wenn Sie fertig sind, gehen Sie zu **Einzelhandel und Commerce \> Einzelhandel und Commerce IT \> Verteilungsplan** und führen Sie den Auftrag 9999 aus.

> [!NOTE] 
> Auftrag 9999 synchronisiert alle neuen Produkte und Debitoren mit der Commerce Scale Unit. Dieser Prozess kann sehr lange dauern. Wenn der Channel nur für die E-Commerce Site Builder-Konfiguration zur Verfügung stehen soll, können Sie Job 1070 anstelle von Job 9999 ausführen.

### <a name="database-refresh-and-commerce-scale-units"></a>Datenbankaktualisierung und Commerce Scale Units

Bevor Sie beginnen, stellen Sie sicher, dass Sie mit den [Schritten nach einer Datenbankaktualisierung für Umgebungen, die Commerce-Funktionen verwenden](../database/database-refresh.md), vertraut sind.

Die Datensätze der Scale-Unit-Kanaldatenbank (im Formular Kanaldatenbank) können im Rahmen einer Datenbankaktualisierung nicht zwischen Umgebungen verschoben werden. Der Grund dafür ist, dass die Datensätze eine umgebungsspezifische Konfiguration darstellen.

Nach der Aktualisierung der Datenbank können Sie den Datensatz der Scale-Unit in der Kanaldatenbank neu generieren, indem Sie Ihre Scale-Unit in LCS neu bereitstellen. Bei jedem Vorgang zum Bereitstellen oder Warten der Scale-Unit wird versucht, die Scale-Unit bei der Zentrale zu registrieren, wenn die Registrierung als fehlend erkannt wird.

Sie können eine erneute Bereitstellung der Scale-Unit veranlassen, ohne Komponenten zu ändern, indem Sie die gleiche Version bereitstellen, in der sich Ihre Scale-Unit bereits befindet. Dies kann in LCS durch die folgenden Schritte erreicht werden:

1. Wählen Sie in LCS auf der Seite mit den Umgebungsdetails **Umgebungsfunktionen \> Einzelhandel**.
2. Wählen Sie auf der Seite Einrichtung bereitstellen die Scale-Einheit aus, die Sie neu bereitstellen möchten.
3. Wählen Sie im Menü des Vorgangs der Scale-Unit **Aktualisieren**.
4. Kommissionieren Sie auf dem Schieberegler im Dropdown-Menü unter **Version auswählen** die Option **Version festlegen**.
5. Geben Sie in das Textfeld unter **Version angeben** die für Ihre Scale-Einheit angezeigte Version ein, die neben dem Label **Aktuelle Version** angezeigt wird.
6. Klicken Sie auf die Schaltfläche **Aktualisieren**.

Sie brauchen **Erweiterungen aktualisieren** nicht zu wählen, selbst wenn Sie zuvor Erweiterungen angewendet haben, da das zuletzt auf die Scale-Unit angewendete Erweiterungspaket automatisch kommissioniert wird, wenn Sie eine Scale-Unit aktualisieren.

Wenn Sie mehrere Scale-Einheiten haben, müssen Sie den obigen Vorgang für jede Scale-Einheit durchführen. Wenn Sie möchten, können Sie diese Vorgänge parallel durchführen.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Bereitstellen zusätzlicher Commerce Scale Units (optional)

Nachdem Sie die Commerce Scale Unit initialisiert haben, können Sie selbst eine zweite Scale-Unit bereitstellen, wenn Ihre Lizenz Sie dazu berechtigt. Um mehr als zwei Scale-Units bereitzustellen, müssen Sie eine Support-Anfrage erstellen. Geben Sie in der Support-Anfrage die Anzahl der von Ihnen benötigten Commerce Scale Units, den Namen der Umgebung und die gewünschten Regionen an. Weitere Informationen zur Lizenzierung finden Sie unter [Dynamics 365 Anleitung zur Lizenzierung](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Wir empfehlen Ihnen, für jede zusätzliche Commerce Scale Unit, die Sie bereitstellen, eine eigene Channel-Datenbankgruppe zu erstellen. Gehen Sie dazu wie folgt vor.

1. Gehen Sie in der Commerce-Zentrale zu **Einzelhandel und Commerce > Retail Headquarters > Einrichtung des Retail Schedulers > Channel-Datenbankgruppe**.
2. Erstellen Sie eine neue Kanaldatenbankgruppe.
3. Gehen Sie auf die Seite **Retail und Commerce > Retail Headquarters > Retail Scheduler Einrichtung > Kanaldatenbank**, und wählen Sie die Kanaldatenbank aus, die der neu erstellten Commerce Scale Unit entspricht.
4. Wählen Sie **Bearbeiten** und wählen Sie die neue Channel-Datenbankgruppe.
5. Wählen Sie **Speichern** aus.
6. Wählen Sie **Vollständige Datensynchronisation ausführen** für die ausgewählte Channel-Datenbank.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Zusätzliche Überlegungen, wenn Sie die in der Cloud gehosteten Commerce Channel-Komponenten in einer bestehenden Umgebung initialisieren

Wenn Sie bereits Cloud-gehostete Commerce-Channel-Komponenten in einer Umgebung verwenden, trägt die Initialisierung von Commerce Scale Unit dazu bei, die Ausfallzeiten zu reduzieren, wenn diese Komponenten aktualisiert werden. Vor der Initialisierung der Commerce Scale Unit ist eine zusätzliche Planung erforderlich.

Wenn Sie Ihre erste Commerce Scale Unit in einer Umgebung initialisieren, die in der Cloud gehostete Commerce Channel-Komponenten verwendet, migriert der Initialisierungsprozess Ihre Channels, die mit den in der Cloud gehosteten Channel-Komponenten verbunden sind, zur ersten Scale-Unit. Kanäle, die mit Store Scale-Einheiten verbunden sind, sind davon nicht betroffen.

Der Migrationsprozess ist für die Kanäle transparent. Nach dem Start der Scale-Unit-Initialisierung werden die folgenden Vorgänge automatisch ausgeführt:

1. Eine neue Commerce Scale Unit wird erstellt und mit der Umgebung verknüpft.
2. Die Scale-Unit von Commerce wird in der Zentralverwaltung als verfügbare Channel-Datenbank registriert.
3. Alle Kanäle, die der **Standard** Kanaldatenbank in der Zentrale zugeordnet sind, werden aktualisiert, um der neuen Commerce Scale Unit zugeordnet zu werden.
4. Eine Commerce Data Exchange (CDX) vollständige Datensynchronisation wird durchgeführt, um die Kanaldaten in die neue Scale-Unit zu bringen.

**Planen und Testen der Initialisierung von Commerce Scale Units** Allgemein müssen Sie bei der Initialisierung von Commerce Scale Units ein fünfstündiges Ausfallzeitfenster für Vorgänge im Store sowie für alle E-Commerce-Kanalvorgänge einplanen, die Retail Server oder Cloud Point of Sale verwenden.

1. Führen Sie eine Datenbankaktualisierung von Ihrer Produktionsumgebung in eine Sandbox-Umgebung (UAT-Umgebung) durch. 
2. Initialisieren Sie die Commerce Scale Unit in der Sandbox-Umgebung (UAT). 
3. Beachten Sie die Initialisierungszeit für die Commerce Scale Unit. Dies ist vergleichbar mit der Zeit, die dieser Vorgang in Ihrer Produktionsumgebung in Anspruch nimmt, während der die Store- und E-Commerce-Vorgänge nicht verfügbar sind.

Vor der Initialisierung von Commerce Scale Unit müssen Sie die folgenden zusätzlichen Schritte durchführen.

- **Alle POS-Schichten schließen** - Nach der Migration können POS-Benutzer keine Schichten schließen, die während des Migrationsprozesses aktiv waren.
- **Prüfen Sie, ob alle P-Aufträge erfolgreich abgeschlossen wurden** - Es wird empfohlen, dass die P-Aufträge zur Synchronisierung ausstehender Transaktionen abgeschlossen sind, bevor die CSU initialisiert wird.
- **Abmelden von allen POS-Geräten** - POS-Vorgänge werden während der Migration nicht unterstützt.
- **Alle ausgesetzten Transaktionen an der Kasse zurückrufen und stornieren** - Ausgesetzte Transaktionen werden nicht als Teil der Initialisierung erhalten.

> [!IMPORTANT]
> Im Rahmen der Initialisierung der Commerce Scale Unit gehen zuvor angehaltene Transaktionen verloren und können nicht wiederhergestellt werden. 

Hier sehen Sie, was während des Initialisierungszeitraums passiert:

- In der Cloud gehostete Commerce-Kanäle funktionieren nicht, es sei denn, Sie schalten die Funktionalitäten von Cloud POS offline ein.
- POS-Geräte mit aktivierter Offline-Funktionalität haben eine eingeschränkte Funktionalität.
- Alle E-Commerce Clients, die von Retail Server abhängig sind, werden unterbrochen.
- Kanäle, die auf Commerce Scale Units gehostet werden (selbst gehostet), sind nicht betroffen.
- Die Funktionalität des Head Office ist davon nicht betroffen.

Hier sehen Sie, was nach Abschluss der Initialisierung geschieht:

- Der Status der Geräteaktivierung aller aktivierten POS-Geräte bleibt erhalten, was bedeutet, dass die Geräte nicht erneut aktiviert werden müssen.
- Eigenständige Hardware-Stationsinstanzen funktionieren weiterhin.
- POS-Kanal-seitige Berichte werden zurückgesetzt und zeigen keine Daten von vor der Initialisierung an.
- Der Vorgang „Journal anzeigen“ wird ebenfalls zurückgesetzt und zeigt keine Daten von vor der Initialisierung an.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
