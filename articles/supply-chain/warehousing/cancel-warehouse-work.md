---
title: Stornieren von Lagerortarbeit für Ausnahmebehandlung
description: In diesem Thema wird die Funktion zum Stornieren von Arbeit beschrieben, mit der Vorgesetzte am Lagerort gesperrte Arbeit verarbeiten können.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016239"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Stornieren von Lagerortarbeit für Ausnahmebehandlung

[!include [banner](../includes/banner.md)]

Mit der Funktion zum Stornieren von Arbeit in Microsoft Dynamics 365 Supply Chain Management können Administratorbenutzer bestimmte Lagerortarbeit stornieren, die derzeit ausgeführt, aber vom System gesperrt wird oder aufgrund außergewöhnlicher Umstände nicht abgeschlossen werden kann. Diese Funktion ist eine attraktive und sichere Alternative zu korrektiven SQL-Skripts, die inkonsistente Daten beheben. Während diese Skripts jedoch normalerweise von IT-Profis angefordert werden, kann die Funktion zum Stornieren von Arbeit von Benutzern im Unternehmen verwendet werden, die Administratorrechte haben.

Sie können auf die Funktion zum Stornieren von Arbeit unter **Lagerortverwaltung** \> **Periodische Aufgaben** \> **Bereinigen \> Arbeit stornieren** zugreifen. Geben Sie im Dialogfeld **Arbeit stornieren** die Arbeitskennung der zu stornierenden Arbeit an, und wählen Sie dann **OK** aus.

## <a name="warehouse-work-that-can-be-canceled"></a>Lagerortarbeit, die storniert werden kann

Während des Lagerortentnahmebetriebs kann es sein, dass eine Arbeitskraft in der Situation ist, dass er Mengen erfasst hat wie von einem Lagerort zu ihrem Benutzerlagerplatz entnommen, aber den Einlagerungsvorgang nicht erfassen kann. Inkonsistente Lagerortdaten sind häufig, allerdings nicht immer, der Grund, warum Arbeit gesperrt wird.

Im Gegensatz zur regulären Stornieren-Funktion, auf die Sie zugreifen können, indem Sie die Schaltfläche **Abbrechen** auf dem Arbeitskopf verwenden, erfordert die Funktion zum Stornieren von Arbeit nicht, dass die letzte abgeschlossene Arbeitsposition eine Arbeitsposition vom Typ **Einlagern** ist. Das bedeutet, dass die Stornierungslogik für die Funktion zum Stornieren von Arbeit selbst dann ausgeführt werden kann, wenn die Artikelmenge in einer Arbeitsposition in einem Benutzerlagerplatz ist.

> [!NOTE]
> Für Arbeit, die aus betrieblichen Ursachen storniert werden muss, müssen Lagerortbenutzer weiterhin die reguläre Stornieren-Funktion auf der Arbeitsseite verwenden.

Nur Arbeit vom Typ **Vertrieb** , **Umlagerungsprobleme** , **Rohmaterialentnahme** oder **Wiederbeschaffung** kann mit Hilfe der Funktion zum Stornieren von Arbeit storniert werden. Die Stornierungslogik wird nicht für gesperrte Rohmaterialentnahmearbeit oder Arbeit ausgeführt, die mit Hilfe der Funktion zum Stornieren von Arbeit storniert werden kann (siehe den vorhergehenden Hinweis).

Um die Sperrung der Arbeit aufzuheben, storniert das System alle verbleibenden Arbeitspositionen und korrigiert die Lagerortdaten, die der Arbeitskennung zugeordnet sind, die der Benutzer angegeben hat. Alle regulären Lagerortverarbeitungsvorgänge, die die betroffene Artikelmenge umfassen, können dann fortgesetzt werden.

Um den betroffenen Artikel in einen bestimmten Lagerplatz einzulagern, nachdem die Arbeit storniert wurde, muss der Benutzer einen Bestandsumlagerungs- oder Mengenanpassungseinstellvorgang auf einem mobilen Gerät verwenden.
