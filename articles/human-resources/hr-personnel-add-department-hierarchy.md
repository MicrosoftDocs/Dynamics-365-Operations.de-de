---
title: Abteilungen erstellen und sie in die Abteilungshierarchie einbeziehen
description: Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cdc0440c02d0e66eaa89bfd875d8c8edf8d99c96
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688600"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Abteilungen erstellen und sie in die Abteilungshierarchie einbeziehen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt. Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig. Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden. Abteilungen können Gewinn- und Verlustzuständigkeit haben.

Eine Abteilung kann möglicherweise auch eine Gruppe von Kostenstellen umfassen. Positionen können Abteilungen zugeordnet sein. Um eine Abteilung zu erstellen, klicken Sie auf **Personalverwaltung** &gt; **Abteilungen** &gt; **Abteilung**. In der folgenden Tabelle werden die Felder beschrieben, die zur Verfügung stehen.

| Feld               | Beschreibung                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Name**                | Geben Sie einen Namens für die Abteilung ein.                                                                                                                                                                                  |
| **Abteilungsnummer**   | Ein Standardwert wird möglicherweise automatisch generiert, wenn ein Zahlenreferenzcode im Feld **Organisationszahl**-Referenz auf der Seite **Zahlensequenz** zugewiesen wird.                                                 |
| **Suchbegriff**         | Einen Namen oder ein Abkürzung eingeben, die für die Suche nach der Abteilung verwendet werden kann.                                                                                                                                            |
| **Memo**                | Geben Sie zusätzliche Informationen hier ein.                                                                                                                                                                            |
| **In Hierarchie**        | Ein aktiviertes Kontrollkästchen zeigt an, dass die Abteilung in der Abteilungshierarchie enthalten ist. Informationen darüber, wie eine Abteilung der Abteilungshierarchie hinzugefügt wird, lesen Sie die Informationen weiter unten in diesem Artikel. |
| **DUNS-Nummer**         | DUNS steht für Daten-universelles Zahlensystem. Dies ist eine 9-stellige Zahl, die von Dun & Bradstreet ausgegeben wird.                                                                                                     |
| **Vorgesetzter**             | Geben Sie die Person ein, die die Abteilung leitet.                                                                                                                                                                    |
| **Adressen**           | Fügen Sie Adressinformationen für die Abteilung hinzu. Fügen Sie z. B. die Postanschrift für das Gebäude hinzu, in dem sich die Abteilung befindet.                                                                          |
| **Kontaktinformationen** | Fügen Sie Kontaktinformationen für die Abteilung hinzu. Fügen Sie z. B. eine Telefonnummer für den Serviceschalter in der Abteilung hinzu.                                                                                           |

Um der Abteilungshierarchie eine Abteilung hinzuzufügen, führen Sie folgende Schritte aus.

1.  Klicken Sie auf **Personalverwaltung** &gt; **Abteilungen** &gt; **Abteilungshierarchie**.
2.  Klicken Sie auf **Bearbeiten** und wählen Sie dann die Organisation, unter der die Abteilung eingefügt werden soll.
3.  Klicken Sie auf **Einfügen** und wählen Sie aus der Liste **Abteilung**.
4.  In der Liste der Abteilungen, die angezeigt werden, wählen Sie die Abteilung aus, die der Hierarchie hinzugefügt werden soll.
5.  Speichern Sie die Änderungen. Sie erhalten eine Meldung, dass eine Entwurfsversion der Hierarchie erstellt wurde.
6.  Wenn Sie fertig sind, klicken auf **Veröffentlichen** im Hierarchie-Designer. Sie können ein Gültigkeitsdatum eingeben, das angibt, wann die Hierarchie veröffentlicht werden soll. Um beispielsweise eine neue Abteilung zu Beginn des folgenden Kalenderjahrs hinzuzufügen, legen Sie das Gültigkeitsdatum auf den 1. Januar des neuen Kalenderjahrs fest. Die Änderungen an der Hierarchie treten an diesem Datum in Kraft.

## <a name="steps-for-creating-a-department"></a>Schritte zum Erstellen einer Abteilung
Im Artikel [Definieren neuer Abteilungen](./hr-personnel-define-departments.md) finden Sie die detaillierte Prozedur zum Erstellen eine neuen Abteilung. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
