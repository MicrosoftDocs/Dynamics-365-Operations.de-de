---
title: "Buchen mit abgeleiteten Büchern"
description: "Dieser Artikel beschreibt, wie Sie die abgeleiteten Bücher verwenden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0afefcbdbea963bf110555bdc80235e071ea4c3e
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="post-with-derived-books"></a>Buchen mit abgeleiteten Büchern

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt, wie Sie die abgeleiteten Bücher verwenden.

Beim Buchen einer Transaktion für ein Buch, das abgeleitete Bücher enthält, werden die Transaktionen für das abgeleitete Buch automatisch aus Erfassungen, Bestellungen oder Freitextrechnungen gebucht. Wenn Sie die primären Buchtransaktionen in der Anlagenerfassung vorbereiten, können Sie die Beträge der abgeleiteten Buchungen anzeigen und ändern, bevor diese gebucht werden.
-   Bestimmte Konten wie Mehrwertsteuer-, Debitoren- oder Kreditorenkonten werden nur einmal durch Buchung des primären Buchs aktualisiert. Buchungen für Transaktionen im abgeleiteten Buch erfolgen auf Konten, die hierfür auf der Seite Anlagenbuchungsprofile definiert wurden.
-   Akquisitionen werden oftmals als Buchungsart für das abgeleitete Buch verwendet. Diese Buchungsart wird verwendet, wenn das Wertmodell und das abgeleitete Abschreibungsbuch ab dem Zeitpunkt der Anschaffung auf eine Anlage angewendet werden sollen.
-   Für die Buchungsart können auch andere Werte zutreffend sein. Besitzen das primäre Buch und das abgeleitete Buch beispielsweise die gleichen Kauf- oder Abgangsintervalle, stehen bei der Einrichtung eines abgeleiteten Abschreibungsbuchs alle Anlagenbuchungsarten zur Verfügung.

> [!WARNING]
> Der Abschreibungsbetrag, der im abgeleiteten Buch gebucht wird, ist der gleiche wie der für das primäre Buch gebuchte. Wenn die Abschreibungsmethoden zwischen den Büchern unterschiedlich sind, sollten Sie keine Abschreibungsbuchungen mit dem Ableitungsverfahren generieren. |

## <a name="example"></a>Beispiel 
Nachfolgend wird beschrieben, wie Anschaffungsbuchungen mit der Funktion für abgeleitete Buchfunktionalitäten eingerichtet werden.

1.  Erstellt die Bücher auf der Buchseite.
    -   Das Buch für die Buchhaltung: WM 1, aktuelle Buchungsebene
    -   Das Buch für steuerliche Zwecke: WM 2, Steuerbuchungsebene

2.  Klicken Sie für WM 1 auf die Registerkarte "Abgeleitetes Buch". Wählen Sie WM 2 im Buchfeld und Anschaffung im Feld Transaktionstyp.

Das Buch kann nun bestimmten Anlagen zugeordnet werden. 

Wenn für eine Anlage mit Wertmodell WM 1 eine Anschaffung gebucht wird, wird diese Anschaffung nicht nur für WM 1, sondern auch im abgeleiteten Abschreibungsbuch WM 2 gebucht. Der Status beider Anlagenwertbücher wird auf Offen aktualisiert.

> [!NOTE]                                                                                                         
> Wenn Sie nicht mit abgeleiteten Abschreibungsbüchern arbeiten, müssen Sie die Anschaffung der Anlage sowohl für Buch WM 1 als auch für Abschreibungsbuch WM 2 buchen.

Weitere Informationen finden Sie unter [Abgeleitete Bücher](derived-books.md).




