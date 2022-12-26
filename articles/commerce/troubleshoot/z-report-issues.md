---
title: Probleme mit dem Datenabgleich eines Z-Berichts
description: Dieser Artikel beschreibt Probleme, die bei der Datenabstimmung eines Z-Berichts in Commerce headquarters auftreten können. Es beschreibt auch mögliche Grundursachen und Lösungen, die dazu beitragen können, zukünftige Vorkommnisse zu verhindern.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832139"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Probleme mit dem Datenabgleich eines Z-Berichts

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn beim Datenabgleich eines Z-Berichts in der Microsoft Dynamics 365 Commerce headquarters Probleme auftreten. Es beschreibt Probleme, auf die Benutzer möglicherweise beim Datenabgleich stoßen, mögliche Ursachen und Lösungen, die dazu beitragen können, zukünftige Vorkommnisse zu verhindern.

## <a name="description"></a>Description

- Es gibt eine Diskrepanz zwischen den Beträgen, die im Z-Bericht angezeigt werden, und den Summen, die auf dem berechneten Auszug angezeigt werden.
- Die Transaktion in der Zentrale weist eine falsche Anzahl von Einzelposten auf, oder es gibt eine Diskrepanz zwischen der Gesamtsumme der Position und der Gesamtsumme für die Transaktion.
- Die Anzahl der Transaktionen, die in einer Schicht in der Zentrale angezeigt werden, ist geringer als die Anzahl der Transaktionen im Z-Bericht.
- Auszugsbuchung ist aus einem der oben genannten Gründe fehlgeschlagen.

### <a name="root-cause"></a>Tiefere Ursache

Die häufigste Ursache für die zuvor beschriebenen Symptome ist die Generierung doppelter Transaktions-IDs in der Kanaldatenbank. Doppelte Transaktions-ID können aus folgenden Gründen nicht generiert werden:

- Der lokale Datenbankspeicher von Modern Point of Sale (MPOS) ist beschädigt.
- MPOS hat einige Transaktionen im Offline-Modus und wird reaktiviert, indem ein Konto verwendet wird, das keinen Zugriff auf die Offline-Datenbank hat.
- Es gibt ein Problem mit der Anpassung, das mit der Generierung von Transaktions-IDs zusammenhängt.

## <a name="resolution"></a>Lösung

Normalerweise verlässt sich Commerce auf eine Zahlenfolge, um fortlaufende Transaktions-IDs zu generieren. Wenn das System aus irgendeinem Grund nicht feststellen kann, dass ein Nummernkreis verwendet wurde, wird eine doppelte Transaktions-ID generiert. 

Um das Problem mit der doppelten Transaktions-ID zu beheben, erstellen Sie ein Support-Ticket, um zu prüfen, ob die Transaktionsdaten behoben werden können. In einigen Fällen, z. B. wenn in der Zentrale kein Datenverlust vorliegt, ist keine Datenkorrektur möglich oder erforderlich.

Um dieses Problem in Zukunft zu vermeiden, müssen Sie die Funktion **Neue Transaktions-ID aktivieren, um doppelte Transaktions-IDs zu vermeiden** in headquarters aktivieren. Diese Funktion wurde in die Commerce-Version 10.0.19 eingeführt. Es hilft, die Erstellung fortlaufender Transaktions-IDs zu verhindern, indem sichergestellt wird, dass für jede Transaktion eine eindeutige Transaktions-ID erstellt wird. Weitere Informationen zu dieser Funktion finden Sie unter [Doppelte Transaktions-ID verhindern](../channel-setup-retail.md#ensure-unique-transaction-ids).
