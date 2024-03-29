---
title: Übergeben von zurückgelieferten Artikeln zur Prüfung
description: Beim Erfassen eines zurückgelieferten Artikels können Sie festlegen, dass ein Artikel zur Prüfung gesendet wird, bevor er an das Lager zurückgegeben oder anderweitig veräußert wird.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 959df8e1ecbc493dc11e4793120f352b94b8b635
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676746"
---
# <a name="pass-returned-items-on-to-inspection"></a>Übergeben von zurückgelieferten Artikeln zur Prüfung 

[!include [banner](../includes/banner.md)]


Beim Erfassen eines zurückgelieferten Artikels können Sie festlegen, dass ein Artikel zur Prüfung gesendet wird, bevor er an das Lager zurückgegeben oder anderweitig veräußert wird.

1.  Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Wareneingang**.
    
    \-oder-
    
    Klicken Sie auf **Lagerverwaltung** \> **Journaleinträge** \> **Wareneingang** \> **Produktions-Wareneingang**.

2.  Erfassen Sie den Zugang eines Artikels wie gewohnt im Formular **Lagerplatzerfassung**.
    

    > [!NOTE]
    > <P>Informationen zum Erfassen des Zugangs zurückgelieferter Artikel finden Sie, <A href="register-the-receipt-of-returned-items.md">Erfassen des Empfangs zurückgelieferter Artikel</A></P>



3.  Auf der Registerkarte **Standardwerte** im Bereich **Handhabungsmodus**, wählen Sie das Feld **Quarantäneverwaltung** aus.

Damit wird das System aufgefordert, einen Quarantäneauftrag zu erstellen, und die Person bzw. die Abteilung, die Prüfungen durchführt, antwortet auf diesen Auftrag mithilfe des Formulars **Quarantäneauftrag**.

## <a name="see-also"></a>Siehe auch

[Prüfen von zurückgelieferten Artikeln](take-returned-items-through-inspection.md)

[Angeben zur Entsorgung zurückgelieferter Artikel](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]