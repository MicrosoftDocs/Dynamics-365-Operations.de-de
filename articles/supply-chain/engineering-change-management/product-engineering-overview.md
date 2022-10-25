---
title: Überblick über die Verwaltung für technische Änderungen (enthält Video)
description: Dieser Artikel bietet einen Überblick über die Verwaltung für technische Änderungen, die Sie bei der Planung und Verwaltung der Produktversionsverwaltung sowie bei der Verwaltung von Produktlebenszyklen und technischen Änderungen unterstützt.
author: t-benebo
ms.date: 08/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a01dfd72428c75d1bb24f32c73c9c799a6c5017e
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682505"
---
# <a name="engineering-change-management-overview"></a>Überblick über die Verwaltung für technische Änderungen

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funktionszusammenfassung

In einer Welt ständig kürzerer Produktlebenszyklen, höherer Anforderungen an Qualität und Zuverlässigkeit und einer stärkeren Konzentration auf die Produktsicherheit benötigen Hersteller heute ein leistungsfähiges Produktdatenmanagement, eine Versionskontrolle und eine Verwaltung für technische Änderungen.

Die Verwaltung für technische Änderungen bringt Struktur und Disziplin in den Prozess der Produktdatenverwaltung und ermöglicht die Definition, Freigabe und Überarbeitung von Produkten auf kontrollierte Weise, die durch Workflows unterstützt wird. Mit Hilfe von Produktversionen und der Verwaltung für technische Änderungen können Sie die Auswirkungen von technischen Änderungen während des gesamten Lebenszyklus eines Produkts dokumentieren, bewerten und anwenden.

Die Verwaltung für technische Änderungen unterstützt Sie bei der Planung und Verwaltung von Produktversionen sowie bei der Verwaltung von Produktlebenszyklen und technischen Änderungen. Hier ist eine Liste der wichtigsten Funktionen:

- Produktversionsverwaltung
- Erweiterte Produktfreigabefunktionalität, mit der Sie Produktstammdaten in einer juristischen Entität (der Engineering-Firma) pflegen und das vollständig konfigurierte freigegebene Produkt an andere juristische Entitäten veröffentlichen können
- Regeln zur Überprüfung, ob erforderliche Informationen eingegeben wurden, bevor eine Produktversion aktiviert wird (Bereitschaftsprüfungen)
- Verbessertes Produktlebenszyklus-Management durch fein abgestufte Kontrolle darüber, wann ein freigegebenes Produkt in bestimmten Geschäftsprozessen verwendet werden kann
- Technische Änderungsanforderungen, die durch Workflows unterstützt werden
- Technische Änderungsaufträge, die durch Workflows unterstützt werden

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Das vorhergehende Video ([Funktionalitäten der Änderungsverwaltung in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) ist in der [Wiedergabeliste Finanzen und Vorgänge](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Schalten Sie die Verwaltungfunktionen für technische Änderungen für Ihr System ein

Bevor Sie die Verwaltung für technische Änderungen nutzen können, müssen Sie sowohl die Funktion *Verwaltung für technische Änderungen* als auch deren Konfigurationsschlüssel aktivieren. Wenn Sie auch die Versionsdimension von Produkten in Transaktionen verfolgen wollen (optional), müssen Sie auch die Funktion *Produktversionsdimension* und deren Konfigurationsschlüssel aktivieren. Nachdem diese Voraussetzungen wie erforderlich eingerichtet wurden, können Sie zusätzliche optionale Funktionen für die Änderungsverwaltung aktivieren.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Die grundlegenden Verwaltungsfunktionen für technische Änderungen an- oder ausschalten

Um die grundlegenden Funktionen der Verwaltung für technische Änderungen an- oder auszuschalten, gehen Sie wie folgt vor. Ab Supply Chain Management Version 10.0.25 ist die Funktion *Verwaltung für technische Änderung* standardmäßig aktiviert.

1. Gehen Sie in den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Suchen Sie nach Updates.
1. Schalten Sie die Funktion *Verwaltung für technische Änderungen* nach Bedarf an oder aus.
1. Wenn Sie auch die Versionsdimension von Produkten in Transaktionen verfolgen wollen (optional), schalten Sie die Funktion *Produktdimensionsversion* an.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Die erforderlichen Konfigurationsschlüssel an- oder ausschalten

Als nächstes schalten Sie die Konfigurationstasten ein, indem Sie diese Schritte befolgen. Diese sind nicht standardmäßig eingeschaltet.

1. Legen Sie Ihr System in den Wartungsmodus ein, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Erweitern Sie den Knoten **Handel**.
1. Aktivieren oder deaktivieren Sie den Konfigurationsschlüssel für die Hauptfunktion über das Kontrollkästchen **Verwaltung für technische Änderungen**.
1. Erweitern Sie den Knoten **Engineering Change Management** und aktivieren oder deaktivieren Sie die folgenden Kontrollkästchen nach Bedarf (abhängig von den Funktionen, die Sie verwenden möchten):

    - **Attributsuche** – Wählen Sie dieses Kontrollkästchen, um die [Attributsuchfunktion](engineering-attributes-and-search.md) zu aktivieren. Wir empfehlen, diese Funktion zu aktivieren. Sie können dieses Kontrollkästchen jedoch deaktivieren, wenn Sie es nicht verwenden.
    - **Änderungsverwaltung für die Prozessfertigung** – Aktivieren Sie dieses Kontrollkästchen, wenn Sie die Funktionen zur Verwaltung technischer Änderungen verwenden möchten, um Änderungen in Formeln für die Prozessfertigung zu verwalten. Wenn Sie keine Formeln verwalten müssen, können Sie dieses Kontrollkästchen deaktivieren. Weitere Informationen finden Sie unter [Verwalten Sie Änderungen in Formeln und deren Substanzen](manage-formula-changes.md).

1. Wenn Sie auch die Dimension „Version“ verwenden möchten, dann aktivieren Sie das Kontrollkästchen **Produktdimension – Version**. (Dieses Kontrollkästchen befindet sich weiter unten in der Liste, nicht unter dem Knoten **Verwaltung für technische Änderungen**.) Sie können dieses Kontrollkästchen deaktivieren, wenn Sie diese Funktion nicht benötigen.
1. Schalten Sie den Wartungsmodus aus, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
1. Die Datenbank muss synchronisiert werden, um sicherzustellen, dass die Konfigurationsschlüssel richtig aktualisiert wurden, um Ihre Änderungen widerzuspiegeln. Führen Sie je nach Art der Umgebung, in der Sie arbeiten, einen der folgenden Schritte aus:
    - **Für Umgebungen der Ebene 1 (Entwicklung)** : Öffnen Sie Ihr Projekt in Microsoft Visual Studio und wählen Sie **Dynamics 365 \> Datenbank synchronisieren \> Synchronisieren** aus.
    - **Für Umgebungen der Stufe 2 (und höher)** : Die Datenbank wird automatisch synchronisiert, nachdem Sie die Umgebung in den Wartungsmodus versetzt und wieder verlassen haben, sodass Sie diesen Schritt überspringen können.

> [!NOTE]
> Um den Änderungsdienst verwenden zu können, müssen sowohl der Stücklisten-Nummernkreis als auch der Formel-Nummernkreis (wenn Sie Formeln verwenden) auf *Automatisch* auf der **Zahlenfolgen** Seite eingestellt sein.

### <a name="turn-on-additional-engineering-change-management-features"></a>Einschalten der zusätzlichen Verwaltungfunktionen für technische Änderungen

Nachdem Sie die grundlegenden Funktionen für die Änderungsverwaltung aktiviert und deren Konfigurationsschlüssel aktiviert haben, werden dem Funktionsmanagement mehrere zusätzliche und optionale Funktionen für die Änderungsverwaltung hinzugefügt. Jede dieser Funktionen ist unter dem **Verwaltung für technische Änderung**-Modul aufgeführt. Die folgende Tabelle beschreibt jede optionale Funktion und enthält Links für weitere Informationen.

| Funktion Name in FunktionVerwaltung | Description | Status der Funktion |
|---|---|---|
| Änderungsmanagement für vorhandene Produkte aktivieren | <p>Mit dieser Funktion können Sie vorhandene Produkte in Konstruktionsprodukte umwandeln, damit Sie sie mithilfe der Änderungsverwaltung verwalten können.</p><p>Weitere Informationen finden Sie unter [Änderungsverwaltung für bestehende Produkte aktivieren](change-management-existing-products.md).</p> | Standardmäßig aktiviert ab Version 10.0.25. |
| Technische Benachrichtigungen für die Produktion | <p>Wenn ein Produkt in der Konstruktion geändert wird, kann es wichtig sein, die Produktion über diese Änderungen zu informieren. Auf diese Weise können Produktionsmitarbeiter geeignete Maßnahmen ergreifen, z. B. Komponentenaustausch, Stücklistenaustausch oder Arbeitsplanaustausch. Mit dieser Funktion können Sie die Produktion über Änderungen an Produkten benachrichtigen, die gerade produziert werden.</p><p>Weitere Informationen finden Sie unter [Verwalten von Änderungen an Engineering-Produkten](engineering-change-management.md).</p> |  Standardmäßig aktiviert ab Version 10.0.25. |
| Verbesserte Attributvererbung für Konstruktionsänderungsmanagement | <p>Diese Funktion vereinfacht die Verwaltung von Attributen für Fertigwaren oder Zwischenartikel. Wenn diese Funktion aktiviert ist, ist es einfacher, alle Attribute zu identifizieren, die zu einem Element gehören, und Sie können die Attribute auswählen, die von diesem Element an sein übergeordnetes Element weitergegeben werden sollen. Diese Funktion ist nützlich, wenn beispielsweise eine Komponente eines Endprodukts zerbrechlich, giftig oder entflammbar ist, da Sie das zerbrechliche, giftige oder entflammbare Attribut leicht identifizieren und auf das Endprodukt übertragen können.</p><p>Weitere Informationen finden Sie unter [Engineering-Attribute und die Suche nach Engineering-Attributen](engineering-attributes-and-search.md).</p> |  Standardmäßig aktiviert ab Version 10.0.25. |
| Produktbereitschaftsprüfungen | <p>Diese Funktion ermöglicht die EInrichtung von Bereitschaftsprüfungen für Standardprodukte (nicht technische Produkte). Verwenden Sie Produktbereitschaftsprüfungen, um sicherzustellen, dass jedes Produkt vollständig definiert und alle erforderlichen Richtlinien konfiguriert sind, bevor das Produkt zur Verfügung gestellt und in Transaktionen verwendet wird. Wenn Sie diese Funktion nach längerer Nutzung deaktivieren, werden alle vorhandenen Bereitschaftsprüfungen für Standardprodukte gelöscht.</p><p>Weitere Informationen finden Sie unter [Produktbereitschaft](product-readiness.md).</p> |  Standardmäßig aktiviert ab Version 10.0.25. |
| Änderungen an Formeln und ihren Substanzen verwalten | <p>Mit dieser Funktion können Sie Änderungen an Formelinhaltsstoffen, Co-Produkten und Nebenprodukten verfolgen.</p><p>Weitere Informationen finden Sie unter [Verwalten Sie Änderungen in Formeln und deren Substanzen](manage-formula-changes.md).</p> |  Standardmäßig aktiviert ab Version 10.0.25. |
| Variantengenerierung für technische Produkte | <p>Mit dieser Funktion können Sie Varianten für Konstruktionsprodukte basierend auf verfügbaren Dimensionswerten generieren.</p><p>Weitere Informationen finden Sie unter [Generieren Sie Varianten für Engineering-Produkte](engineering-variants.md).</p> |  Standardmäßig aktiviert ab Version 10.0.25. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

