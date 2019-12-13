---
title: Containermodul
description: Dieses Thema enthält Containermodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697059"
---
# <a name="container-module"></a>Containermodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Containermodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Containermodul ist ein Modul, das andere Module hostet. Dies ist der generischste Container, der in Dynamics 365 Commerce verwendet wird. Der Hauptzweck eines Containermoduls ist es, die Eigenschaften zu definieren, die für sie festgelegt, werden, wie das Layout der Module, die enthalten sind. Diese Module können nebeneinander in einem Zwei-, Drei-, Vier- oder Sechsspalten-Layout angezeigt werden. Sie können auch auf die Breite des Containers beschränkt werden, oder sie können den Bildschirm ausfüllen. Eine Überschrift kann zu jedem Containermodul hinzugefügt werden.

Es gibt drei standardmäßige Containermodule: Container, Containern mit 2 Slots und Container mit 3 Slots. Module von einem beliebigen Typ von Modulen können innerhalb dieser Container festgelegt werden. Es gibt auch bestimmte Arten von Containermodulen, wie Karussell, umfangreicher Inhaltsblock, Inhaltplatzierung, Einkaufskorb, Auschecken, Kauffeld, Kopf- und Fußzeile. Diese Container gelten bestimmten Zwecken und nur bestimmte unterstützte Typen von Modulen können darin festgelegt werden.

Es wird empfohlen, dass Sie die Module innerhalb eines Containers festlegen, sodass sie auf die Breite des Containers beschränkt werden können.

## <a name="examples-of-container-modules-in-e-commerce"></a>Beispiele für Containermodulen in E-Commerce

- Ein Siteautor will ein Dreispaltenlayout, bei dem drei Module nebeneinander angezeigt werden. Daher nutzt der Siteautor ein Containermodul des Containers vom Typ mit 3 Slots.
- Ein Siteautor will ein Sechspaltenlayout, bei dem sechs Module nebeneinander angezeigt werden. Daher verwendet der Siteautor einen Container des Typs mit sechs Spalten darin.
- Ein Standortautor möchte ein Modul für eine Seite setzen, möchte aber sie nicht den Bildschirm ausfüllen. Daher wird der Siteautor das Modul einem Containermodul hinzufügen und legt die Eigenschaft **Breite** des Containers auf **Eingepasster Container** fest.

## <a name="container-module-properties"></a>Containermoduleigenschaften

| Eigenschaftenname     | Werte | Beschreibung |
|-------------------|--------|-------------|
| Überschrift           | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Eine optionale Überschrift kann für den Container bereitgestellt werden. Standardmäßig wird die **H2** Überschriftsmarkierung für die Überschrift verwendet. Die Markierung kann jedoch geändert werden, um Zugangsbedingungen zu erfüllen. |
| Breite             | **Eingepasster Container** oder **Bildschirm ausfüllen** | Wenn der Wert auf **Eingepasster Container** (der Standardwert) festgelegt ist, werden die Module im Containers auf die Breite des Containers beschränkt. Wenn der Wert auf **Bildschirm ausfüllen** gesetzt wird, werden die Module nicht auf die Containerbreite eingeschränkt und können den Bildschirm ausfüllen. |
| Spaltenanzahl | **1**, **2**, **3**, **4**, **6**, oder **12** | Diese Eigenschaft definiert die Anzahl der Spalten in Container. Ein Container kann bis 12 Spalten enthalten. |

## <a name="container-with-2-slots"></a>Container mit 2 Slots

Der Container vom Typ mit 2 Slots wird für ein Zwei-Spaltenlayout optimiert. Der Containertyp hat zwei Slots, um eine parallele Ansicht der Module zuzulassen, die sich darin befinden.

Zusätzliche Eigenschaften können verwendet werden, um das Layout für verschiedene Ansichtsports zu optimieren (mobile Geräte, Tablets, Computer, etc.) Für jeden Ansichtsport kann die Breite jeder Spalte definiert werden. Die folgende Spaltenbreiteneinstellungen sind verfügbar:

- **75%/25%** – Das erste Modul verfügt über eine Spaltenbreite von 75 Prozent, und das zweites Modul verfügt eine Spaltenbreite von 25 Prozent. Eine Option **25%/75%** steht auch zur Verfügung.
- **50%/50%** – Beide Module haben gleiche Spaltenbreite.
- **67%/33%** – Das erste Modul verfügt über eine Spaltenbreite von 67 Prozent, und das zweites Modul verfügt eine Spaltenbreite von 33 Prozent. Eine Option **33%/67%** steht auch zur Verfügung.
- **100%** – Beide Module haben eine volle Spaltenbreite. Daher werden die Module vertikal gestapelte in eine einzelne Spalte. Obwohl dieses einspaltige Layout dem Zweck des Containers mit 2 Slots widerspricht, kann es für einige Ansichtsports von Vorteil sein (beispielsweise, sehr kleine Viewports wie mobile Geräte).

### <a name="container-with-2-slots-properties"></a>Container mit 2 Sloteigenschaften

| Eigenschaftenname                   | Werte | Beschreibung |
|---------------------------------|--------|-------------|
| Überschrift                         | Überschriftentext und Überschriftsmarkierung | Eine optionale Überschrift kann für den Container bereitgestellt werden. |
| Sehr kleine Ansichtsportkonfiguration | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, oder **100%** | Diese Eigenschaft definiert das Layout für sehr kleine Ansichtsports. |
| Kleine Ansichtsportkonfiguration   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, oder **100%** | Diese Eigenschaft definiert das Layout für kleine Ansichtsports wie mobile Geräte. |
| Mittlere Ansichtsportkonfiguration  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, oder **100%** | Diese Eigenschaft definiert das Layout für mittlere Ansichtsports wie Tablets. |
| Große Ansichtsportkonfiguration   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, oder **100%** | Diese Eigenschaft definiert das Layout für große Ansichtsports wie Computer. |

## <a name="container-with-3-slots"></a>Container mit 3 Slots

Der Container vom Modultyp mit 3 Slots wird für ein Drei-Spaltenlayout optimiert.

Zusätzliche Eigenschaften können verwendet werden, um das Layout für verschiedene Ansichtsports zu optimieren. Für jeden Ansichtsport kann die Breite jeder Spalte definiert werden. Die folgende Spaltenbreiteneinstellungen sind verfügbar:

- **33%/33%/33%** – Alle drei Module haben gleiche Spaltenbreite.
- **50%/25%/25%** – Das erste Modul verfügt über eine Spaltenbreite von 50 Prozent, und jedes der beiden verbleibenden Module verfügt über eine Spaltenbreite von 25 Prozent. **25%/50%/25%** und **25%/25%/50%** Optionen stehen auch zur Verfügung.
- **16%/16%/67%** – Jede der ersten zwei Modul verfügt über eine Spaltenbreite von 16 Prozent, und das dritte Modul verfügt über eine Spaltenbreite von 67 Prozent. **16%/67%/16%** und **67%/16%/16%** Optionen stehen auch zur Verfügung.

### <a name="container-with-3-slots-properties"></a>Container mit 3 Sloteigenschaften

| Eigenschaftenname                   | Werte | Beschreibung |
|---------------------------------|--------|-------------|
| Überschrift                         | Überschriftentext und Überschriftsmarkierung | Eine optionale Überschrift kann dem Container hinzugefügt werden. |
| Sehr kleine Ansichtsportkonfiguration | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** oder **67%/16%/16%** | Diese Eigenschaft definiert das Layout für sehr kleine Ansichtsports. |
| Kleine Ansichtsportkonfiguration   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** oder **67%/16%/16%** | Diese Eigenschaft definiert das Layout für kleine Ansichtsports wie mobile Geräte. |
| Mittlere Ansichtsportkonfiguration  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** oder **67%/16%/16%** | Diese Eigenschaft definiert das Layout für mittlere Ansichtsports wie Tablets. |
| Große Ansichtsportkonfiguration   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** oder **67%/16%/16%** | Diese Eigenschaft definiert das Layout für große Ansichtsports wie Computer. |

## <a name="add-a-container-module-to-a-page"></a>Ein Containermodul einer neuen Seite hinzufügen

Um ein Containerspielmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Containervorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein Containermodul hinzu.
1. Im Containermodul fügen Sie ein Funktionsmodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Containervorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Containerseite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.
1. Im Eigenschaftenbereich für das Containermodul legen Sie die **Anzahl der Spalten** auf **1** die **Breite** auf **Eingepasster Container**.
1. Im Containermodul fügen Sie ein Funktionsmodul hinzu.
1. Im Eigenschaftenbereich für das Funktionsmodul konfigurieren Sie eine Überschrift.
1. Seite speichern und Vorschau anzeigen. Sie sollten ein Funktionsmodul sehen, das in die Breite des Containermoduls passt.
1. Im Eigenschaftenbereich für das Containermodul ändern Sie die **Anzahl der Spalten** auf **3**
1. Fügen Sie zwei weitere Funktionsmodule dem Containermodul hinzu.
1. Seite speichern und Vorschau anzeigen. Sie können drei Funktionsmodule sehen, die nebeneinander angezeigt werden.
1. Nachdem Sie das Layout erstellt haben, das Sie möchten, laden Sie die Seite hoch und veröffentlichen diese.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Karussellmodul](add-carousel.md)

[Umfangreiches Inhaltsblockmodul](add-content-rich-block.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
