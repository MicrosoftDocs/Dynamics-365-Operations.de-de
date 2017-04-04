---
title: Verwalten des Lebenszyklus der elektronischen Berichterstellung
description: "In diesem Thema wird beschrieben, wie Sie den Lebenszyklus elektronischer meldenden (ER)- Konfigurationen für das Microsoft Dynamics 365 für Arbeitsgangslösung verwaltet."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Verwalten des Lebenszyklus der elektronischen Berichterstellung

In diesem Thema wird beschrieben, wie Sie den Lebenszyklus elektronischer meldenden (ER)- Konfigurationen für das Microsoft Dynamics 365 für Arbeitsgangslösung verwaltet.

<a name="overview"></a>Überblick
--------

Die elektronische Berichterstellung (ER) ist ein Modul, das gesetzlich vorgeschriebene und länderspezifische elektronische Dokumente in Microsoft Dynamics 365 for Operations unterstützt. Im Allgemeinen setzt ER die Möglichkeit der Ausführung der folgenden Aufgaben für ein einzelnes elektronisches Dokument voraus. Genauere Informationen finden Sie in der Berichterstellungsüberblick []( general-electronic-reporting.md).

-   Entwerfen einer Vorlage für ein elektronisches Dokument:
    -   Identifizieren Sie die erforderlichen Datenquellen, die in diesem Dokument angezeigt werden können.
        -   Dynamics 365 für Arbeitsgangsdaten, wie Datenentitäten Datentabellen, Klassen und zugrunde liegen.
        -   Prozess-Besondereeigenschaften, z Ausführungsdatum und Zeit und Zeitzone.
        -   Benutzereingabeparameter, zur Bearbeitungszeit die vom Endbenutzer.
    -   Definieren der erforderlichen Dokumentelemente sowie ihrer Topologie, um das Format des endgültigen Dokuments anzugeben;
    -   Konfiguration des gewünschten Datenflusses von ausgewählten Datenquellen in definierten Dokumentelementen über Datenquellenbindungen zu den Dokumentformatkomponenten und Definition der Prozesssteuerungslogik.
-   Erstellen einer Vorlage zur Verwerdnung in anderen Dynamics 365 for Operations-Instanzen:
    -   Umwandeln einer Dokumentvorlage, die in Dynamics 365 for Operations in einer ER-Konfiguration erstellt wurde, und Exportieren der Konfiguration aus der aktuellen Dynamics 365 for Operations-Instanz als XML-Paket, das entweder lokal oder in LCS gespeichert werden kann.
    -   Umwandeln einer ER-Konfiguration in eine Dynamics 365 for Operations-Dokumentvorlage.
    -   Importieren eines XML-Pakets, das entweder lokal oder in LCS in die aktuelle Dynamics 365 for Operations-Instanz gespeichert wird.
-   Anpassen einer Vorlage eines elektronischen Dokuments:
    -   Verschieben einer Vorlage von LCS zur aktuellen Dynamics 365 for Operations Instanz als ER-Konfiguration:
    -   Entwerfen Sie eine benutzerdefinierte Version einer ER-Konfiguration und behalten Sie eine Referenz zur Basisversion.
-   Integriert eine Vorlage mit einem bestimmten Geschäftsprozess, so das er in Dynamics 365 for Operations verfügbar ist:
    -   Konfigurieren von Dynamics 365 for Operations-Einstellungen, damit eine ER-Konfiguration verwendet werden kann, indem Sie auf diese Konfiguration in einem prozessbezogenen Parameter verweisen. Beispiel finden Sie die ER-Konfiguration in zu einer Zahlungsmethode der definierten Konten an, wenn Sie eine Meldung für elektronische Zahlung zur Verarbeitung von Rechnungen zu generieren.
-   Verwenden einer Vorlage in einem bestimmten Geschäftsprozess:
    -   Ausführen einer bestimmten ER-Konfiguration in einem Geschäftsprozess aus. Sie können eine Nachricht der elektronischen Zahlung zur Verarbeitung von Rechnungen generieren, wenn eine Zahlungsmethode, die die ER-Konfiguration verweist, ausgewählt wird.

## <a name="concepts"></a>Konzepte
Folgende Rollen und zugehörige Aktivitäten werden mit dem ER-Konfigurationslebenszyklus zugeordnet.

| Rolle                                       | Aktivitäten                                                      | Beschreibung                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionaler Berater für elektronische Berichterstellung | Erstellen und Verwalten von ER-Komponenten (Modelle und Formate).           | Eine Geschäftsperson, die domänenspezifische Datenmodelle, die erforderlichen ER entwirft Vorlagen für elektronische Dokumente entwirft und nach bindet.                                                                           |
| Entwickler für elektronische Berichterstellung             | Erstellen und Verwalten von Datenmodellzuordnungen.                          | Dynamics 365 für Arbeitsgangsspezialisten, die das erforderliche Dynamics 365 für Arbeitsgangsdatenquellen auswählen und sie zu domänenspezifischen Datenmodellen ER bindet.                                                                 |
| Supervisor Buchhaltung                      | Konfiguration von prozessbezogenen Einstellungen, die auf ER-Artefakte verweisen. | Beispiel einer Buchhaltungssupervisor ** ** Rolle, die die Einstellungen einer, um eine Nachricht in ermöglicht Kreditorenzahlungsmethode einer bestimmten verwendet werden ER-Konfiguration, " Elektronische Zahlung zur Verarbeitung von Rechnungen zu generieren. |
| Sachbearbeiter Kreditorenkontozahlungen            | Verwenden von ER-Artefakten in einem bestimmten Geschäftsprozess.                | Beispielsweise eine ** Kreditorenzahlungen werden als Angestellter tätig ** Rolle, die für die Verarbeitung können generiert werden Meldungen der elektronischen Zahlung, Rechnungen, basierend auf dem ER-Format, das für eine bestimmte Zahlungsmethode konfiguriert wird.           |

## <a name="er-configuration-development-lifecycle"></a>Er-Konfigurationsentwicklungslebenszyklus
Bei den folgenden ER-bezogenen Gründen empfehlen wir, Ihre ER-Konfigurationen in der Entwicklungsumgebung als getrennte Instanz von Dynamics 365 for Operations zu entwickeln:

-   Benutzer, die entweder die Rolle des **Elektronischen Berichterstellungsentwicklers** oder **des funktionalen Beraters der elektronischen Berichterstellung** ausüben, können Konfigurationen bearbeiten und anschließend für Testzwecke ausführen. Dieses Szenario ruft möglicherweise Geschäftsabläufe und Tabellen auf, die für die Daten und die Leistung der Dynamicx 365 for Operations-Instanz schädlich sein können.
-   Das Aufrufen von Geschäftsabläufen und Tabellen als ER Datenquelle von ER Konfigurationen sind bei Dynamics 365 for Operations-Einstiegspunkten und angemeldeten Unternehmensinhalten nicht beschränkt. Deshalb können Benutzer mit der Rolle **Entwickler für elektronische Berichterstellung** oder **Funktionaler Berater für elektronische Berichterstellung** auf geschäftskritische Daten zugreifen.

Er-Konfigurationen, die in der Entwicklungsumgebung vorgesehen sind, können der Testumgebung (Konfigurationsbewertung für die korrekte Prozeßintegration, Korrektheit Ergebnissen und Leistung) und die Qualitätssicherung, wie von Rolle-getriebenen Korrektheit Zugriffsrechten und der Aufgabentrennung hochgeladen werden. Die Funktionen, die ER-Konfigurationsaustausch aktivieren, können für diesen Zweck verwendet werden. Schließlich können ER-Konfigurationen nachgewiesene hochgeladene jede zu Kreditbriefen, in dem sie mit Service-Abonnenten freigegeben werden kann, z oder Produktionsumgebung für interne Verwendung vorgesehen sein, z angezeigt wurden in der folgenden Abbildung. ![Er-Konfigurationslebenszyklus](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Siehe auch
--------

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)


