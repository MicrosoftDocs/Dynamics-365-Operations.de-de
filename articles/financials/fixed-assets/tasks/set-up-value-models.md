---
title: Wertmodelle einrichten
description: Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a528bd12552d5ce100027c9a789f6e1bdc597b66
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839760"
---
# <a name="set-up-value-models"></a>Wertmodelle einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen. Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.


## <a name="create-a-book"></a>Buch erstellen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Bücher".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld 'Buch' einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Wenn "Abschreibung berechnen" ausgewählt ist, werden die zugeordneten Anlagenbuch in die Abschreibungsvorschläge einbezogen. Wenn dies nicht ausgewählt ist, wird die Anlagebuch nicht automatisch abgeschrieben.  
5. Wählen Sie "Ja" im Feld "Ermittelte Abschreibung" aus.
6. Geben Sie im Feld 'Abschreibungsprofil' einen Wert ein, oder wählen Sie einen Wert aus.
    * Ein alternatives Abschreibungsprofil ist auch als eine Switchover-Methode der Abschreibung bekannt. Der Abschreibungsvorschlag schaltet auf dieses Profil um, wenn das alternative Profil einen Abschreibungsbetrag berechnet, der gleich oder größer ist, als das standardmäßiges "Abschreibungsprofil".  
    * Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet. Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.  
    * Wenn die Option "Abschreibungsregulierungen mit Basisregulierungen erstellen" ausgewählt ist, werden Abschreibungsregulierungen automatisch erstellt, wenn der Wert einer Anlage aktualisiert wird. Wenn sie nicht ausgewählt ist, wird der aktualisierte Anlagewert sich nur auf die Abschreibungsberechnungen ausgehend vom heutigen Datum auswirken.  
7. Wählen Sie "Ja" im Feld "Abschreibungsregulierungen mit Basisregulierungen erstellen".
    * Standardmäßig werden Anlagenbuchtransaktionen im Hauptbuch gebucht. Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld "Ins Hauptbuch buchen" auf Nein festlegen. Bücher, die nicht im Hauptbuch buchen, werden in der Regel für die Steuererklärung verwendet. Dies bietet zusätzliche Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da sie nicht im Hauptbuch eingerichtet wurden.  
    * Die Buchungsebene wird standardmäßig auf die aktuellen Ebene festgelegt, wenn das Buch im Hauptbuch bucht, und auf "Keine", wenn es nicht im Hauptbuch bucht. Aktualisieren Sie die "Buchungsebene", wenn Sie benötigen, dass Transaktionen für dieses Buch zu einer anderen Ebene gebucht werden.  
8. Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.
    * Abgeleitete Bücher buchen Translationen für verschiedene Bücher gleichzeitig. Sie erstellen die Buchungen mit dem primären Buch und während der Buchung wird eine genaue Kopie der Buchung im abgeleiteten Abschreibungsbuch gebucht. Es gibt keine Neuberechnung bei den Transaktionen im abgeleiteten Buch. Sie sollten diese nicht für Abschreibungsbuchungen verwenden.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Buch einer Anlagengruppe zuordnen
1. Klicken Sie auf "Anlagengruppen".
2. Geben Sie im Feld "Anlagengruppe" einen Wert ein oder wählen Sie einen Wert aus.
3. Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.
    * Beachten Sie, dass Abschreibungszeiträume nach der Festlegung der Nutzungsdauer berechnet wird.  
    * Sie können die Abschreibungskonvention für Steuerzwecke bei Bedarf festlegen.  

