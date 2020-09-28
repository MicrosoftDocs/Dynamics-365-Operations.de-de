---
title: Projektteam erstellen
description: Dieser Artikel bietet Informationen dazu, wie Projektteams erstellt und verwaltet werden.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760554"
---
# <a name="create-a-project-team"></a>Projektteam erstellen

[!include [banner](../includes/banner.md)]

Um die Rollen zu verwenden, muss ein Projektmanager die Rollen dem Projekt zuordnen. Es können mehrere Rollen können für ein Projekt zugeordnet werden. Um Unklarheiten zu vermeiden, werden diese Rollen während der Reservierung automatisch beschriftet. Wenn beispielsweise der Projektmanager drei Softwareingenieure benötigt, werden automatisch drei Softwareingenieur-Rollen mit der Beschriftung **Software Engineer 1**, **Software Engineer 2** und **Software Engineer 3** generiert. Wenn zuvor Rollenmerkmal für die Rolle festgelegt wurden, werden sie als Filter für die Suche nach einer Ressource angewendet. Zusätzliche Merkmale können nach Bedarf hinzugefügt werden, um die Suche noch weiter zu verfeinern.

Die Ansichtseinstellungen können ebenfalls angepasst werden, um eine bessere Ansicht der Ressourcenverfügbarkeit zu ermöglichen. Es gibt Optionen für eine stündliche, tägliche, wöchentliche, monatliche, quartalsweise und jährliche Verfügbarkeit. Es gibt auch eine Option, um verfügbarer und Restkapazitäten für Ressourcen anzuzeigen. Diese Option ist für die Zeitverwaltung hilfreich, wenn Sie die verfügbare Zeit für Aktivitäten oder die Ressourcenverfügbarkeit schätzen.

Der Projektmanager kann eine Rolle auf der Seite auswählen. Wenn es eine verfügbares Ressourcen gibt, die zu den Anforderung passt, kann er die Ressource einer Rolle reservieren. Beachten Sie, dass die Ressourcen zu diesem Zeitpunkt der Planungsphase noch nicht in reserviert werden müssen. Wenn Sie einen PSP erstellen, können Sie Rollen durch geplanten Ressourcen für das Projekt ersetzen. Wenn die Rollen durch mit Personal versehene Ressourcen im PSP ersetzt werden, aktualisiert die Ressourceneinrichtung automatisch die Projektteamliste und den Zeitplan.

[![Projektteamliste mit Rollen und aktuellen Ressourcen](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Der Projektmanager hat verschiedene Optionen für die Buchung einer Ressource für ein Projekt wie **Restkapazität** **Restkapazität** **Volle Kapazität** und **spezifische Stunden**. Diese Buchungsoptionen können jederzeit storniert werden, wenn sich Ressourcenzuweisung ändern. Es werden gibt zwei Typen von Buchungen unterstützt:

- **Verbindlich buchen** - Die Ressourcenreservierung wurde genehmigt und bestätigt, um an dem Auftrag in dem festgelegten Zeitraum zu arbeiten.
- **Nicht verbindlich buchen** - Die Ressourcenreservierung wurde eingeplant, um an dem Auftrag in dem festgelegten Zeitraum zu arbeiten.

Das folgende Verfahren zeigt, wie ein Projektteam erstellt wird.

## <a name="create-a-project-team"></a>Projektteam erstellen

1. Wählen Sie auf der Listenseite **Alle Projekte** ein Projekt und anschließend **Bearbeiten** aus.
2. Geben Sie auf der Registerkarte **Projektteam und Planung** im Feld **Enddatum planen** das Zeitplanstartdatum plus einen Monat ein. Wenn das Zeitplanstartdatum beispielsweise am 24. Juni 2017 ist, geben Sie **24.07.2017** ein.
3. Wählen Sie **Hinzufügen** aus.
4. Wählen Sie im Bereich **Rollen zum Projekt hinzufügen** im **Rolle**-Feld **Senior-Projektmanager** aus.
5. Wählen Sie **Erforderliche Kompetenzen** aus.
6. Auf der Seite **Merkmale auswählen** wählen Sie die Merkmale, dass Sie zuvor für die Senior-Projektmanager festgelegt haben. Wählen Sie **OK**.
7. Auf der Seite **Rollen zum Projekt hinzufügen** geben Sie im Feld **Anzahl der Ressourcen** den Wert **1** ein.
8. Im Feld **Ressource** zeigt die Suche alle Ressourcen an, die die erforderlichen Kompetenzen haben. Wählen Sie **Daniel Goldschmidt** und dann **Erstellen** aus.
9. Wählen Sie auf der Seite **Projekt** **Hinzufügen** aus.
10. Wählen Sie im Bereich **Rollen zum Projekt hinzufügen** im **Rolle**-Feld **Teammitglied** aus. Geben Sie **5** in das Feld **Anzahl der Ressourcen** ein.
11. Wählen Sie **Erstellen** aus.
12. Wählen Sie **Ressource auffüllen** auf der **Projekte**-Seite aus.

## <a name="monitor-project-teams"></a>Überwachung von Projektteams
1. Wählen Sie auf der Seite **Alle Projekte** den **Projekt-ID**-Link für das **XYZ-Upgrade-Phase 2**-Projekt aus.
2. Überprüfen Sie auf dem **Projektteam und Planung**-Inforegister, dass die Projektressourcen korrekt aufgelistet werden.
