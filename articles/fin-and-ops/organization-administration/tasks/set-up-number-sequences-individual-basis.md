---
title: Nummernkreise einzeln einrichten
description: In diesem Thema wird erläutert, wie Sie Nummernkreise einzeln einrichten.
author: sericks007
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58e69b680c006c814e9408135b6947161ad7c4f3
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738880"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Nummernkreise einzeln einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Sie Nummernkreise einzeln einrichten. Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Kennungen für Masterdaten- und Buchungsdatensätze, die diese benötigen. Ein Masterdaten- oder Buchungsdatensatz, der eine Kennung erfordert, wird als Referenz bezeichnet. Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden. Mit dem Assistenten **Nummernkreise einrichten** können alle erforderlichen Nummernkreise gleichzeitig eingerichtet werden. Mit der Seite **Nummernkreise** können Sie einzelne Nummernkreise einrichten.

1. Wechseln Sie zu **Navigationsbereich > Module > Organisationsverwaltung > Nummernkreise > Nummernkreise**.
2. Wählen Sie **Nummernkreis** aus.
3. Geben Sie im Feld **Nummernkreiscode** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie auf dem Inforegister **Bereichsparameter** einen Bereich für den Nummernkreis aus, und wählen Sie Bereichswerte in der Dropdownliste aus. Mit dem Bereich wird definiert, welche Organisationen den Nummernkreis verwenden. Nummernkreise mit einem anderen Bereich als **Freigegeben** können Segmente enthalten, die ihrem Bereich entsprechen. Ein Nummernkreis mit dem Bereich **Juristische Person** kann beispielsweise ein Segment für juristische Personen enthalten. Weitere Informationen zu Bereichen finden Sie unter [Überblick über Nummernkreise](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/fin-and-ops/organization-administration/number-sequence-overview.md).  
6. Erweitern Sie den Abschnitt **Segmente**.
    - Definieren Sie das Format für den Nummernkreis, indem Sie Segmente hinzufügen, entfernen und neu anordnen.  
    - Nummernkreise aller Bereiche können *konstante Segmente* und *alphanumerische Segmente* enthalten. Konstante Segmente enthalten einen Satz alphanumerischer Zeichen, die sich nicht ändern. Fügen Sie mithilfe dieses Segmenttyps einen Bindestrich oder andere Trennzeichen zwischen Nummernkreissegmenten hinzu. Alphanumerische Segmente enthalten eine Kombination aus Nummernzeichen (#) und kaufmännischen Und-Zeichen (&). Diese Zeichen stellen Buchstaben und Zahlen dar, die jedes Mal schrittweise erhöht werden, wenn eine Nummer aus dem Nummernkreis verwendet wird. Verwenden Sie ein Nummernzeichen (#) zur Angabe inkrementeller Nummern und ein kaufmännisches Und-Zeichen zur Angabe inkrementeller Buchstaben. Mit dem Format `#####_2014` wird beispielsweise der Nummernkreis `00001_2014`, `00002_2014` usw. erstellt. Mindestens ein alphanumerisches Segment muss vorhanden sein. Bereichssegmente, z. B. ein Unternehmen oder eine juristische Person, sind nicht erforderlich. Doch wenn Sie keine Bereichssegmente in das Format einschließen, werden Nummern für die ausgewählte Referenz dennoch pro Bereich generiert.  
7. Erweitern Sie den Abschnitt **Referenzen**. Wählen Sie den Dokumenttyp oder Datensatz aus, dem dieser Nummernkreis zugeordnet werden soll. Dieser Schritt ist für Nummernkreise, die für spezielle Anwendungsverwendungsmuster definiert werden, optional. In diesen Szenarien wird eine neue Nummer generiert, indem der Wert eines Nummernkreiscodes oder einer Nummernkreiskennung, aber keine Referenz verwendet wird. Ein Beispiel für ein spezielles Anwendungsverwendungsmuster sind Belegnummern, die für bestimmte Journale verwendet werden. Es wird jedoch nicht empfohlen, solche Muster zu verwenden.  
8. Erweitern Sie den Abschnitt **Allgemein**. Geben Sie auf dem Inforegister "Allgemein" an, ob der Nummernkreis manuell und fortlaufend bzw. nicht fortlaufend ist. Geben Sie zudem die niedrigste und die höchste Nummer ein, die in einem Nummernkreis verwendet werden kann. Es wird nicht empfohlen, einen nicht fortlaufenden Nummernkreis zu einem fortlaufenden Nummernkreis zu ändern. Der Nummernkreis wird nicht tatsächlich fortlaufend sein. Diese Änderung führt möglicherweise auch zu Doppelschlüssel-Verstößen in der Datenbank. Zudem besitzen fortlaufende Nummernkreise eine größere Auswirkungen auf die Leistung.   
9. Klicken Sie auf **Speichern**.

