---
title: Fertigmeldungen für Stücklisten ausführen
description: Dieser Artikel enthält Informationen zum Berichten von Stücklisten als fertig.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMReportFinish, BOMReportFinishMax, BOMSetupReportFinish
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c68ff6fdb77cb8de23b6b803b0300c6daa0fd106
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428995"
---
# <a name="report-boms-as-finished"></a>Fertigmeldungen für Stücklisten ausführen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zum Berichten von Stücklisten als fertig.

Die Seiten **Fertigmeldung** und **Retrograd nach Lagermengen** werden verwendet, um Stücklisten (BOMs) als fertig zu melden. Konzeptionell ist der Vorgang für das Fertigmelden einer Stückliste derselbe wie beim Fertigmelden eines Produktionsauftrags. Dieser Vorgang kann zum Beispiel bei einfachen Montage- und Bausatzprozessen genutzt werden, bei denen die erweiterten Fähigkeiten von Produktionsaufträgen nicht erforderlich sind. Mit der **Fertigmeldung** Seite können Sie mehrere Stücklisten in einer Charge als fertig melden. Die **Retrograd nach Lagermengen** Seite können Sie nur eine Stückliste zu melden, wie auf einmal abgeschlossen. Die **Als fertig melden** Seite ist über eine Menüoption in der Lagerverwaltung und verfügbar, da beide Seiten sind auf die Menüoptionen **Freigegebene Produkte** Seite verfügbar.

## <a name="report-as-finished-page"></a>Seite Fertigmeldung
Wenn Sie die Seite **Fertigmeldung** aus einem freigegebenen Produkt öffnen, schlägt die Seite vor, dass Sie die Standardbestands-Standardmenge als fertig melden. Standardmäßig wird die aktive Stücklistenversion angezeigt, aber Sie können die Stücklistenversion ändern, wenn es andere genehmigte Versionen gibt. Mit der Seite können Sie Datensätze auch löschen und neue Datensätze für freigegebene Produkte erstellen, die als fertig gemeldet werden sollen. Um eine Abfrage zur Auswahl von Produkten zu verwenden, klicken Sie auf die Menüoption **Auswählen**. Sie können Berichterstellung für die ausgewählten Produkte manuell als fertig bestätigen, indem Sie auf **OK** klicken. Alternativ können Sie den Prozess so einrichten, dass er in einem Stapel ausgeführt wird. Wenn der Fertigmeldungsvorgang bestätigt wird, erstellt das System eine Stücklistenerfassung, in der die Buchung zum Bestand verarbeitet wird. Diese Erfassung besteht aus einer Positionsartikel für das Produkt und einem Positionsartikel für jede Stücklistenposition. Sie können steuern, ob die Erfassung automatisch gebucht wird, oder ob sie für zusätzliche Regulierungen übrig gelassen wird.

## <a name="max-report-as-finished-page"></a>Retrograd nach Lagermengen
Auf der Seite **Retrograd nach Lagermengen** gibt jede Stücklistenposition die Stückanzahl des Produkts an, die als fertig gemeldet werden können. Diese Berechnung basiert auf dem physischen verfügbaren Lagerbestand jeder Materialposition. Im folgenden Beispiel zur Produktion verbraucht die Artikelnummer FG zwei Stück Rohmaterial RM10 und ein Stück des Rohmaterials RM20. Da nur 10 Stück RM10 am Lager vorhanden sind, beträgt die Höchstmenge von FG, die als fertig gemeldet werden kann, fünf Artikel. Dieser Wert wird im Feld **Retrograd nach Lagermengen** angezeigt.

| Ebene | Artikelnummer | Menge | Bestand | Retrograd Fertigmeldung |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Stücklisten, die mehrere Ebenen besitzen
Wenn eine Stückliste mehrere Ebenen hat, können Sie steuern, wie Materialien auf allen Ebenen berücksichtigt werden, indem Sie das Feld **Stücklistenauflösung** verwenden. Dieses Feld steht sowohl auf der Seite **Fertigmeldung** als auch auf der Seite **Retrograd nach Lagermengen** zur Verfügung. Die folgenden Optionen sind verfügbar:

-   **Nie** – Zugrunde liegende Stücklisten werden nicht aufgelöst, wenn ein Materialengpass vorliegt.
-   **Immer** – Alle zugrunde liegenden Stücklisten werden vollständig aufgelöst. Daher werden keine freien verfügbaren Lagerbestände für halbfertige Komponentenartikel verwendet.
-   **Engpass** – Zugrunde liegende Stücklisten werden nur aufgeschlüsselt, wenn die erforderliche Menge des Materials nicht vollständig verfügbar ist.

### <a name="example"></a>Beispiel

In diesem Beispiel sind drei Stück des Fertigprodukts (Artikelnummer FG) bereit, um als fertig gemeldet zu werden. Es gibt eine Stückliste mit zwei Ebenen, wie hier angezeigt.

| Ebene | Artikelnummer | Stücklistenpositionsmenge | Bestand |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Die folgenden Tabellen enthalten Informationen dazu, wie der **Auflösung** Einstellung im Feld die Methode betroffen, dass Stücklistenerfassungspositionen generiert werden. **Auflösung: Nie**

| Ebene | Artikelnummer | Menge |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Während weiter Tabelle steht nur, Artikelnummer COMP als abgezogen in der Erfassung wird. Artikelnummer RM, die Teil von COMP ist, darf der Erfassungsposition und zu den beiden verfügbaren Artikel von berücksichtigt. Zunächst werden nicht aufgelöst. **Auflösung: Immer**

| Ebene | Artikelnummer | Menge |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

In diesem Fall wird Artikelnummer COMP in das Rohmaterial mit der Artikelnummer RM aufgelöst. Die beiden verfügbaren Teile von COMP werden nicht in der verwertbaren Menge von RM berücksichtigt. **Auflösung: Mangel**

| Ebene | Artikelnummer | Menge |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

In diesem Fall werden die zwei verfügbaren Artikel aus Artikelnummer COMP berücksichtigt. Da jedoch drei Stück der Artikelnummer FG erforderlich sind, ist zur Produktion auch ein Stück der Artikelnummer RM erforderlich, um das zusätzliche Stück von COMP zu fertigen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]