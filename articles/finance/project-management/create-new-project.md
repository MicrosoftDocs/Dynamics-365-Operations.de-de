---
title: Neues Projekt erstellen
description: Dieser Artikel bietet Informationen dazu, wie ein neues Projekt erstellt wird.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760553"
---
# <a name="create-a-new-project"></a>Neues Projekt erstellen

[!include [banner](../includes/banner.md)]

Führen Sie die folgenden Schritte aus, um ein neues Projekt zu erstellen.

1. Wählen Sie auf der Seite **Projektmanagement** **Neues Projekt** aus und geben Sie die folgenden Werte ein:

    - **Projekttype:** Nach Aufwand
    - **Projektname:** XYZ Upgrade-Phase 2
    - **Projektgruppe:** TM\_WIP
    - **Projektvertragskennung:** 00000002

2. Wählen Sie **Projekt erstellen** aus.

## <a name="assign-a-resource-to-a-project"></a>Ressource zum Projekt zuweisen

1. Wählen Sie auf der Seite **Arbeitskräfte** in der Liste **Arbeitskräfte** den Datensatz für die Arbeitskraft aus, für die Sie zuvor Kompetenzen eingerichtet haben aus, und öffnen Sie den Arbeitskraftdatensatz.
2. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Projekt** in der Gruppe **Einrichten** **Projekte zuweisen** aus.
3. Filtern Sie auf der Seite **Projektzuweisungen für Ressourcenüberprüfung** auf der Registerkarte **Projekte** im Feld **Fügen Sie das Projekt zu den ausgewählten Projekten hinzu** nach dem **XYZ Upgrade-Phase 2**-Projekt.
4. Wählen Sie im Bereich **Verbleibende Projekte** ein Projekt aus, und klicken Sie anschließend auf den Pfeil, um es dem Bereich **Ausgewählte Projekte** hinzuzufügen.

Bei Bedarf können Sie auch Kategorien für eine Ressource zuweisen. Der Kategorietyp ist **Kosten** oder **Umsatzerlös**. Der Kategorietyp wird von Ihrer Organisation festgelegt. Wenn einer Ressource keine Kategorien zugewiesen sind, sucht Finance nach der Standardkategorie für Stundenpreise für die Kosten und den Umsatzerlös.

## <a name="set-up-project-resource-and-role-characteristics"></a>Einrichten von Projektressourcen und Rollenmerkmalen

Ein Projektmanager kann die Projektressourcenfunktionen verwenden, um die Rollen erstellen, die für das Projekt erforderlich sind. Rollen können verwendet werden, wenn bestätigte Ressourcen während der Ressourcenreservierungen noch unbekannt sind. Rollen können verwendet werden, um Ressourcen vorübergehend als geplante Ressourcen zu reservieren, um die Projektplanungsphasen fortsetzen zu können.

[![Beispiel einer Rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Szenario:** Contoso wurde für ein Aufwandsprojekt gebucht, das eine genehmigte Projektcharter hat. Der Juniorprojektmanager arbeitet noch am Umfang des Projekts. Der Ressourcen-Manager identifiziert derzeit zugewiesene Ressourcen, die reserviert für die Arbeit an dem neuen Projekt zugewiesen werden. Aufgrund der kritischen Natur des Projekts forderte der Projektträger einen Senior-Projektmanager als eine der Rollen. Der Ressourcen-Manager muss die neue Ressource erwerben und die Rolle im System definieren, falls der Juniorprojektmanager die Ressourceninformationen während der Projektplanung benötigt.

Die folgenden Schritte zeigen, wie der Ressourcen-Manager den Senior-Projektmanager einrichten und Ressourcenmerkmale zuordnen kann. Später kann die Rolle verwendet werden, um für verfügbare Ressourcen zu finden, die die erforderlichen Ressourcenkompetenzen aufweisen.

1. Wählen Sie auf der Seite **Einstellungsrollen** **Neu** aus, und geben Sie die folgenden Werte ein:

    - **Rollenkennung:** Senior Project Manager
    - **Beschreibung:** Senior Project Manager

2. Wählen Sie **Erstellen** aus.
3. Wählen Sie die Rolle für den **Senior-Projektmanager** aus und anschließend **Merkmale konfigurieren**.
4. Wählen Sie im Feld **Merkmalstyp** die Option **Qualifikation**.
5. Geben Sie im Feld **Verfügbare Merkmale** die Qualifikation ein, nach der gesucht wird.
6. Wählen Sie im Feld **Merkmalstyp** die Option **Bescheinigung** aus.
7. Geben Sie im **Verfügbare Merkmale**-Feld die Bescheinigung ein, die Sie suchen.

## <a name="assign-a-project-resource-to-a-project"></a>Projektressource zum Projekt zuweisen

1. Wählen Sie auf der Seite **Alle Projekte** das Projekt **XYZ Upgrade-Phase 2** aus.
2. Klicken Sie auf der Registerkarte **Projektteam und Planung** auf **Hinzufügen**.
3. Wählen Sie im Feld **Rolle** **Teammitglied** aus.
4. Wählen Sie **Aus Kalender buchen** aus.
5. Klicken Sie auf der Seite **Ressourcenverfügbarkeit** auf **Einstellungen anzeigen**.
6. Geben Sie auf der **Ansichtseinstellungen anpassen**-Seite die folgenden Werte ein:

    - **Format für Datumsbereichsansicht:** Tag
    - **Verfügbarkeitsbeschreibungen anzeigen**: Ja
    - **Verbleibende Kapazität anzeigen**: Ja

7. Wählen Sie in der Liste der Ressourcen eine Ressource aus.
8. Wählen Sie **Verbindlich buchen** und **Vollständige Kapazität** aus.

## <a name="assign-a-resource-to-a-default-role"></a>Zuweisen einer Ressource zu einer Standardrolle

Um Projekt- und Ressourcen-Manager zu unterstützen, können Sie die zu einem Projekt reservierbaren Ressourcen detaillierter darstellen. Sie können eine standardmäßige Rolle zu einer vorhandenen Ressource oder zu einer neu abgerufenen Ressource zuordnen. Wenn Sie beispielsweise als Daniel eingestellt wurde, weist er Erfahrung und Fähigkeiten, um die der Business Analysten-Rolle ein. Ressourcen-Manager Der zugewiesene Rolle diese als Daniels Standardrolle zu. Daher ist Leiterin des Ressourcenmanagements Daniel einem Pool der Business Analysten hinzu, hinzufügen, die verfügbar sind, für Projekte zu arbeiten.

Während der Ressourcenreservierung können Projektmanager die Rollenressourcen filtern, die verfügbar sind, um an Projekten zu arbeiten. Sie können diese Informationen als als Kriterium verwenden, wenn sie Multikriterienentscheidungsanalysen für die Ressourcenerfüllung ausführen. Sie können andere Ressourcenmerkmale dem Filter für die Suche nach Ressourcen hinzufügen, die eine bestimmte Ausbildung, Qualifikationen und Erfahrungen für ein bestimmtes Projekt besitzen.

**Szenario:** Ein genehmigtes Projekt wurde gestartet, und die Senior-Projektmanager wurde während der Projektplanungsphase als geplante Ressource reserviert. Der Ressourcen-Manager hat nun eine Ressource abgerufen, um die Rolle Senio-Projektmanager zu erfüllen.

1. Wählen Sie auf der Seite **Ressourcenliste** **Daniel Goldschmidt** aus.
2. Wählen Sie auf der Seite **Ressourcenrolle** **Neu** aus, und geben Sie die folgenden Werte ein:

    - **Gültigkeit:** Geben Sie das aktuelle Datum ein.
    - **Ablauf:** Geben Sie **Nie** ein.
    - **Rolle:** Geben Sie **Senior-Projektmanager** ein.

3. Klicken Sie auf **Speichern** und schließen Sie die Seite.
4. Fügen Sie auf der **Kompetenzen**-Registerkarte die **ProjectMgmt**-Qualifikation und die **PMP**-Bescheinigung hinzu.
