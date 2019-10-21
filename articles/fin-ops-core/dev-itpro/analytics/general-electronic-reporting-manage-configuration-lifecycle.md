---
title: Den Konfigurationslebenszyklus der elektronischen Berichterstellung (EB) verwalten
description: In diesem Thema wird beschrieben, wie Sie den Lebenszyklus von Konfigurationen für die elektronische Berichterstellung (EB) für die Microsoft Dynamics 365 Finance-Lösung verwalten.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6206b3a1ac298af98e4b69b6800b9a493658c4ea
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181288"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Den Konfigurationslebenszyklus der elektronischen Berichterstellung (EB) verwalten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie den Lebenszyklus von Konfigurationen für die elektronische Berichterstellung (EB) für die Microsoft Dynamics 365 Finance-Lösung verwalten.

## <a name="overview"></a>Übersicht

Die elektronische Berichterstellung (EB) ist ein Modul, das gesetzlich vorgeschriebene und länderspezifische elektronische Dokumente  unterstützt. Im Allgemeinen setzt ER die Möglichkeit der Ausführung der folgenden Aufgaben für ein einzelnes elektronisches Dokument voraus. Genauere Informationen finden Sie in der [Berichterstellungsüberblick](general-electronic-reporting.md).

- Entwerfen einer Vorlage für ein elektronisches Dokument:

    - Identifizieren Sie die erforderlichen Datenquellen, die in diesem Dokument angezeigt werden können.

        - Zugrundeliegende Daten (Datentabellen, Datenentitäten usw.)
        - Prozessspezifische Eigenschaften (Ausführungsdatum und Zeit, Zeitzone)
        - Benutzereingabeparameter (definiert nach Endbenutzer bei Laufzeit).

    - Definieren der erforderlichen Dokumentelemente sowie ihrer Topologie, um das Format des endgültigen Dokuments anzugeben;
    - Konfiguration des gewünschten Datenflusses von ausgewählten Datenquellen in definierten Dokumentelementen über Datenquellenbindungen zu den Dokumentformatkomponenten und Definition der Prozesssteuerungslogik.

- Erstellen einer Vorlage zur Verwendung in anderen Instanzen:

    - Umwandeln einer Dokumentvorlage, die in einer ER-Konfiguration erstellt wurde, und Exportieren der Konfiguration aus der aktuellen Anwendungsinstanz als XML-Paket, das entweder lokal oder in LCS gespeichert werden kann.
    - Umwandeln einer ER-Konfiguration in eine Anwendungsdokumentvorlage.
    - Importieren eines XML-Pakets, das entweder lokal oder in LCS in die aktuelle Instanz gespeichert wird.

- Anpassen einer Vorlage eines elektronischen Dokuments:

    - Verschieben einer Vorlage von LCS zur aktuellen Instanz als ER-Konfiguration:
    - Entwerfen Sie eine benutzerdefinierte Version einer ER-Konfiguration und behalten Sie eine Referenz zur Basisversion.

- Integriert eine Vorlage mit einem bestimmten Geschäftsprozess, so das er in der Anwendung verfügbar ist:

    - Konfigurieren der Anwendungseinstellungen, damit eine ER-Konfiguration verwendet werden kann, indem Sie auf diese Konfiguration in einem prozessbezogenen Parameter verweisen. (Wenn Sie z. B. auf die ER-Konfiguration in einer bestimmten Kreditorenkonten-Zahlungsmethode zur Generierung einer elektronischen Zahlungsnachricht zur Verarbeitung von Rechnungen verweisen.)

- Verwenden einer Vorlage in einem bestimmten Geschäftsprozess:

    - Ausführen einer bestimmten ER-Konfiguration in einem Geschäftsprozess aus. (Wenn Sie z. B. auf die ER-Konfiguration in einer bestimmten Kreditorenkonten-Zahlungsmethode zur Generierung einer elektronischen Zahlungsnachricht zur Verarbeitung von Rechnungen verweisen.)

## <a name="concepts"></a>Konzepte
Folgende Rollen und Aktivitäten gehören zu ER-Konfigurationslebenszyklen.

| Rolle                                       | Aktivitäten                                                      | Beschreibung |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Funktionaler Berater für elektronische Berichterstellung | Erstellen und Verwalten von ER-Komponenten (Modelle und Formate).           | Eine Mitarbeiter, der domänenspezifische ER-Datenmodelle gestaltet, entwirft die erforderlichen Vorlagen für elektronische Dokumente und bindet sie entsprechend. |
| Entwickler für elektronische Berichterstellung             | Erstellen und Verwalten von Datenmodellzuordnungen.                          | Ein Spezialist, der die erforderlichen Finanzdatenquellen auswählt und sie an domänenspezifische ER-Datenmodelle bindet |
| Supervisor Buchhaltung                      | Konfiguration von prozessbezogenen Einstellungen, die auf ER-Artefakte verweisen. | Zum Beispiele eine Rolle **Supervisor Buchhaltung**, die die Einstellungen einer ER-Konfiguration in einer bestimmten Kreditorenzahlungsmethode zulässt, um eine elektronische Zahlung zur Verarbeitung von Rechnungen zu generieren |
| Sachbearbeiter Kreditorenkontozahlungen            | Verwenden von ER-Artefakten in einem bestimmten Geschäftsprozess.                | Beispielsweise eine **Sachbearbeiter Kreditorenkontozahlungen**-Rolle, die die für die Generierung von Nachrichten für elektronischen Zahlung zulässt, die auf dem ER-Format basieren, das für eine bestimmte Zahlungsmethode konfiguriert ist |

## <a name="er-configuration-development-lifecycle"></a>Er-Konfigurationsentwicklungslebenszyklus
Bei den folgenden ER-bezogenen Gründen empfehlen wir, Ihre ER-Konfigurationen in der Entwicklungsumgebung als getrennte Instanz von Finance and Operations zu entwickeln:

- Benutzer, die entweder die Rolle des **Elektronischen Berichterstellungsentwicklers** oder **des funktionalen Beraters der elektronischen Berichterstellung** ausüben, können Konfigurationen bearbeiten und anschließend für Testzwecke ausführen. Dieses Szenario ruft möglicherweise Geschäftsabläufe und Tabellen auf, die für die Daten und die Leistung der Instanz schädlich sein können.
- Das Aufrufen von Geschäftsabläufen und Tabellen als ER Datenquelle von ER Konfigurationen sind bei Einstiegspunkten und angemeldeten Unternehmensinhalten nicht beschränkt. Deshalb können Benutzer mit der Rolle **Entwickler für elektronische Berichterstellung** oder **Funktionaler Berater für elektronische Berichterstellung** auf geschäftskritische Daten zugreifen.

ER-Konfigurationen, die in der Testumgebung entworfene wurden, können in die Testumgebung hochgeladen werden, um eine Konfigurationsauswertung (korrekte Prozessintegration, Korrektheit der Ergebnisse, Leistung) vorzunehmen und das Qualitätsmanagement (Korrektheit der Rollen getriebener Zugriffsrechts, Aufgabentrennung, usw.) sicherzustellen. Die Funktionen, die den ER-Konfigurationsaustausch ermöglichen, können zu diesem Zweck verwendet werden. Nachgewiesene ER-Konfigurationen können außerdem entweder zu LCS hochgeladen werden (dort können Sie mit Dienstleistungsabonnenten geteilt werden).

![ER-Konfiguration Lebenszyklus](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
