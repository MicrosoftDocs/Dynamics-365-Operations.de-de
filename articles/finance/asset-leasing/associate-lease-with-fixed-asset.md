---
title: Anlagevermögen mit einem Mietvertrag verknüpfen
description: In diesem Thema wird erläutert, wie Sie eine vorhandene Anlage einem neuen Mietvertrag zuordnen.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0e2261755d98ee38564b4b864daf8e79551d1239
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814079"
---
# <a name="associate-fixed-assets-with-leases"></a>Anlagevermögen mit einem Mietvertrag verknüpfen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine vorhandene Anlage einem neuen Mietvertrag zuordnen. Wenn Sie eine Anlage einem Mietvertrag verknüpfen, entspricht der Wert des Nutzungsrechts am Leasingobjekt bei der erstmaligen Erfassung den Anschaffungskosten der Anlage.

Bevor Sie eine Anlage einem Mietvertrag zuordnen können, müssen Sie im Anlagevermögen einen Datensatz für das Anlagevermögen erstellen. Dann müssen Sie auf der **Mietvertragsübersicht** Seite einen Mietvertrag erstellen und die Anlage mit damit verknüpfen.

1. Fügen Sie einen Mietvertrag hinzu, indem Sie die Schritte in [Mietverträge hinzufügen oder kopieren](add-lease.md) ausführen. Wählen Sie auf der **Mietvertrag hinzufügen**-Seite im Feld **Anlagennnummer** die Anlage aus, die noch nicht erworben wurde.
2. Wählen Sie **Bücher** und bestätigen Sie den Zahlungsplan.
3. Wählen Sie **Erstmalige Erfassung**.
4. Wählen Sie **Erfassung für Anlagenleasing**.

    Der Journaleintrag der erstmaligen Erfassung für den Mietvertrag belastet die Anlage mit dem Betrag, der normalerweise dem Konto für das Nutzungsrecht am Leasingobjekt belastet wird.

    Sie können jetzt die Transaktionsart anzeigen und für die Anlage buchen.

5. Wählen Sie **Erfassungsdetails**.
6. Wählen Sie **Zeilen**, um die einzelnen Zeilen für den Journaleintrag anzuzeigen.
7. Wählen Sie die Erfassungszeile aus, die die Anlage enthält, und wählen Sie dann die Registerkarte **Anlagevermögen** aus.

    Die Registerkarte **Anlagevermögen** zeigt die Transaktionsart und das Buch. Standardmäßig ist das **Transaktionart**-Feld auf **Anschaffung** festgelegt, und das **Buch**-Feld wird auf das aktuelle Buch für die Anlage gesetzt.

Nachdem Sie den Journaleintrag der erstmaligen Erfassung gebucht haben, wird die Transaktion als Anschaffungstransaktion für die Anlage angezeigt. Um die Transaktionstabelle anzuzeigen, gehen Sie zu **Anlagevermögen \> Anlagevermögen \> Anlagevermögen**, wählen Sie die entsprechende Anlage und dann **Bewertungen** aus. Sie sollte sehen, dass der Journaleintrag der erstmaligen Erfassung eine Anschaffungstransaktion für die angegebene Anlage erstellt hat.

Die Anlage kann jetzt mithilfe der Standardabschreibungsfunktion im Anlagevermögen abgeschrieben werden. Weitere Informationen zur Abschreibung finden Sie untere [Abschreibungsmethoden und - konventionen](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Wenn Sie eine Anlage mit einem Mietvertrag verknüpfen, wird die **Anlagenabschreibung** und **Leasingminderung** Schaltflächen im Anlagenvermögen deaktiviert. Sie können Transaktionen zur Anlagenabschreibung und zur Leasingminderung im Anlagevermögen anzeigen. Die **Anlagentransaktionen**-Schaltfläche, mit der ein Anfrageformular geöffnet wird, ist ebenfalls deaktiviert. Sie können auch das **Anlagentransaktionen** -Anfrageformular im Anlagevermögen öffnen.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]