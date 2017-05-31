---
title: "Steuerkalender, Geschäftsjahre und Finanzzeiträume"
description: "Dieser Artikel behandelt Steuerkalender, Geschäftsjahre und Perioden und erläutert, wie diese für juristische Personen, Anlagen und die Budgetierung verwendet werden."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 22a08b1b9e819f5c683d278f37bf3404e757d200
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Steuerkalender, Geschäftsjahre und Finanzzeiträume

[!include[banner](../includes/banner.md)]


Dieser Artikel behandelt Steuerkalender, Geschäftsjahre und Perioden und erläutert, wie diese für juristische Personen, Anlagen und die Budgetierung verwendet werden.

Steuerkalender bieten einen Rahmen für die finanziellen Aktivitäten einer Organisation. Jeder Steuerkalender beinhaltet mindestens ein Geschäftsjahr, und jedes Geschäftsjahr besteht aus mehreren Perioden. Steuerkalender können auf Geschäftsjahren mit Beginn am 1. Januar und Ende am 31. Dezember oder auf beliebigen anderen Datumsangaben für Geschäftsjahre basieren. In einigen Organisationen beginnt das Geschäftsjahr zum Beispiel am 1. Juli eines Jahres und endet am 30. Juni des darauf folgenden Jahres. 

Es gilt keine Beschränkung in Bezug auf die Anzahl der erstellbaren Steuerkalender und auch keine Beschränkung bezüglich der Anzahl der Geschäftsjahre, die für einen Steuerkalender erstellt werden können. Jeder Steuerkalender ist unabhängig von der Organisation und kann von mehreren juristischen Personen in der Organisation verwendet werden. Zum Beispiel verfügt eine Organisation über acht Abteilungen, wobei jede Abteilung eine eigene juristische Person darstellt. Fünf Abteilungen verwenden den gleichen Steuerkalender, drei Abteilungen greifen hingegen auf andere Kalender zurück. Sie können für die fünf juristischen Personen, die den gleichen Steuerkalender verwenden, einen Steuerkalender und anschließend separate Steuerkalender für die anderen juristischen Personen erstellen.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Erstellen von Steuerkalendern, Geschäftsjahren und Perioden
Auf der Seite Steuerkalender können Sie Steuerkalender, Geschäftsjahre und Finanzzeiträume erstellen und löschen. Außerdem können vorhandene Perioden unterteilt und Abschlussperioden für den Abschluss eines Geschäftsjahres erstellt werden. 

Eine Abschlussperiode wird verwendet, um getrennte Hauptbuchbuchungen nutzen zu können, die beim Abschließen eines Geschäftsjahrs generiert werden. Wenn sich die Abschlussbuchungen in einer Steuerperiode befinden, können Finanzaufstellungen einfacher erstellt werden, die unterschiedliche Arten von Abschlusseinträgen entweder enthalten oder nicht enthalten. Wenn ein Geschäftsjahr in 12 Steuerperioden unterteilt ist, ist die Abschlussperiode normalerweise die 13. Periode. Eine Abschlussperiode kann jedoch aus allen Perioden erstellt werden, die über den Status Offen verfügen. 

Wählen Sie beim Erstellen einer Abschlussperiode eine Periode aus, die den Status Offen sowie die gewünschten Daten aufweist. Die neue Abschlussperiode kopiert das Start- und Enddatum aus der vorhandenen Periode. Die ursprüngliche Periode bleibt dabei erhalten. Angenommen, Sie wählen Periode 12 aus, wobei es sich um die letzte Periode des Geschäftsjahrs mit den Daten 1. August bis 31. August handelt. Sie geben einen Namen für die Abschlussperiode ein, z. B. Abschluss. Nach der Erstellung der neuen Abschlussperiode verfügen Sie über die ursprüngliche Periode und die Abschlussperiode. Beide weisen das Startdatum 1. August und das Enddatum 31. August auf.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Auswählen von Steuerkalendern für Sachkonten, Anlagen und Budgetzyklen
Steuerkalender werden mit Anlagenabschreibung, Finanzbuchungen und Budgetzyklen verwendet. Wenn Sie einen Steuerkalender erstellen, können Sie ihn für mehrere Zwecke verwenden. Sie können einen Steuerkalender für ein Wertmodell oder ein Abschreibungsbuch auswählen, um ihn als Anlagenkalender festzulegen. Sie können einen Steuerkalender für ein Sachkonto auswählen, um ihn als Sachkontokalender zu verwenden. Außerdem kann ein Steuerkalender für einen Budgetzyklus ausgewählt werden, um ihn als Budgetkalender zu verwenden. Für alle diese Kategorien kann der gleiche Steuerkalender verwendet werden.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Auswählen eines Steuerkalenders für die juristische Person

Wählen Sie den Steuerkalender aus, den Sie für das Sachkonto für die juristische Person im Formular Sachkonto verwenden möchten. Auf der Seite Sachkonto muss für jede juristische Person ein Steuerkalender ausgewählt werden. Nach der Auswahl eines Steuerkalenders können Sie auf der Seite Sachkontokalender Periodenstatus und ‑berechtigungen für alle Perioden eines Geschäftsjahrs einrichten.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Auswählen eines Steuerkalenders für Anlagen

Sie können einen Steuerkalender für ein Wertmodell oder ein Abschreibungsbuch auswählen. Der betreffende Steuerkalender wird für die Anlagen verwendet, für die auch das ausgewählte Wertmodell oder Abschreibungsbuch verwendet wird. Sie können jeden auf der Seite "Steuerkalender" definierten Steuerkalender auswählen.

### <a name="define-budget-cycle-time-spans"></a>Definieren von Zeitspannen für Budgetzyklen

Budgetzyklen sind der Zeitraum, in dem ein Budget verwendet wird. Budgetzyklen können einen Teil einen Geschäftsjahrs oder mehrere Geschäftsjahre umfassen, zum Beispiel einen zwei oder drei Jahre umfassenden Budgetzyklus. Durch die Zeitspanne für den Budgetzyklus wird die Anzahl der Perioden definiert, die im Budgetzyklus enthalten sind. Geben Sie die Zeitspanne für den Budgetzyklus auf der Seite "Zeitspannen für Budgetzyklus" ein.

## <a name="maintain-periods-for-your-organization"></a>Verwalten von Perioden für die Organisation
Auf der Seite Sachkontokalender können Sie die Details zum Steuerkalender, zu den Geschäftsjahren und zu den Perioden angezeigt werden, die in Ihrer Organisation verwendet werden. Sie können auch den Status der Perioden ändern und auswählen, welche Benutzer Buchungen für bestimmte Perioden vornehmen können. Zu Beginn einer neuen Periode soll zum Beispiel eine Gruppe von Benutzern die Buchung von Posten aus der vorherigen Periode abschließen, während andere Gruppen nur in der neuen Periode arbeiten.






