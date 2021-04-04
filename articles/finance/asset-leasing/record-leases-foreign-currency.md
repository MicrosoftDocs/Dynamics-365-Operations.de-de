---
title: Leasingobjekte in Fremdwährungen erfassen
description: In diesem Thema wird erläutert, wie Mietverträge in anderen Währungen als der Buchhaltungs- oder Berichtswährung erfasst werden.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fd4d04ae7e89b8ce41ed745c643b8e736484789d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241489"
---
# <a name="record-leases-in-foreign-currencies"></a>Leasingobjekte in Fremdwährungen erfassen

[!include [banner](../includes/banner.md)]

Anlagenleasingkonten für Mietverträge, die in anderen Währungen als der Buchhaltungswährung oder der Berichtswährung geführt werden, werden auf der **Sachkontoeinstellung**-Seite erstellt. Alle Mietverträge sollten in ihrer Transaktionswährung eingegeben werden. Mit anderen Worten, sie sollten in der Währung eingegeben werden, die im Mietvertrag angegeben ist. In diesem Thema wird erläutert, wie Mietverträge in anderen Währungen als der Buchhaltungs- oder Berichtswährung erfasst werden.

Wenn Sie einen Mietvertrag in einer Fremdwährung abschließen, wird der Vermögenswert des Nutzungsrechts am Leasingobjekt sowohl in der Rechnungswährung als auch in der Berichtswährung abgeschrieben. Diese Währungen werden auf der **Sachkontoeinstellung**-Seite konfiguriert. Dieses Verhalten wird auch im Anlagevermögen verwendet. Wenn Sie einen Mietvertrag in einer Fremdwährung erstellen, wählen Sie die Transaktionswährung im **Währung**-Feld.

Der Wechselkurs der Rechnungswährung ist der Standardwert im **Wechselkurstyp der Buchhaltungswährung**-Feld. Der Wechselkurs der Berichtswährung ist der Standardwert im **Wechselkurstyp der Berichtswährung**-Feld. Diese Wechselkurse waren zum Beginn des Mietvertrags wirksam. Die Felder **Wechselkurs der Buchhaltungswährung** und **Wechselkurs der Berichtswährung** befinden sich im Inforegister **Informationen zum Finanz- und Berichtsaustausch** auf der **Details zum Mietvertrag**-Seite.

1. Aktivieren Sie das Kontrollkästchen **Fester Wechselkurs**, um den automatisch eingegebenen Wechselkurs zu überschreiben, und geben Sie dann den neuen Wechselkurs ein.
2. Geben Sie in die anderen Felder die Informationen ein, die für den Mietvertrag erforderlich sind, und wählen Sie dann **Zeitpläne erstellen**.
3. Wählen Sie auf der neuen **Details zum Mietvertrag**-Seite **Bücher**.
4. Überprüfen Sie auf der **Leasingbuch**-Seite auf der **Informationen zum Finanz- und Berichtsaustausch** Registerkarte die Werte der Felder **Buchhaltungswährung bei anfänglichen Nutzungsrecht am Leasingobjekt** und **Berichtswährung bei anfänglichen Nutzungsrecht am Leasingobjekt**. In jedem dieser Felder wird die umgerechnete Bilanz für das Nutzungsrecht am Leasingobjekt in der entsprechenden Währung angezeigt. Diese Felder werden aktualisiert, wenn Sie Finanzinformationen ändern. Wählen Sie **Zeitpläne erstellen**, bevor Sie den Zahlungsplan bestätigen.

    Der Journaleintrag der erstmaligen Erfassung erfasst das Nutzungsrecht am Leasingobjekt, das die im Mietvertrag aufgeführten Wechselkurse verwendet. Der Journaleintrag enthält auch die Werte der Felder **Buchhaltungswährung für anfängliches Nutzungsrecht am Leasingobjekt** und **Berichtswährung für anfängliches Nutzungsrecht am Leasingobjekt**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Nachträgliche Bewertung von Mietverträgen in Fremdwährung

Der Abschreibungsplan zeigt die erwarteten Abschreibungsaufwandsbeträge in der Berichtswährung, der Buchhaltungswährung und der Transaktionswährung.

Um die Bilanz des Nutzungsrechts am Leasingobjekt und die Abschreibungsbeträge entweder in der Berichtswährung oder in der Buchhaltungswährung anzuzeigen, öffnen Sie die **Abschreibungsplan für Anlagen**-Seite und aktivieren Sie die Kontrollkästchen **Buchhaltungswährungsbeträge anzeigen** oder **Berichtswährungsbeträge anzeigen**.

Wenn Sie die Journaleinträge für Abschreibungskosten für einen Mietvertrag erstellen, der auf eine Fremdwährung lautet, verwendet der Eintrag die Wechselkurse, die im Mietvertrag aufgeführt sind. Er verwendet auch die Werte der Felder **Buchhaltungswährung für anfängliches Nutzungsrecht am Leasingobjekt** und **Berichtswährung für anfängliches Nutzungsrecht am Leasingobjekt**.

Der endgültige Abschreibungsaufwand kann unter Verwendung eines geringfügig anderen Wechselkurses berechnet werden, sodass das Nutzungsrecht am Leasingobjekt sowohl in der Rechnungswährung als auch in der Berichtswährung vollständig abgeschrieben wird.

Wenn der Mietvertrag als **Zurückgestellter Mietaufwand** umgegliedert wurde, löscht das System automatisch die Wechselkurse der Buchhaltungs- und Berichtswährungen, sofern diese bereits definiert wurden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]