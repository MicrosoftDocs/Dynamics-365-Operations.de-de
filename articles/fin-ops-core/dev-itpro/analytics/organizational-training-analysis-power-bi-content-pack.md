---
title: Organisatorische Trainings Power BI-Inhalt
description: Dieser Artikel beschreibt den Inhalt von Finanzen und Betrieb – Organisationsschulung Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.openlocfilehash: 2e80810dbeb536dccf6e13b5fca6a85f4858d8da
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267241"
---
# <a name="organizational-training-power-bi-content"></a>Organisatorische Trainings Power BI-Inhalt

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt den Inhalt von Finanzen und Betrieb – Organisationsschulung Power BI.

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten sind
Nachdem Sie das Inhaltspaket mit Ihren Daten verbunden haben, zeigen die Berichte die Daten Ihrer Organisation an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Die Berichte, die im Paket enthalten sind, haben Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht          | Inhalt                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurs-Analyse | Erfassung nach Lagerplatz, Kursteilnehmer nach Status und Erfassungsliste |
| Kurstypen    | Kurstypen nach Qualifikation                                                       |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Anwendungsdaten werden für die Berichte des Inhaltspakets für das organisatorische Training verwendet. Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                    | Inhalt                                                         | Beziehungen mit anderen Entitäten |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Kalendergegenkonten zu den Segmentberichten                                | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_Company         | Unternehmen, nach denen Berichte gefiltert werden können                                   | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_Course          | Kurs, Beschreibung, Kursleitername, Standort und Status | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill |
| Training\_CourseAgenda    | Kursprogrammen, Kurs und Start- und Endzeiten                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course |
| Training\_CourseAttendees | Name, Status, Einzelvorgang und Erstzulassung                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Qualifikation, Fähigkeitstyp und Level                                     | Training\_Course |
| Training\_Date            | Tage, Wochen, Monate und Jahre                                   | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_Demographics    | Geburtsdatum, Geschlecht, Familienstand und Nationalität         | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_Employment      | Startdatum, Enddatum und Umbuchungsdatum                        | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_Job             | Funktion, Typ und Titel                                        | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_Position        | Position, Titel und FTE                  | Training\_CourseAgenda Training\_CourseAttendees |
| Training\_WorkerName      | Vorname, Nachname, vollständiger Name                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Titel- und Dienstalter                                         | Training\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
