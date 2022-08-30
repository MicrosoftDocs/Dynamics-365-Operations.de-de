---
title: Den Lebenszyklus der elektronischen Berichterstellungskonfiguration (ER) verwalten
description: In diesem Artikel wird beschrieben, wie Sie den Lebenszyklus von Konfigurationen für die elektronische Berichterstellung (EB) für Dynamics 365 Finance verwalten.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337194"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Den Lebenszyklus der elektronischen Berichterstellungskonfiguration (ER) verwalten

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie den Lebenszyklus von [Konfigurationen](general-electronic-reporting.md#Configuration) für die [elektronische Berichterstellung](general-electronic-reporting.md) (EB) für Dynamics 365 Finance verwalten.

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
Aus den folgenden Gründen, die mit ER zusammenhängen, empfehlen wir Ihnen, ER-Konfigurationen in der Entwicklungsumgebung zu entwerfen, und zwar als separate Instanz von Finanzen und Betrieb:

- Benutzer, die entweder die Rolle des **Elektronischen Berichterstellungsentwicklers** oder **des funktionalen Beraters der elektronischen Berichterstellung** ausüben, können Konfigurationen bearbeiten und anschließend für Testzwecke ausführen. Dieses Szenario ruft möglicherweise Geschäftsabläufe und Tabellen auf, die für die Daten und die Leistung der Instanz schädlich sein können.
- Das Aufrufen von Geschäftsabläufen und Tabellen als EB-Datenquelle von EB-Konfigurationen sind bei Einstiegspunkten und angemeldeten Unternehmensinhalten nicht beschränkt. Deshalb können Benutzer mit der Rolle **Entwickler für elektronische Berichterstellung** oder **Funktionaler Berater für elektronische Berichterstellung** auf geschäftskritische Daten zugreifen.

EB-Konfigurationen, die in der Testumgebung entworfene wurden, können in die Testumgebung [hochgeladen](#data-persistence-consideration) werden, um eine Konfigurationsauswertung (korrekte Prozessintegration, Korrektheit der Ergebnisse, Leistung) vorzunehmen und das Qualitätsmanagement (Korrektheit der Rollen getriebener Zugriffsrechts, Aufgabentrennung usw.) sicherzustellen. Die Funktionen, die den EB-Konfigurationsaustausch ermöglichen, können zu diesem Zweck verwendet werden. Nachgewiesene EB-Konfigurationen können außerdem entweder zu LCS hochgeladen werden, um sie mit Dienstabonnenten zu teilen, oder in die Produktionsumgebung für den internen Gebrauch [importiert](#data-persistence-consideration) werden.

![EB-Konfigurationslebenszyklus.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Berücksichtigung der Datenpersistenz

Sie können verschiedene Versionen einer EB-[Konfiguration](general-electronic-reporting.md#Configuration) einzeln in Ihre Instanz von Finance [importieren](tasks/er-import-configuration-lifecycle-services.md). Wenn eine neue Version einer EB-Konfiguration importiert wird, steuert das System den Inhalt der Entwurfsversion dieser Konfiguration:

- Wenn die importierte Version niedriger als die höchste Version dieser Konfiguration in der aktuellen Instanz von Finance ist, bleibt der Inhalt der Entwurfsversion dieser Konfiguration unverändert.
- Wenn die importierte Version höher ist als jede andere Version dieser Konfiguration in der aktuellen Instanz von Finance, wird der Inhalt der importierten Version in die Entwurfsversion dieser Konfiguration kopiert, damit Sie die letzte abgeschlossene Version weiter bearbeiten können.

Wenn diese Konfiguration dem [Konfigurationsanbieter](general-electronic-reporting.md#Provider) gehört, der derzeit aktiviert ist, ist die Entwurfsversion dieser Konfiguration für Sie im Inforegister **Versionen** der Seite **Konfigurationen** (**Organisationsverwaltung** > **Elektronische Berichterstattung** > **Konfigurationen**) sichtbar. Sie können die Entwurfsversion der Konfiguration auswählen und ihren Inhalt unter Verwendung des entsprechenden EB-Designers [ändern](er-quick-start2-customize-report.md#ConfigureDerivedFormat). Wenn die Entwurfsversion einer EB-Konfiguration bearbeitet haben, passt ihr Inhalt nicht mehr zur höchsten VErsion dieser Konfiguration in der aktuellen Instanz von Finance. Um den Verlust Ihrer Änderungen zu verhindern, zeigt das System einen Fehler an, dass der Import nicht fortgesetzt werden kann, da die Version dieser Konfiguration höher ist als die höchste Version dieser Konfiguration in der aktuellen Instanz von Finance. Wenn dies zum Beispiel bei der Formatkonfiguration **X** passiert, wird der Fehler **Format-„X“-Version nicht abgeschlossen** angezeigt.

Um die Änderungen rückgängig zu machen, die Sie in der Entwurfsversion vorgenommen haben, wählen Sie die höchste abgeschlossene oder freigegebene Version Ihrer EB-Konfiguration in Finance auf dem Inforegister **Versionen** und dann die Option **Diese Version abrufen** aus. Der Inhalt der ausgewählten Version wird in die Entwurfsversion kopiert.

## <a name="applicability-consideration"></a>Überlegungen zur Anwendbarkeit

Wenn Sie eine neue Version einer EB-Konfiguration entwerfen, können Sie deren [Abhängigkeit](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) auf anderen Softwarekomponenten festlegen. Dieser Schritt gilt als eine Voraussetzung für das Steuern des Downloads der Version dieser Konfiguration von einem EB-Repository oder einer externen XML-Datei und für jede weitere Nutzung der Version. Wenn Sie versuchen, eine neue Version einer EB-Konfiguration zu importieren, verwendet das System die konfigurierten Voraussetzungen, um zu steuern, ob die Version importiert werden kann.

In einigen Fällen kann es erforderlich sein, dass das System die konfigurierten Voraussetzungen ignoriert, wenn Sie neue Versionen von EB-Konfigurationen importieren. Gehen Sie folgendermaßen vor, damit das System die Voraussetzungen beim Import ignoriert.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Stellen Sie die Option **Produktaktualisierungen und Prüfung der Versionsvoraussetzungen während des Imports überspringen** auf **Ja**.

    > [!NOTE]
    > Dieser Parameter ist benutzerspezifisch und unternehmensspezifisch.

## <a name="dependencies-on-other-components"></a>Abhängigkeiten von anderen Komponenten

EB-Konfigurationen können so konfiguriert werden, dass sie von anderen Konfigurationen [abhängig](er-download-configurations-global-repo.md#import-filtered-configurations) sind. Zum Beispiel können Sie die Konfiguration eines EB-[Datenmodells](er-overview-components.md#data-model-component) aus dem globalen Repository in Ihre [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) oder Dynamics 365 Finance-Instanz [importieren](er-download-configurations-global-repo.md) und erstellen Sie dann eine neue EB [Format](er-overview-components.md#format-component)-Konfiguration, die aus der importierten EB-Datenmodellkonfiguration [abgeleitet](er-quick-start2-customize-report.md#DeriveProvidedFormat) ist. Die abgeleitete EB-Formatkonfiguration hängt von der Konfiguration des Basis-EB-Datenmodells ab.

![Abgeleitete EB-Formatkonfiguration auf der Seite „Konfigurationen“.](./media/ger-configuration-lifecycle-img1.png)

Wenn Sie mit der Gestaltung des Formats fertig sind, können Sie den Status Ihrer anfänglichen Version der EB-Formatkonfiguration von **Entwurf** auf **Abgeschlossen** ändern. Sie können dann die fertige Version der EB-Formatkonfiguration durch [Veröffentlichung](../../../finance/localizations/rcs-global-repo-upload.md) in das globale Repository freigeben. Als Nächstes können Sie von jeder RCS- oder Finance-Cloud-Instanz aus auf das globale Repository zugreifen. Sie können dann jede EB-Konfigurationsversion, die für die Anwendung anwendbar ist, aus dem globalen Repository in diese Anwendung importieren.

![Veröffentlichen der EB-Formatkonfiguration auf der Seite „Konfigurations-Repository“.](./media/ger-configuration-lifecycle-img2.png)

Basierend auf der Konfigurationsabhängigkeit wird, wenn Sie die EB-Formatkonfiguration im globalen Repository auswählen, um sie in eine neu bereitgestellte RCS- oder Finance-Instanz zu importieren, die grundlegende EB-Datenmodellkonfiguration automatisch im globalen Repository gefunden und zusammen mit der ausgewählten EB-Formatkonfiguration als Basiskonfiguration importiert.

Sie können auch Ihre Konfigurationsversion im EB-Format aus Ihrer aktuellen RCS- oder Finance-Instanz exportieren und lokal als XML-Datei speichern.

![Exportieren der Version der EB-Formatkonfiguration als XML auf der Seite „Konfiguration“.](./media/ger-configuration-lifecycle-img3.png)

Wenn Sie in Versionen von Finance **vor der Version 10.0.29** versuchen, die Version der EB-Formatkonfiguration aus dieser XML-Datei oder aus einem anderen Repository als dem globalen Repository in eine neu bereitgestellte RCS- oder Finance-Instanz zu importieren, die noch keine EB-Konfigurationen enthält, wird die folgende Ausnahme ausgelöst, um Sie darüber zu informieren, dass eine Basiskonfiguration nicht erhalten werden kann:

> Nicht aufgelöste Referenzen übrig<br>
Referenz des Objekts „\<imported configuration name\>“ auf das Objekt „Basis“ (\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>) kann nicht hergestellt werden

![Importieren der Version der EB-Formatkonfiguration auf der Seite „Konfigurations-Repository“.](./media/ger-configuration-lifecycle-img4.gif)

Wenn Sie in der Version **10.0.29 und höher** versuchen, denselben Konfigurationsimport durchzuführen, wenn eine Basiskonfiguration nicht in der aktuellen Anwendungsinstanz oder im aktuell verwendeten Quellrepository (falls zutreffend) gefunden werden kann, versucht das EB-Framework automatisch, den Namen der fehlenden Basiskonfiguration im Cache des globalen Repository zu finden. Anschließend werden der Name und der Globally Unique Identifier (GUID) der fehlenden Basiskonfiguration im Text der ausgelösten Ausnahme angezeigt.

> Nicht aufgelöste Referenzen übrig<br>
Referenz des Objekts „\<imported configuration name\>“ auf das Objekt „Basis“ (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>) kann nicht hergestellt werden

![Ausnahme auf der Seite „Konfigurations-Repository“, wenn die Basiskonfiguration nicht gefunden werden kann.](./media/ger-configuration-lifecycle-img5.png)

Sie können den bereitgestellten Namen verwenden, um die Basiskonfiguration zu finden und sie dann manuell zu importieren.

> [!NOTE]
> Diese neue Option funktioniert nur, wenn sich mindestens ein Benutzer bereits beim globalen Repository mithilfe der Seite [Konfigurations-Repositorys](er-download-configurations-global-repo.md#open-configurations-repository) oder eines der [Such](er-extended-format-lookup.md)felder des globalen Repository in der aktuellen Finance-Instanz angemeldet hat und wenn der Inhalt des globalen Repositorys zwischengespeichert wurde.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die elektronische Berichterstellung (EB)](general-electronic-reporting.md)

[Abhängigkeit von ER-Konfigurationen von anderen Komponenten festlegen](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

