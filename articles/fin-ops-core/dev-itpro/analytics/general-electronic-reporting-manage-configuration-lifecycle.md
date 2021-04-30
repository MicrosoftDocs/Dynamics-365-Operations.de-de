---
title: Den Konfigurationslebenszyklus der elektronischen Berichterstellung (EB) verwalten
description: In diesem Thema wird beschrieben, wie Sie den Lebenszyklus von Konfigurationen für die elektronische Berichterstellung (EB) für Dynamics 365 Finance verwalten.
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52aba53b5323a9c6c4331cd8de7e932bb9c3547e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893200"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Den Lebenszyklus der elektronischen Berichterstellungskonfiguration (ER) verwalten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie den Lebenszyklus von Konfigurationen für die elektronische Berichterstellung (EB) für Dynamics 365 Finance verwalten.

## <a name="overview"></a>Übersicht

Die elektronische Berichterstellung (EB) ist ein Modul, das gesetzlich vorgeschriebene und länderspezifische elektronische Dokumente unterstützt. Im Allgemeinen setzt ER die Möglichkeit der Ausführung der folgenden Aufgaben für ein einzelnes elektronisches Dokument voraus. Weitere Informationen finden Sie unter [Elektronisches Berichtswesen (ER) Übersicht](general-electronic-reporting.md).

- Entwerfen einer Vorlage für ein elektronisches Dokument:

    - Identifizieren Sie die erforderlichen Datenquellen, die in diesem Dokument angezeigt werden können.

        - Zugrundeliegende Daten (Datentabellen, Datenentitäten usw.)
        - Prozessspezifische Eigenschaften (Ausführungsdatum und Zeit, Zeitzone)
        - Benutzereingabeparameter (definiert nach Endbenutzer bei Laufzeit).

    - Definieren der erforderlichen Dokumentelemente sowie ihrer Topologie, um das Format des endgültigen Dokuments anzugeben;
    - Konfiguration des gewünschten Datenflusses von ausgewählten Datenquellen in definierten Dokumentelementen über Datenquellenbindungen zu den Dokumentformatkomponenten und Definition der Prozesssteuerungslogik.

- Erstellen einer Vorlage zur Verwendung in anderen Instanzen:

    - Umwandeln einer Dokumentvorlage, die in einer EB-Konfiguration erstellt wurde, und Exportieren der Konfiguration aus der aktuellen Anwendungsinstanz als XML-Paket, das entweder lokal oder in Lifecycle Services (LCS) gespeichert werden kann.
    - Umwandeln einer EB-Konfiguration in eine Anwendungsdokumentvorlage.
    - Importieren eines XML-Pakets, das entweder lokal oder in LCS in die aktuelle Instanz gespeichert wird.

- Anpassen einer Vorlage eines elektronischen Dokuments:

    - Verschieben einer Vorlage von LCS zur aktuellen Instanz als EB-Konfiguration:
    - Entwerfen Sie eine benutzerdefinierte Version einer EB-Konfiguration und behalten Sie eine Referenz zur Basisversion.

- Integriert eine Vorlage mit einem bestimmten Geschäftsprozess, so das er in der Anwendung verfügbar ist:

    - Konfigurieren der Anwendungseinstellungen, damit eine EB-Konfiguration verwendet werden kann, indem Sie auf diese Konfiguration in einem prozessbezogenen Parameter verweisen. (Wenn Sie z. B. auf die EB-Konfiguration in einer bestimmten Kreditorenkonten-Zahlungsmethode zur Generierung einer elektronischen Zahlungsnachricht zur Verarbeitung von Rechnungen verweisen.)

- Verwenden einer Vorlage in einem bestimmten Geschäftsprozess:

    - Ausführen einer bestimmten EB-Konfiguration in einem Geschäftsprozess aus. (Wenn Sie z. B. auf die EB-Konfiguration in einer bestimmten Kreditorenkonten-Zahlungsmethode zur Generierung einer elektronischen Zahlungsnachricht zur Verarbeitung von Rechnungen verweisen.)

## <a name="concepts"></a>Konzepte
Folgende Rollen und Aktivitäten gehören zu EB-Konfigurationslebenszyklen.

| Rolle                                       | Aktivitäten                                                      | Beschreibung |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Funktionaler Berater für elektronische Berichterstellung | Erstellen und Verwalten von EB-Komponenten (Modelle und Formate).           | Eine Mitarbeiter, der domänenspezifische EB-Datenmodelle gestaltet, entwirft die erforderlichen Vorlagen für elektronische Dokumente und bindet sie entsprechend. |
| Entwickler für elektronische Berichterstellung             | Erstellen und Verwalten von Datenmodellzuordnungen.                          | Ein Spezialist, der die erforderlichen Finanzdatenquellen auswählt und sie an domänenspezifische EB-Datenmodelle bindet |
| Supervisor Buchhaltung                      | Konfiguration von prozessbezogenen Einstellungen, die auf EB-Artefakte verweisen. | Zum Beispiele eine Rolle **Supervisor Buchhaltung**, die die Einstellungen einer EB-Konfiguration in einer bestimmten Kreditorenzahlungsmethode zulässt, um eine elektronische Zahlung zur Verarbeitung von Rechnungen zu generieren |
| Sachbearbeiter Kreditorenkontozahlungen            | Verwenden von EB-Artefakten in einem bestimmten Geschäftsprozess.                | Beispielsweise eine **Sachbearbeiter Kreditorenkontozahlungen**-Rolle, die die für die Generierung von Nachrichten für elektronischen Zahlung zulässt, die auf dem EB-Format basieren, das für eine bestimmte Zahlungsmethode konfiguriert ist |

## <a name="er-configuration-development-lifecycle"></a>EB-Konfigurationsentwicklungslebenszyklus
Bei den folgenden EB-bezogenen Gründen empfehlen wir, Ihre EB-Konfigurationen in der Entwicklungsumgebung als getrennte Instanz von Finance and Operations zu entwickeln:

- Benutzer, die entweder die Rolle des **Elektronischen Berichterstellungsentwicklers** oder **des funktionalen Beraters der elektronischen Berichterstellung** ausüben, können Konfigurationen bearbeiten und anschließend für Testzwecke ausführen. Dieses Szenario ruft möglicherweise Geschäftsabläufe und Tabellen auf, die für die Daten und die Leistung der Instanz schädlich sein können.
- Das Aufrufen von Geschäftsabläufen und Tabellen als EB-Datenquelle von EB-Konfigurationen sind bei Einstiegspunkten und angemeldeten Unternehmensinhalten nicht beschränkt. Deshalb können Benutzer mit der Rolle **Entwickler für elektronische Berichterstellung** oder **Funktionaler Berater für elektronische Berichterstellung** auf geschäftskritische Daten zugreifen.

EB-Konfigurationen, die in der Testumgebung entworfene wurden, können in die Testumgebung [hochgeladen](#data-persistence-consideration) werden, um eine Konfigurationsauswertung (korrekte Prozessintegration, Korrektheit der Ergebnisse, Leistung) vorzunehmen und das Qualitätsmanagement (Korrektheit der Rollen getriebener Zugriffsrechts, Aufgabentrennung usw.) sicherzustellen. Die Funktionen, die den EB-Konfigurationsaustausch ermöglichen, können zu diesem Zweck verwendet werden. Nachgewiesene EB-Konfigurationen können außerdem entweder zu LCS hochgeladen werden, um sie mit Dienstabonnenten zu teilen, oder in die Produktionsumgebung für den internen Gebrauch [importiert](#data-persistence-consideration) werden.

![EB-Konfiguration Lebenszyklus](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><a name="data-persistence-consideration" />Berücksichtigung der Datenpersistenz

Sie können verschiedene [Versionen](general-electronic-reporting.md#component-versioning) einer EB-[Konfiguration](general-electronic-reporting.md#Configuration) einzeln in Ihre Instanz von Finance [importieren](tasks/er-import-configuration-lifecycle-services.md). Wenn eine neue Version einer EB-Konfiguration importiert wird, steuert das System den Inhalt der Entwurfsversion dieser Konfiguration:

   - Wenn die importierte Version niedriger als die höchste Version dieser Konfiguration in der aktuellen Instanz von Finance ist, bleibt der Inhalt der Entwurfsversion dieser Konfiguration unverändert.
   - Wenn die importierte Version höher ist als jede andere Version dieser Konfiguration in der aktuellen Instanz von Finance, wird der Inhalt der importierten Version in die Entwurfsversion dieser Konfiguration kopiert, damit Sie die letzte abgeschlossene Version weiter bearbeiten können.

Wenn diese Konfiguration dem [Konfigurationsanbieter](general-electronic-reporting.md#Provider) gehört, der derzeit aktiviert ist, ist die Entwurfsversion dieser Konfiguration für Sie im Inforegister **Versionen** der Seite **Konfigurationen** (**Organisationsverwaltung** > **Elektronische Berichterstattung** > **Konfigurationen**) sichtbar. Sie können die Entwurfsversion der Konfiguration auswählen und ihren Inhalt unter Verwendung des entsprechenden EB-Designers [ändern](er-quick-start2-customize-report.md#ConfigureDerivedFormat). Wenn die Entwurfsversion einer EB-Konfiguration bearbeitet haben, passt ihr Inhalt nicht mehr zur höchsten VErsion dieser Konfiguration in der aktuellen Instanz von Finance. Um den Verlust Ihrer Änderungen zu verhindern, zeigt das System einen Fehler an, dass der Import nicht fortgesetzt werden kann, da die Version dieser Konfiguration höher ist als die höchste Version dieser Konfiguration in der aktuellen Instanz von Finance. Wenn dies zum Beispiel bei der Formatkonfiguration **X** passiert, wird der Fehler **Format-„X“-Version nicht abgeschlossen** angezeigt.

Um die Änderungen rückgängig zu machen, die Sie in der Entwurfsversion vorgenommen haben, wählen Sie die höchste abgeschlossene oder freigegebene Version Ihrer EB-Konfiguration in Finance auf dem Inforegister **Versionen** und dann die Option **Diese Version abrufen** aus. Der Inhalt der ausgewählten Version wird in die Entwurfsversion kopiert.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (EB)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
