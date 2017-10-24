---
title: Organisatorische Trainings-Power BI-Inhalt
description: "In diesem Thema wird der Power BI-Inhalt Finance and Operations – Organisatorisches Training beschrieben. Es wird erläutert, wie Sie auf das Content-Pack zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e49d9af8b8bd8d5edb977c49742861199c6964fd
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="organizational-training-power-bi-content"></a>Organisatorische Trainings-Power BI-Inhalt

[!include[banner](../includes/banner.md)]


In diesem Thema wird der Power BI-Inhalt Finance and Operations – Organisatorisches Training beschrieben. Es wird erläutert, wie Sie auf das Content-Pack zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen auf das Inhaltspaket
--------------------------

Sie finden das Organisatorische Trainings-Content-Pack in der Bibliothek für freigegebene Anlagen in Microsoft Dynamics Lifecycle Services (LCS). Weitere Informationen dazu, wie Sie Inhalte herunterladen und mit Ihrem Microsoft Dynamics 365 for Finance and Operations verbinden, finden Sie unter [Power Bi-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Berichte, die im Paket enthalten sind
Nachdem Sie das Inhaltspaket mit Ihren Finance and Operations-Daten verbunden haben, zeigen die Berichte die Daten Ihrer Organisation an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Die Berichte, die im Paket enthalten sind, haben Diagrammen und Tabellen, die zusätzliche Informationen enthalten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht          | Inhalt                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurs-Analyse | Erfassung nach Lagerplatz, Kursteilnehmer nach Status und Erfassungsliste |
| Kurstypen    | Kurstypen nach Qualifikation                                                       |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Finance and Operations-Daten werden für die Berichte des Inhaltspakets für das organisatorische Training verwendet. Die folgende Tabelle zeigt die Entitäten, auf denen das Paket basiert.

| Entität                    | Inhalt                                                         | Beziehungen mit anderen Entitäten                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalendergegenkonten zu den Segmentberichten                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Unternehmen, nach denen Berichte gefiltert werden können                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Kurs, Beschreibung, Kursleitername, Standort und Status | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Kursprogrammen, Kurs und Start- und Endzeiten                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Name, Status, Einzelvorgang und Erstzulassung                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Qualifikation, Fähigkeitstyp und Level                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Tage, Wochen, Monate und Jahre                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Geburtsdatum, Geschlecht, Familienstand und Nationalität         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Startdatum, Enddatum und Umbuchungsdatum                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Funktion, Typ und Titel                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Position, Titel und FTE                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Vorname, Nachname, vollständiger Name                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Titel- und Dienstalter                                         | Training\_CourseAttendees                                                                                                                                                                          |

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhaltspaket verwendet werden. Wenn Sie zusätzliche Berechnungen in Ihren Berichten und Dashboard einbeziehen möchten, können Sie die Training.pbix Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um das Inhaltspaket zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





