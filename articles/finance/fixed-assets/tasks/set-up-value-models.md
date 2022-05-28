---
title: Wertmodelle einrichten
description: Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71d256b600956a4e525cde626c958713f6258f5a
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727060"
---
# <a name="set-up-value-models"></a>Wertmodelle einrichten

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen.

## <a name="create-a-book"></a>Buch erstellen
1. Wechseln Sie zu **Anlagen \> Einstellungen \> Bücher**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Bücher** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.
5. Legen Sie die Option **Abschreibung berechnen** auf **Ja** fest.

    Wenn die Option **Abschreibung berechnen** auf **Ja** gesetzt ist, wird das zugehörige Anlagenbuch in die Abschreibungsvorschläge aufgenommen. Wenn **Nein** ausgewählt ist, wird die Anlagebuch nicht automatisch abgeschrieben.

6. Geben Sie im Feld **Abschreibungsprofil** einen Wert ein, oder wählen Sie einen Wert aus.

    * Ein alternatives Abschreibungsprofil ist auch als eine Switchover-Methode der Abschreibung bekannt. Der Abschreibungsvorschlag schaltet auf dieses Profil um, wenn das alternative Profil einen Abschreibungsbetrag berechnet, der gleich oder größer ist, als das standardmäßiges "Abschreibungsprofil".
    * Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet. Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.
    * Wenn Sie die Option **Abschreibungsregulierungen mit Basisregulierungen erstellen** auswählen, werden Abschreibungsregulierungen automatisch erstellt, wenn der Wert einer Anlage aktualisiert wird. Andernfalls wirkt sich der aktualisierte Anlagenwert nur auf zukünftige Abschreibungsberechnungen aus.

7. Wählen Sie im Feld **Abschreibungsregulierungen mit Basisregulierungen erstellen** die Option **Ja** aus.

    * Standardmäßig werden Anlagenbuchtransaktionen im Hauptbuch gebucht. Sie können aber Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld **Ins Hauptbuch buchen** auf **Nein** festlegen. Bücher, die nicht im Hauptbuch gebucht werden, werden in der Regel für die Steuererklärung verwendet. Dies bietet Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da die Transaktionen nicht im Hauptbuch eingerichtet wurden.
    * Das Feld **Buchungsebene** wird standardmäßig auf **Aktuelle Ebene** festgelegt, wenn das Buch im Hauptbuch bucht, und auf **Keine**, wenn es nicht im Hauptbuch bucht. Aktualisieren Sie den Wert des Felds **Buchungsebene**, wenn Sie benötigen, dass Transaktionen für dieses Buch zu einer anderen Ebene gebucht werden.

8. Positive Abschreibung berechnen

    * Standardmäßig ist die Option **Positive Abschreibung berechnen** auf **Nein** festgelegt. Diese Einstellung gibt an, dass die Abschreibung dem ausgewählten Anlagenbuch gutgeschrieben wird. Zusätzlich sind die Optionen **Nettobuchwert höher als Anschaffungspreis zulassen** und **Negativen Nettobuchwert zulassen** beide auf **Nein** eingestellt, und die Einstellungen können unabhängig geändert werden. 
    * Setzen Sie die Option **Positive Abschreibung berechnen** auf **Ja**, um die positive Abschreibung zu berechnen. Diese Einstellung gibt an, dass die Abschreibung das Anlagenbuch belastet. Wenn die Option **Positive Abschreibung berechnen** auf **Ja** eingestellt ist, werden die Optionen **Nettobuchwert höher als Anschaffungspreis zulassen** und **Negativen Nettobuchwert zulassen** automatisch auf **Ja** gesetzt und gesperrt. Diese Sperre trägt dazu bei, dass positive Abschreibungen nur auf Anlagen vorgenommen werden, die mit negativem Buchwert (Guthaben) erworben wurden. 

10. Geben Sie im Feld **Kalender** einen Wert ein oder wählen Sie einen Wert aus.

    Abgeleitete Bücher buchen Translationen für verschiedene Bücher gleichzeitig. Sie erstellen die Buchungen mit dem primären Buch und während der Buchung wird eine genaue Kopie der Buchung im abgeleiteten Abschreibungsbuch gebucht. Es gibt keine Neuberechnung bei den Transaktionen im abgeleiteten Buch. Sie sollten diese nicht für Abschreibungsbuchungen verwenden.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Buch einer Anlagengruppe zuordnen

1. Wählen Sie **Anlagengruppen**.
2. Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus.
3. Geben Sie im Feld **Nutzungsdauer** eine Zahl ein.

    * Periodische Abschreibungen werden berechnet, nachdem die Nutzungsdauer der Anlage eingegeben wurde.
    * Die Abschreibungskonvention kann wie für Steuerzwecke erforderlich festgelegt werden.
    * Bei Anlagen, die mit Leasingverträgen verbunden sind, wird der Wert im Feld **Nutzungsdauer** durch den kleineren Wert von entweder der Leasingdauer im Anlagenbuch oder der Nutzungsdauer der Anlage außer Kraft gesetzt. Wenn die Option **Eigentumsübergang** für das Leasingbuch auf **Ja** festgelegt ist, entspricht der Wert im Feld **Nutzungsdauer** immer der Nutzungsdauer der Anlage.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
