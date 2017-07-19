---
title: "Produktinformationsübersicht"
description: "Dieses Thema enthält Informationen zur Produktinformationsverwaltung. Die Produktinformationsverwaltung funktioniert mit einer freigegebenen Produktdefinition, Kategorisierung und Kennungen für alle juristischen Personen und auch bestimmte Konfigurationen eines Produkts, um Geschäftsprozessen gerecht zu werden."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: db8a9666518b58b6b32bb4a14933095dd9416aa0
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="product-information-overview"></a>Produktinformationsübersicht

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Dieses Thema enthält Informationen zur Produktinformationsverwaltung. Die Produktinformationsverwaltung funktioniert mit einer freigegebenen Produktdefinition, Kategorisierung und Kennungen für alle juristischen Personen und auch bestimmte Konfigurationen eines Produkts, um Geschäftsprozessen gerecht zu werden. 

Produktinformationen sind die Grundlage von Lieferketten- und Einzelhandelsanwendungen in allen Branchen. Sie beziehen sich auf Prozesse und Technologien, die sich auf die zentrale Verwaltung von Informationen zu Produkten fokussieren (beispielsweise Lieferketten). Es ist wichtig, dass freigegebene Produktdefinitionen, Dokumentationen, Attribute, Kennungen verwendet werden. In den verschiedenen Modulen einer Geschäftslösung sind produktspezifische Informationen und Konfigurationen erforderlich, um die Geschäftsprozesse zu verwalten, die mit bestimmten Produkten, Produktkategorien oder Produktfamilien verknüpft sind.

## <a name="product-definition"></a>Produktdefinition

Ein Produkt wird hauptsächlich durch eine Produktnummer, einen Namen und eine Beschreibung definiert. Es sind jedoch auch andere Daten erforderlich, ein Produkt oder einen Service zu beschreiben:

- Produkttyp: Artikel oder Service
- Produktuntertyp: Eindeutig identifizierbare Produkte oder Produktmaster
- Produktvariantenmodell-Definition:

     - Produktdimensionen und Dimensionsgruppen
     - Produktbezeichnungen
     - Produktkonfigurationsmodelle

- Zuordnung des Produkts zu einer oder mehreren Kategorien
- Definition der Produkt- und Kategorieattribute
- Produktbilder
- Anhänge
- Die Maßeinheiten und verwandte Umwandlungen
- Übersetzungen aller Namen und Beschreibungen

## <a name="distribution-export-and-import-of-product-data"></a>Vertrieb, Export und Import von Produktdaten

Die Produktdefinition kann in Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, erstellt werden. Sie kann auch von der Produktlebenszyklusverwaltung (PLM), von der Produktdatenverwaltung (PDM) oder von Produktinformationsmanagement (PIM)-Systemen importiert werden. Werden mehrere Finance and Operations-Instanzen verwendet, ist eine Instanz in der Regel der Master der Produktdaten für alle anderen Instanzen. Dieser Ansatz wird von einem großen Satz an Datenentitäten unterstützt, der den Import und Export von Produktdefinitionsdaten von einer Instanz zu einer anderen ermöglicht.

Um die Verteilung von Produktdaten auf viele Instanzen zu unterstützen, ermöglicht Finance and Operations Ihnen die Nutzung des Common Data Service. Produktdefinitionen können von einer Finance and Operations-Instanz zu Common Data Service exportiert werden. Die Produktdefinitionen können dann verwendet werden, um andere Geschäftsanwendungen wie Microsoft Dynamics 365 for Sales mit Produktdaten zu versorgen.

Beachten Sie, dass sich in dynamischen und agilen Organisationen die Produktinformationsdaten täglich ändern. Deshalb ist die Verwaltung von genauen und tatsächlichen Produktdaten selbst ein kritischer Geschäftsprozess.

## <a name="product-masters-and-product-variants"></a>Produktmaster und Produktvarianten

In einer agilen Welt, in der Produkte an die Kundenanforderungen schnell angepasst werden müssen, geben Produktdefinitionen einen Satz an Produkten dar anstelle von eindeutig identifizierbaren Produkten. In Microsoft Dynamics 365 for Finance and Operations werden diese generischen Produkte als *Produktmaster* bezeichnet. Produktmaster enthalten die Definition und die Regeln, die angeben, wie eindeutig identifizierbare Produkte in Geschäftsprozessen beschrieben sind uns sich verhalten. Auf Grundlage dieser Definitionen können eindeutig identifizierbare Produkte generiert werden. Diese eindeutig identifizierbare Produkte bezeichnet man als *Produktvarianten*.

In Finance and Operations wird ein Produktmaster einer Produktdimensionsgruppe und einer Konfigurationstechnologie zugeordnet, um die Geschäftsregeln anzugeben. Die Produktdimensionen (Farbe, Größe, Stil und Konfiguration) sind ein bestimmter Satz an Attributen, der in der Anwendung verwendet werden kann, um das Verhalten verwandter Produkte zu definieren und zu verfolgen. Diese Dimensionen helfen Benutzern bei der Suche nach Produkten und deren Identifizierung.

## <a name="configuration-technologies"></a>Konfigurationstechnologien

Sie können zwischen drei Konfigurationstechnologien wählen:

- Die vordefinierten Varianten werden nach vordefinierten Produktdimensionen definiert. Die Variantendefinition enthält die Definition einer bestimmten zulässigen Kombination von Varianten wie Farbe, Stil und Größe. Jede Kombination erzeugt eine eindeutig identifizierbare Produktvariante.
- Die dimensionsbasierte Konfiguration wird üblicherweise bei Fertigungsszenarien verwendet und ermöglicht Ihnen die Nutzung der Konfigurationsdimension in der Definition der Stücklisten (BOMs). Nachdem eine bestimmte Konfiguration ausgewählt ist, verwendet das System die Teilmenge der Stücklistenpositionen, die für diese Konfiguration für die Planung und Produktion gültig sind. Dieses Konzept ist auch als *globale Stückliste* bekannt, da eine gemeinsame Stückliste für alle Konfigurationen eines Produkts verwendet wird.
- Die einschränkungsbasierte Konfiguration verwendet ein Produktkonfigurationsmodell, um alle möglichen Attribute und Komponenten zu beschreiben, die erforderlich sind, um alle möglichen Varianten eines Produkts in einem einzigen Modell zu beschreiben. Die Einschränkungen der Kombinationen von Attributen können über regelmäßige Ausdrücke oder tabellenbasierte Einschränkungen beschrieben werden. Konfigurationsmodelle und Konfiguratoren werden beim Produktinformationsmanagement wichtig und werden in allen Branchen eingesetzt.

Wenn Sie die Implementierung von Finance and Operations planen, müssen Sie die richtige Konfigurationstechnologie für einen Geschäftsprozess auswählen. Ein Produkt kann nach der Implementierung nicht von einem Modell in ein anderes konvertiert werden.

## <a name="product-variant-model-definition-workspace"></a>Produktvariantenmodell-Definition – Arbeitsbereich

Der Arbeitsbereich **Produktvariantenmodell-Definition** enthält eine Übersicht über Produktmaster. Er zeigt auch den Status der Freigabe des Masters sowie verwandte Varianten für bestimmte juristische Personen.

## <a name="released-products"></a>Freigegebene Produkte

Die Produkte, die für eine bestimmte juristische Person freigegeben werden, werde als als *freigegebene Produkte* bezeichnet. Produkte können mit anderen zusammen für eine juristische Person oder gleichzeitig für mehrere juristische Personen freigegeben werden. Da verschiedene Eigenschaften und Attribute der Produkte möglicherweise pro juristischer Person hinzugefügt werden müssen, ermöglicht Ihnen der Arbeitsbereich **Freigegebene Produktverwaltung** die Überwachung und das Abschließen kürzlich freigegebener Produkte in den einzelnen juristischen Personen oder in den Suborganisationen einer juristischen Person.

### <a name="released-product-maintenance-workspace"></a>Freigegebene Produktverwaltung – Arbeitsbereich

Sie können den Arbeitsbereich **Freigegebene Produktverwaltung** über die Menüoption **Eigenen Arbeitsbereich konfigurieren** konfigurieren. Wählen Sie eine Kategoriehierarchie und eine Kategorie aus, nach der der Arbeitsbereich gefiltert wird. Um die relevanten Produktdaten im Arbeitsbereich anzupassen, können Sie, in Tagen, auch die Planungszeiträume für **Zuletzt freigegebene Produkte** und **Gestoppte, freigegebene Produkte** definieren.

Der Arbeitsbereich enthält eine Zusammenfassung von Kacheln und zweier Listen. Die Liste **Offene Anfragen** zeigt Produktänderungsanfragen für Produkte in der ausgewählten Produktkategoriehierarchie, die nicht abgeschlossen und geschlossen sind. Die Liste **Vor kurzem freigegeben** enthält Produkte, die innerhalb des Planungszeitraums freigegeben wurden, der in der Arbeitsbereichkonfiguration festgelegt ist. Für jeden Artikel der Liste wird eine Validierung ausgeführt und der Validierungsstatus angezeigt. Dieser Status könnte angeben, dass die für die juristische Person erforderlichen Konfigurationen noch nicht abgeschlossen sind. Über die Liste können Sie direkt auf die Seiten **Details für freigegebene Produkte**, **Produktattributverwaltung**, **Produktkategorieverwaltung**, **Standardauftragseinstellungen** und **Textübersetzungen** zugreifen, um die erforderliche Konfiguration für das Produkt abzuschließen.

### <a name="manually-creating-a-new-released-product"></a>Ein neues freigegebenes Produkt manuell erstellen

Sie können ein freigegebenes Produkt manuell in einer einzigen Ausführung erstellen, je nach Geschäftsprozessen der Organisation und Regeln darüber, ob diese Funktion genutzt werden sollte. Diese Funktion erstellt ein neues Produkt und gibt es automatisch für die aktuelle juristische Person frei. Zum Erstellen eines neuen Produkts klicken Sie auf **Freigegebene Produkte** im Arbeitsbereich **Freigegebene Produktverwaltung** oder auf der Listenseite **Freigegebenes Produkt**.

