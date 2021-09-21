---
title: Überblick über die Verwaltung für technische Änderungen
description: Dieses Thema bietet einen Überblick über die Verwaltung für technische Änderungen, die Sie bei der Planung und Verwaltung der Produktversionsverwaltung sowie bei der Verwaltung von Produktlebenszyklen und technischen Änderungen unterstützt.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.21
ms.openlocfilehash: b4fe2d62bc8084cf8c0d10b7bcb94f08cc618900
ms.sourcegitcommit: 07fada750de54e2907377df2a9f7dae497c3b66e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2021
ms.locfileid: "7467397"
---
# <a name="engineering-change-management-overview"></a>Überblick über die Verwaltung für technische Änderungen

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funktionszusammenfassung

Heutige Hersteller benötigen ein starkes Produktdatenmanagement, eine Versionskontrolle und eine Verwaltung für technische Änderungen, um in einer Welt ständig kürzer werdender Produktlebenszyklen, erhöhter Qualitäts- und Zuverlässigkeitsanforderungen und eines verstärkten Fokus auf die Produktsicherheit erfolgreich zu sein.

Die Verwaltung für technische Änderungen bringt Struktur und Disziplin in den Prozess der Produktdatenverwaltung und ermöglicht es, Produkte auf kontrollierte Weise zu definieren, freizugeben und zu überarbeiten, die durch Workflows unterstützt wird. Mit Hilfe von Produktversionen und der Verwaltung für technische Änderungen können Sie technische Änderungen während des gesamten Lebenszyklus eines Produkts dokumentieren, deren Auswirkungen bewerten und anwenden.

Die Verwaltung für technische Änderungen unterstützt Sie bei der Planung und Verwaltung von Produktversionen sowie bei der Verwaltung von Produktlebenszyklen und technischen Änderungen. Hier ist eine Liste der wichtigsten Funktionen:

- Produktversionsverwaltung
- Erweiterte Produktfreigabefunktionalität, mit der Sie Produktstammdaten in einer juristischen Entität (der Engineering-Firma) pflegen und das vollständig konfigurierte freigegebene Produkt an andere juristische Entitäten veröffentlichen können
- Regeln zur Überprüfung, ob erforderliche Informationen eingegeben wurden, bevor eine Produktversion aktiviert wird (Bereitschaftsprüfungen)
- Verbessertes Produktlebenszyklus-Management durch fein abgestufte Kontrolle darüber, wann ein freigegebenes Produkt in bestimmten Geschäftsprozessen verwendet werden kann
- Technische Änderungsanforderungen, die durch Workflows unterstützt werden
- Technische Änderungsaufträge, die durch Workflows unterstützt werden

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Das vorhergehende Video ([Funktionalitäten der Änderungsverwaltung in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) ist in der [Finance and Operations-Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Schalten Sie die Verwaltungfunktionen für technische Änderungen für Ihr System ein

Bevor Sie die Verwaltung für technische Änderungen nutzen können, müssen Sie sowohl die Funktion *Verwaltung für technische Änderungen* als auch deren Konfigurationsschlüssel aktivieren. Wenn Sie auch die Versionsdimension von Produkten in Transaktionen verfolgen wollen (optional), müssen Sie auch die Funktion *Produktversionsdimension* und deren Konfigurationsschlüssel aktivieren. Nachdem diese Voraussetzungen wie erforderlich eingerichtet wurden, können Sie zusätzliche optionale Funktionen für die Änderungsverwaltung aktivieren.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Einschalten der grundlegenden Verwaltungfunktionen für technische Änderungen

Schalten Sie zunächst die Funktionen ein, indem Sie diese Schritte ausführen.

1. Gehen Sie in den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Suchen Sie nach Updates.
1. Schalten Sie die Funktion ein, die *Verwaltung für technische Änderungen* genannt wird.
1. Wenn Sie sie verwenden wollen, dann schalten Sie auch die Funktion ein, die *Produktdimension Version* heißt.

### <a name="turn-on-the-required-configuration-keys"></a>Einschalten der erforderlichen Konfigurationsschlüssel

Als nächstes schalten Sie die Konfigurationstasten ein, indem Sie diese Schritte befolgen.

1. Legen Sie Ihr System in den Wartungsmodus ein, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Erweitern Sie den Knoten **Handel**.
1. Aktivieren Sie den Konfigurationsschlüssel für die Hauptfunktion, indem Sie das Kontrollkästchen **Verwaltung für technische Änderungen** aktivieren.
1. Erweitern Sie den Knoten **Engineering Change Management** und aktivieren oder deaktivieren Sie die folgenden Kontrollkästchen nach Bedarf (abhängig von den Funktionen, die Sie verwenden möchten):

    - **Attributsuche** – Wählen Sie dieses Kontrollkästchen, um die [Attributsuchfunktion](engineering-attributes-and-search.md) zu aktivieren. Wir empfehlen, diese Funktion zu aktivieren. Sie können dieses Kontrollkästchen jedoch deaktivieren, wenn Sie es nicht verwenden.
    - **Änderungsverwaltung für die Prozessfertigung** – Aktivieren Sie dieses Kontrollkästchen, wenn Sie die Funktionen zur Verwaltung technischer Änderungen verwenden möchten, um Änderungen in Formeln für die Prozessfertigung zu verwalten. Wenn Sie keine Formeln verwalten müssen, können Sie dieses Kontrollkästchen deaktivieren. Weitere Informationen finden Sie unter [Verwalten Sie Änderungen in Formeln und deren Substanzen](manage-formula-changes.md).

1. Wenn Sie auch die Dimension „Version“ verwenden möchten, dann aktivieren Sie das Kontrollkästchen **Produktdimension – Version**. (Dieses Kontrollkästchen befindet sich weiter unten in der Liste, nicht verschachtelt unter dem Knoten **Knoten Verwaltung für technische Änderungen**.)
1. Schalten Sie den Wartungsmodus aus, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.

> [!IMPORTANT]
> Ab April 2022 werden die Lizenzschlüssel für sowohl **Verwaltung für technische Änderungen** als auch **Produktdimension – Version** standardmäßig für alle neuen Installationen aktiviert sein, aber Sie können sie bei Bedarf immer noch deaktivieren.

### <a name="turn-on-additional-engineering-change-management-features"></a>Einschalten der zusätzlichen Verwaltungfunktionen für technische Änderungen

Nachdem Sie die grundlegenden Funktionen für die Änderungsverwaltung aktiviert und deren Konfigurationsschlüssel aktiviert haben, werden dem Funktionsmanagement mehrere zusätzliche und optionale Funktionen für die Änderungsverwaltung hinzugefügt. Jede dieser Funktionen ist unter dem **Verwaltung für technische Änderung**-Modul aufgeführt. Die folgende Tabelle beschreibt jede optionale Funktion und enthält Links für weitere Informationen.

| Funktion Name in FunktionVerwaltung | Beschreibung |
|---|---|
| Änderungsmanagement für vorhandene Produkte aktivieren | <p>Mit dieser Funktion können Sie vorhandene Produkte in Konstruktionsprodukte umwandeln, damit Sie sie mithilfe der Änderungsverwaltung verwalten können.</p><p>Weitere Informationen finden Sie unter [Änderungsverwaltung für bestehende Produkte aktivieren](change-management-existing-products.md).</p> |
| Technische Benachrichtigungen für die Produktion | <p>Wenn ein Produkt in der Konstruktion geändert wird, kann es wichtig sein, die Produktion über diese Änderungen zu informieren. Auf diese Weise können Produktionsmitarbeiter geeignete Maßnahmen ergreifen, z. B. Komponentenaustausch, Stücklistenaustausch oder Arbeitsplanaustausch. Mit dieser Funktion können Sie die Produktion über Änderungen an Produkten benachrichtigen, die gerade produziert werden.</p><p>Weitere Informationen finden Sie unter [Verwalten von Änderungen an Engineering-Produkten](engineering-change-management.md).</p> |
| Verbesserte Attributvererbung für Konstruktionsänderungsmanagement | <p>Diese Funktion vereinfacht die Verwaltung von Attributen für Fertigwaren oder Zwischenartikel. Wenn diese Funktion aktiviert ist, ist es einfacher, alle Attribute zu identifizieren, die zu einem Element gehören, und Sie können die Attribute auswählen, die von diesem Element an sein übergeordnetes Element weitergegeben werden sollen. Diese Funktion ist nützlich, wenn beispielsweise eine Komponente eines Endprodukts zerbrechlich, giftig oder entflammbar ist, da Sie das zerbrechliche, giftige oder entflammbare Attribut leicht identifizieren und auf das Endprodukt übertragen können.</p><p>Weitere Informationen finden Sie unter [Engineering-Attribute und die Suche nach Engineering-Attributen](engineering-attributes-and-search.md).</p> |
| Produktbereitschaftsprüfungen | <p>Diese Funktion ermöglicht die EInrichtung von Bereitschaftsprüfungen für Standardprodukte (nicht technische Produkte). Verwenden Sie Produktbereitschaftsprüfungen, um sicherzustellen, dass jedes Produkt vollständig definiert und alle erforderlichen Richtlinien konfiguriert sind, bevor das Produkt zur Verfügung gestellt und in Transaktionen verwendet wird. Wenn Sie diese Funktion nach längerer Nutzung deaktivieren, werden alle vorhandenen Bereitschaftsprüfungen für Standardprodukte gelöscht.</p><p>Weitere Informationen finden Sie unter [Produktbereitschaft](product-readiness.md).</p> |
| Änderungen an Formeln und ihren Substanzen verwalten | <p>Mit dieser Funktion können Sie Änderungen an Formelinhaltsstoffen, Co-Produkten und Nebenprodukten verfolgen.</p><p>Weitere Informationen finden Sie unter [Verwalten Sie Änderungen in Formeln und deren Substanzen](manage-formula-changes.md).</p> |
| Variantengenerierung für technische Produkte | <p>Mit dieser Funktion können Sie Varianten für Konstruktionsprodukte basierend auf verfügbaren Dimensionswerten generieren.</p><p>Weitere Informationen finden Sie unter [Generieren Sie Varianten für Engineering-Produkte](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
