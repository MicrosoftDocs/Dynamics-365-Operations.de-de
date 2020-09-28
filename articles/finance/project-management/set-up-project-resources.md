---
title: Einrichten von Projektressourcen
description: Dieser Thema enthält Informationen über die Einrichtung oder Anforderung von Projektressourcen.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760558"
---
# <a name="set-up-project-resources"></a>Einrichten von Projektressourcen

[!include [banner](../includes/banner.md)]

Sie müssen einen Kalender einrichten und diesen einem Mitarbeiter oder einer Arbeitskraft zuordnen. Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen planen, die dem Projekt reserviert werden. Während der Kalendereinstellung können Projektmanager einen Ressourcenausgleich als Teil der Ressourcenoptimierung ausführen. Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen festgelegt werden. Sie können einen Kalender auf der **Seite** Kalender einrichten.

Wenn Sie eine Arbeitskraft als Projektressource einrichten, können Sie aus Arbeitskräften auswählen, die in dem Unternehmen arbeiten, für das Sie Ressourcen einrichten. Alternativ können Sie Arbeitskräfte von anderen Unternehmen in Ihrer Organisation auswählen. Diese Arbeitskräfte werden als Intercompany-Ressourcen bezeichnet.

Nachfolgend wird erläutert, wie eine Arbeitskraft als Projektressource in Ihrem Unternehmen eingerichtet wird und wie eine Intercompany-Ressource eingerichtet wird.

## <a name="set-up-a-worker-as-a-project-resource"></a>Arbeitskräfte als Projektressourcen einrichten

1. Wählen Sie auf der Seite **Arbeitskräfte** in der Liste **Arbeitskräfte** die Arbeitskraft, die Sie als Projektressource hinzufügen und öffnen Sie den Arbeitskraftdatensatz.
2. Klicken Sie im Aktivitätsbereich auf **Projekt** &gt; **Einstellungen** &gt; **Projekteinstellungen**.
3. Wählen Sie einen Kalender aus, und schließen Sie die Seite.

Sie können außerdem standardmäßige Projekte für eine Ressource als Typ einer Vorabzuweisung angeben. Vorabzuweisungen können verwendet werden, wenn der Ressourcen-Manager oder der Projektmanager weiß, welche Projekte für die Ressource gelten oder im Voraus. Vorabzuweisungen können außerdem auf der Anforderung eines Projektträgers oder des Debitors basieren. Damit ein Projekt auf der Seite **Projekte zuweisen** vorab zugewiesen werden kann, wählen Sie auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** das gewünschte Projekt aus.

## <a name="set-up-an-intercompany-resource"></a>Einrichten einer Intercompany-Ressource

Wenn Sie eine Arbeitskraft als Intercompany-Ressource einrichten, müssen Sie die Einstellungen im Ausleiheunternehmen und im leihenden Unternehmen ausführen.

### <a name="in-the-lending-company"></a>Im Ausleiheunternehmen

1. Überprüfen Sie in Finance, dass das Ausleiheunternehmen aktiviert ist, und schließen Sie dann das Verfahren wie im vorherigen Abschnitt „Arbeitkraft als Projektressource einrichten“ beschrieben ab.
2. Wählen Sie auf der Seite **Verrechnung** **Neu** aus.
3. Wählen Sie im Feld **Kennung der juristischen Person** das Ausleiheunternehmen aus. Füllen Sie die restlichen Felder entsprechend aus, und wählen Sie dann **Speichern** aus.
4. Wählen Sie auf der Seite **Interner Verrechnungspreis** **Neu** aus.
5. Wählen Sie im Feld **Ausleihende juristische Person** das entsprechende Unternehmen aus.
6. Wenn Sie dem borgenden Unternehmen nur die Ressource ausleihen möchten, die Sie am Anfang dieses Abschnitts im Feld **Ressource** erstellt haben, wählen Sie den Namen der Ressource aus, die Sie erstellt haben. Wenn alle Ressourcen im Ausleiheunternehmen für das borgende Unternehmen verfügbar gemacht werden sollen, lassen Sie das Feld **Ressource** leer.
7. Setzen Sie auf der Seite **Projektverwaltungs- und -verrechnungsparameter** auf der Registerkarte **Intercompany** die Option **Intercompany-Ressourcenplanung und -Arbeitszeitnachweise** auf **Ja**.

### <a name="in-the-borrowing-company"></a>Im leihenden Unternehmen

- Geben Sie auf der Seite **Ressourcenliste** im Suchfilter den Namen der Ressource ein, die Sie für das Ausleiheunternehmen erstellt haben, um zu prüfen, ob der Name in der Ressourcenliste für das borgende Unternehmen enthalten ist.

## <a name="request-project-resources"></a>Projektressourcen anfordern
Die Projekteinsatzplanungsfunktionen unterstützen Ressourcen-Manager nur bei der Verteilung von Ressourcen mit Personal auf Aufträge oder Projekte. Um diese Funktion zu aktivieren, führen Sie die folgenden Aufgaben aus, oder stellen Sie sicher, dass diese abgeschlossen wurden:

- Hier können Sie Nummernkreise einrichten.
- Einrichten von Projektverwaltungs- und Buchhaltungsworkflows
- Aktivieren der Ressourcenanforderungsworkflows.

Nachdem Sie die vorherigen Aufgaben abgeschlossen haben, können Sie die folgenden Aufgaben bei Bedarf abschließen:

- Erstellen Sie eine Ressourcenanforderung von nicht fest gebuchten Personal Ressourcen.
- Ressourcenanforderungen überwachen
- Ressourcenanforderungen erfüllen
- Anfordern von Ressourcen mit Personal aus PSP.
- Buchen von Ressourcen für ein Projekt ohne Anforderung einer Ressource mit Personal.
