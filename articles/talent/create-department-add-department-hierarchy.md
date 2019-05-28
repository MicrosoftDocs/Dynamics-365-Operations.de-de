---
title: Abteilungen erstellen und sie in die Abteilungshierarchie einbeziehen
description: Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig. Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden. Abteilungen können Gewinn- und Verlustzuständigkeit haben.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 7b6308c54d237d0d7558fc1f94647f7ca1ab82a1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506173"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Abteilungen erstellen und sie in die Abteilungshierarchie einbeziehen

[!include [banner](includes/banner.md)]

Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig. Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden. Abteilungen können Gewinn- und Verlustzuständigkeit haben.

Eine Abteilung kann möglicherweise auch eine Gruppe von Kostenstellen umfassen. Positionen können Abteilungen zugeordnet sein. Um eine Abteilung zu erstellen, klicken Sie auf **Personalverwaltung** &gt; **Abteilungen** &gt; **Abteilung**. In der folgenden Tabelle werden die Felder beschrieben, die zur Verfügung stehen.

| Feld               | Beschreibung                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name                | Geben Sie einen Namens für die Abteilung ein.                                                                                                                                                                                  |
| Abteilungsnummer   | Ein Standardwert wird möglicherweise automatisch generiert, wenn ein Zahlenreferenzcode im Feld **Organisationszahl**-Referenz auf der Seite **Zahlensequenz** zugewiesen wird.                                                 |
| Suchbegriff         | Einen Namen oder ein Abkürzung eingeben, die für die Suche nach der Abteilung verwendet werden kann.                                                                                                                                            |
| Memo                | Geben Sie zusätzliche Informationen hier ein.                                                                                                                                                                            |
| In Hierarchie        | Ein aktiviertes Kontrollkästchen zeigt an, dass die Abteilung in der Abteilungshierarchie enthalten ist. Informationen darüber, wie eine Abteilung der Abteilungshierarchie hinzugefügt wird, lesen Sie die Informationen weiter unten in diesem Artikel. |
| DUNS-Nummer         | DUNS steht für Daten-universelles Zahlensystem. Dies ist eine 9-stellige Zahl, die von Dun & Bradstreet ausgegeben wird.                                                                                                     |
| Vorgesetzter             | Geben Sie die Person ein, die die Abteilung leitet.                                                                                                                                                                    |
| Adressen           | Fügen Sie Adressinformationen für die Abteilung hinzu. Fügen Sie z. B. die Postanschrift für das Gebäude hinzu, in dem sich die Abteilung befindet.                                                                          |
| Kontaktinformationen | Fügen Sie Kontaktinformationen für die Abteilung hinzu. Fügen Sie z. B. eine Telefonnummer für den Serviceschalter in der Abteilung hinzu.                                                                                           |

Um der Abteilungshierarchie eine Abteilung hinzuzufügen, führen Sie folgende Schritte aus.

1.  Klicken Sie auf **Personalverwaltung** &gt; **Abteilungen** &gt; **Abteilungshierarchie**.
2.  Klicken Sie auf **Bearbeiten** und wählen Sie dann die Organisation, unter der die Abteilung eingefügt werden soll.
3.  Klicken Sie auf **Einfügen** und wählen Sie aus der Liste **Abteilung**.
4.  In der Liste der Abteilungen, die angezeigt werden, wählen Sie die Abteilung aus, die der Hierarchie hinzugefügt werden soll.
5.  Speichern Sie die Änderungen. Sie erhalten eine Meldung, dass eine Entwurfsversion der Hierarchie erstellt wurde.
6.  Wenn Sie fertig sind, klicken auf **Veröffentlichen** im Hierarchie-Designer. Sie können ein Gültigkeitsdatum eingeben, das angibt, wann die Hierarchie veröffentlicht werden soll. Um beispielsweise eine neue Abteilung zu Beginn des folgenden Kalenderjahrs hinzuzufügen, legen Sie das Gültigkeitsdatum auf den 1. Januar des neuen Kalenderjahrs fest. Die Änderungen an der Hierarchie treten an diesem Datum in Kraft.

## <a name="steps-for-creating-a-department"></a>Schritte zum Erstellen einer Abteilung
Im Thema [Definieren neuer Abteilungen](../fin-and-ops/hr/tasks/define-new-departments.md) finden Sie die detaillierte Prozedur zum Erstellen eine neuen Abteilung. 
