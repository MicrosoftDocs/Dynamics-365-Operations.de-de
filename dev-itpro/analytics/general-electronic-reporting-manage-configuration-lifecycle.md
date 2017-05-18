---
title: Verwalten des Lebenszyklus der elektronischen Berichterstellung
description: "In diesem Artikel wird beschrieben, wie Sie den Lebenszyklus von ER-Konfigurationen für die Microsoft Dynamics 365 for Operations-Lösung verwalten."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c6779f22699cbdb1a3ad1debd173c82a38d0f847
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Verwalten des Lebenszyklus der elektronischen Berichterstellung

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie Sie den Lebenszyklus von ER-Konfigurationen für die Microsoft Dynamics 365 for Operations-Lösung verwalten.

<a name="overview"></a>Überblick
--------

Die elektronische Berichterstellung (ER) ist ein Modul, das gesetzlich vorgeschriebene und länderspezifische elektronische Dokumente in Microsoft Dynamics 365 for Operations unterstützt. Im Allgemeinen setzt ER die Möglichkeit der Ausführung der folgenden Aufgaben für ein einzelnes elektronisches Dokument voraus. Genauere Informationen finden Sie in der [Berichterstellungsüberblick](general-electronic-reporting.md).

-   Entwerfen einer Vorlage für ein elektronisches Dokument:
    -   Identifizieren Sie die erforderlichen Datenquellen, die in diesem Dokument angezeigt werden können.
        -   Zugrundeliegende Dynamics 365 for Operations-Daten (Datentabellen, Datenentitäten usw.)
        -   Prozessspezifische Eigenschaften (Ausführungsdatum und Zeit, Zeitzone)
        -   Benutzereingabeparameter (definiert nach Endbenutzer bei Laufzeit).
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
    -   Konfigurieren von Dynamics 365 for Operations-Einstellungen, damit eine ER-Konfiguration verwendet werden kann, indem Sie auf diese Konfiguration in einem prozessbezogenen Parameter verweisen. (Wenn Sie z. B. auf die ER-Konfiguration in einer bestimmten Kreditorenkonten-Zahlungsmethode zur Generierung einer elektronischen Zahlungsnachricht zur Verarbeitung von Rechnungen verweisen.)
-   Verwenden einer Vorlage in einem bestimmten Geschäftsprozess:
    -   Ausführen einer bestimmten ER-Konfiguration in einem Geschäftsprozess aus. (Wenn Sie z. B. auf die ER-Konfiguration in einer bestimmten Kreditorenkonten-Zahlungsmethode zur Generierung einer elektronischen Zahlungsnachricht zur Verarbeitung von Rechnungen verweisen.)

## <a name="concepts"></a>Konzepte
Folgende Rollen und Aktivitäten gehören zu ER-Konfigurationslebenszyklen.

| Rolle                                       | Aktivitäten                                                      | Beschreibung                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionaler Berater für elektronische Berichterstellung | Erstellen und Verwalten von ER-Komponenten (Modelle und Formate).           | Eine Mitarbeiter, der domänenspezifische ER-Datenmodelle gestaltet, entwirft die erforderlichen Vorlagen für elektronische Dokumente und bindet sie entsprechend.                                                                           |
| Entwickler für elektronische Berichterstellung             | Erstellen und Verwalten von Datenmodellzuordnungen.                          | Ein Dynamics 365 for Operations-Spezialist, der die erforderlichen Dynamics 365 for Operations-Datenquellen auswählt und sie an domänenspezifische ER-Datenmodelle bindet                                                                 |
| Supervisor Buchhaltung                      | Konfiguration von prozessbezogenen Einstellungen, die auf ER-Artefakte verweisen. | Zum Beispiele eine Rolle **Supervisor Buchhaltung**, die die Einstellungen einer ER-Konfiguration in einer bestimmten Kreditorenzahlungsmethode zulässt, um eine elektronische Zahlung zur Verarbeitung von Rechnungen zu generieren |
| Sachbearbeiter Kreditorenkontozahlungen            | Verwenden von ER-Artefakten in einem bestimmten Geschäftsprozess.                | Beispielsweise eine **Sachbearbeiter Kreditorenkontozahlungen**-Rolle, die die für die Generierung von Nachrichten für elektronischen Zahlung zulässt, die auf dem ER-Format basieren, das für eine bestimmte Zahlungsmethode konfiguriert ist           |

## <a name="er-configuration-development-lifecycle"></a>Er-Konfigurationsentwicklungslebenszyklus
Bei den folgenden ER-bezogenen Gründen empfehlen wir, Ihre ER-Konfigurationen in der Entwicklungsumgebung als getrennte Instanz von Dynamics 365 for Operations zu entwickeln:

-   Benutzer, die entweder die Rolle des **Elektronischen Berichterstellungsentwicklers** oder **des funktionalen Beraters der elektronischen Berichterstellung** ausüben, können Konfigurationen bearbeiten und anschließend für Testzwecke ausführen. Dieses Szenario ruft möglicherweise Geschäftsabläufe und Tabellen auf, die für die Daten und die Leistung der Dynamicx 365 for Operations-Instanz schädlich sein können.
-   Das Aufrufen von Geschäftsabläufen und Tabellen als ER Datenquelle von ER Konfigurationen sind bei Dynamics 365 for Operations-Einstiegspunkten und angemeldeten Unternehmensinhalten nicht beschränkt. Deshalb können Benutzer mit der Rolle **Entwickler für elektronische Berichterstellung** oder **Funktionaler Berater für elektronische Berichterstellung** auf geschäftskritische Daten zugreifen.

ER-Konfigurationen, die in der Testumgebung entworfene wurden, können in die Testumgebung hochgeladen werden, um eine Konfigurationsauswertung (korrekte Prozessintegration, Korrektheit der Ergebnisse, Leistung) vorzunehmen und das Qualitätsmanagement (Korrektheit der Rollen getriebener Zugriffsrechts, Aufgabentrennung, usw.) sicherzustellen. Die Funktionen, die den ER-Konfigurationsaustausch ermöglichen, können zu diesem Zweck verwendet werden. Nachgewiesene ER-Konfigurationen können außerdem entweder zu LCS hochgeladen werden (dort können Sie mit Dienstleistungsabonnenten geteilt werden). ![ER-Konfiguration Lebenszyklus](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Siehe auch
--------

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)




