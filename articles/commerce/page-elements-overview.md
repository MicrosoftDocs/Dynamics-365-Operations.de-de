---
title: Seitenmodellglossar
description: In diesem Thema werden die verschiedenen Elemente beschrieben, die auf den Seiten der Microsoft Dynamics 365 Commerce-Website verwendet werden.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4823bec149b7256960752824496ed7958586398
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339382"
---
# <a name="page-model-glossary"></a>Seitenmodellglossar


[!include [banner](includes/banner.md)]

In diesem Thema werden die verschiedenen Elemente beschrieben, die auf den Seiten der Microsoft Dynamics 365 Commerce-Website verwendet werden.

## <a name="page-element-definitions"></a>Seitenelementdefinitionen

Die folgende Tabelle enthält eine Zusammenfassung der Begriffe, die Sie kennen sollten, wenn Sie das Erscheinungsbild und den Inhalt Ihrer Website ändern. Für genauere Erklärungen und Vorgehensweisen folgen Sie den Links.

| Zeitdauer | Beschreibung und Notizen |
|------|-----------------------|
| [Modul](work-with-modules.md) | <p>**Definition:** Module sind Bausteine, die erstellt werden können und das Grundgerüst einer Webseite bilden. Zu den Beispielen zählen Kopfzeilen-, Hero- und Karusselmodule.</p><p>**Zeitpunkt der Auswahl:** Bereitgestellte Module können in verschiedenen Phasen des Site-Authoring-Workflows ausgewählt und konfiguriert werden, z. B. in den Phasen Vorlage, Layout, Seite und Fragment-Authoring.</p><p>**Bearbeitungsort:** Benutzerdefinierte Module werden mit dem Software Development Kit (SDK) im Code erstellt. Sie werden dann auf Ihre Site hochgeladen und stehen dort zur Auswahl.</p> |
| Moduleigenschaft | <p>**Definition:** Moduleigenschaften sind bestimmte Einstellungen, die im Modul festgelegt werden. Sie können in den E-Commerce-Erstellungstools bearbeitet werden. Beispielsweise werden Moduleigenschaften verwendet, um die Überschrift und das Hintergrundbild eines Bannermoduls festzulegen.</p><p>**Konfigurationsort:** Moduleigenschaften werden im Eigenschaftenbereich ausgewählt und konfiguriert, der in den Erstellungsumgebungen (Editoren) für Vorlagen, Layouts, Seiten, Fragmente und App-Einstellungen angezeigt wird.</p> |
| [Vorlage](templates-layouts-overview.md) | <p>**Definition:** Vorlagen definieren die Modulkombinationen und -optionen, die für eine Kategorie von Seiten verwendet werden sollen (z. B. Marketing-Seiten, Kategorieseiten und Produktseiten).</p><p>**Auswahlort:** Vorlagen können während der Seiten- oder Layouterstellungsworkflows ausgewählt werden.</p><p>**Bearbeitungsort:** Vorlagen werden im Vorlageneditor erstellt. Es ist kein Code erforderlich, um sie zu erstellen oder zu ändern.</p> |
| [Layout](templates-layouts-overview.md) | <p>**Definition:** Layouts definieren die endgültige Auswahl und Anordnung der Module aus dem Optionssatz der übergeordneten Vorlage. Ein Layout kann für eine einzelne Seite konfiguriert werden (*benutzerdefiniertes Layout*) oder es kann für mehrere Seiten freigegeben werden (*vordefiniertes Layout*).</p><p>**Auswahlort:** Layouts können während der Erstellung neuer Seiten, oder wenn für eine vorhandene Seite ein anderes Layout erforderlich ist, ausgewählt werden.</p><p>**Bearbeitungsort:** Layouts werden im Layout-Editor erstellt. Es ist kein Code erforderlich, um sie zu erstellen oder zu ändern.</p> |
| [Seiteninstanz](modify-existing-page.md) | <p>**Definition:** Seiteninstanzen definieren den endgültigen, seitenbezogenen lokalisierten Inhalt für eine einzelne Seite. Dieser Inhalt wird aus den Werten der Moduleigenschaften abgeleitet.</p><p>**Auswahlort:** Seiten werden bei der Zuweisung von URLs ausgewählt.</p><p>**Bearbeitungsort:** Seiten werden im Seiten-Editor bearbeitet. Es ist kein Code erforderlich, um sie zu erstellen oder zu ändern.</p> |
| [Thema](select-site-theme.md) | <p>**Definition:** Designs definieren das Cascading Style Sheet (CSS) und legen das Erscheinungsbild der Module fest, die auf einer Seite gerendert werden.</p><p>**Auswahlort:** Nachdem ein Design auf Ihre Website durch die Verwendung von Microsoft Dynamics Lifecycle Services (LCS) hochgeladen wurde, kann es als Eigenschaft des Seitencontainermoduls ausgewählt werden.</p><p>**Bearbeitungsort:** Designs werden derzeit mithilfe des SDK erstellt und bearbeitet. Sie werden dann mithilfe von LCS auf Ihre Site hochgeladen.</p> |
| [Fragment](work-with-fragments.md) | <p>**Definition:** Fragmente sind vollständig konfigurierte Module mit lokalisiertem Inhalt, der auf mehreren Seiten wiederverwendet und zentral aktualisiert werden kann. Beispielsweise kann ein Fragment, das aus einem Kopfzeilenmodul erstellt wurde, in allen Vorlagen und auf allen Seiten Ihrer Website verwendet und zentral an einer Stelle aktualisiert werden.</p><p>**Auswahlort:** Fragmente können überall dort ausgewählt werden, wo Module ausgewählt werden können. Sie können ein Modul ersetzen, um die Effizienz durch wiederverwendbares und zentrales Authoring zu steigern.</p><p>**Bearbeitungsort:** Fragmente werden im Fragmenten-Editor bearbeitet. Es ist kein Code erforderlich, um sie zu erstellen oder zu ändern.</p> |
| [URL](create-page-URL.md) | <p>**Definition:** Uniform Resource Locators (URLs) sind Adressen, die auf Webseiten oder andere URLs verweisen.</p><p>**Auswahlort:** URLs werden immer ausgewählt, wenn Links zwischen Seiten erforderlich sind.</p><p>**Bearbeitungsort:** URLs werden im URL-Editor bearbeitet. Es ist kein Code erforderlich, um sie zu erstellen oder zu ändern.</p> |
| Anlage | <p>**Definition:** Assets sind Dateibinärdateien mit einer Erweiterung wie .jpg, .docx, .pdf oder .mpg.</p><p>**Auswahlort:** Assets werden als Moduleigenschaften für Module ausgewählt, die sie benötigen.</p><p>**Bearbeitungsort:** Assets werden hochgeladen und die zugehörigen Metadaten werden im Asset Manager bearbeitet.</p> |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Möglichkeiten zum Hinzufügen von Inhalten](add-manage-content.md)

[Dokumentstatus und -Lebenszyklus](document-states-overview.md)

[Arbeiten mit Veröffentlichungsgruppen](publish-groups.md)

[Aktivieren und verwenden Sie die kanalübergreifende Freigabe](cross-channel-sharing.md)

[Arbeiten mit Modulen](work-with-modules.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Anpassen der Sitenavigation](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]