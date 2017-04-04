---
title: Eine Abteilung erstellen und der Abteilungshierarchie zuordnen
description: "Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig. Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden. Abteilungen können Gewinn- und Verlustzuständigkeit haben."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee51abe108b3bc0aabc764b991222db6d185e532
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Eine Abteilung erstellen und der Abteilungshierarchie zuordnen

Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig. Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden. Abteilungen können Gewinn- und Verlustzuständigkeit haben.

Eine Abteilung kann möglicherweise auch eine Gruppe von Kostenstellen umfassen. Positionen können Abteilungen zugeordnet sein. Um eine Abteilung zu erstellen, klicken Sie auf Personalverwaltung ** ** &gt; ** Abteilungen ** &gt; ** ** Abteilung. In der folgenden Tabellen werden die Felder beschrieben, die verfügbar sind.

| Feld               | Beschreibung                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name                | Geben Sie einen Namens für die Abteilung ein.                                                                                                                                                                                  |
| Abteilungsnummer   | Ein Standardwert wird möglicherweise automatisch generiert, wenn ein Zahlenreferenzcode im Feld **Organisationszahl**referenz auf der Seite **Zahlensequenz** zugewiesen wird.                                                 |
| Suchbegriff         | Einen Namen oder ein Abkürzung eingeben, die für die Suche nach der Abteilung verwendet werden kann.                                                                                                                                            |
| Memo                | Geben Sie zusätzliche Informationen hier ein.                                                                                                                                                                            |
| In Hierarchie        | Ein aktiviertes Kontrollkästchen zeigt an, dass die Abteilung in der Abteilungshierarchie enthalten ist. Informationen darüber, wie eine Abteilung der Abteilungshierarchie hinzugefügt wird, lesen Sie die Informationen weiter unten in diesem Artikel. |
| DUNS-Nummer         | DUNS steht für Daten-universelles Zahlensystem. Dies ist eine 9-stellige Zahl, die von Dun & Bradstreet ausgegeben wird.                                                                                                     |
| Vorgesetzter             | Geben Sie die Person ein, die die Abteilung leitet.                                                                                                                                                                    |
| Adressen           | Fügen Sie Adressinformationen für die Abteilung hinzu. Fügen Sie z. B. die Postanschrift für das Gebäude hinzu, in dem sich die Abteilung befindet.                                                                          |
| Kontaktinformationen | Fügen Sie Kontaktinformationen für die Abteilung hinzu. Fügen Sie z. B. eine Telefonnummer für den Serviceschalter in der Abteilung hinzu.                                                                                           |

Um der Abteilungshierarchie eine Abteilung hinzuzufügen, führen Sie folgende Schritte aus.

1.  ** Auf Personalverwaltung ** &gt; ** Abteilungen ** &gt; ** Abteilungshierarchie **.
2.  Klicken Sie auf **Bearbeiten** und wählen Sie dann die Organisation, unter der die Abteilung eingefügt werden soll.
3.  Klicken Sie auf **Einfügen** und wählen Sie aus der Liste **Abteilung**.
4.  In der Liste der Abteilungen, die angezeigt werden, wählen Sie die Abteilung aus, die der Hierarchie hinzugefügt werden soll.
5.  Speichern Sie die Änderungen. Es wird eine Nachricht, dass eine Entwurfsversion der Hierarchie erstellt wurde.
6.  Wenn Sie fertig sind, klicken ** Veröffentlichen ** im Hierarchie-Designer. Sie können ein Gültigkeitsdatum ein, das angibt, wann die Hierarchie veröffentlicht werden soll. Um beispielsweise eine neue Abteilung zu Beginn des folgenden Kalenderjahrs hinzuzufügen, legen Sie das Gültigkeitsdatum auf den 1. Januar des neuen Kalenderjahrs fest. Die Änderungen an der Hierarchie treten an diesem Datum in Kraft.



