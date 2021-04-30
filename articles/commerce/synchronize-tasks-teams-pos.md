---
title: Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren
description: In diesem Thema wird beschrieben, wie Sie die Aufgabenverwaltung zwischen Microsoft Teams und der Verkaufsstelle (POS) in Dynamics 365 Commerce synchronisieren.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b4a9ad561e3bff67720a08d6e4184a81e01f734
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908268"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Aufgabenverwaltung zwischen Microsoft Teams und der Verkaufsstelle (POS) in Dynamics 365 Commerce synchronisieren.

Einer der Hauptzwecke der Teams-Integration besteht darin, die Synchronisierung der Aufgabenverwaltung zwischen der POS-Anwendung und Teams zu ermöglichen. Auf diese Weise können Filialmitarbeiter entweder die POS-Anwendung oder Teams zum Verwalten von Aufgaben verwenden und müssen nicht zwischen Anwendungen wechseln.

Da Planner als Repository für Aufgaben in Teams verwendet wird, muss eine Verknüpfung zwischen Teams und Dynamics 365 Commerce bestehen. Diese Verknüpfung wird mithilfe einer bestimmten Plan-ID für ein bestimmtes Filialteam hergestellt.

Die folgenden Prozeduren zeigen, wie Sie die Synchronisierung der Aufgabenverwaltung zwischen der POS- und der Teams-Anwendung einrichten.

## <a name="publish-a-test-task-list-in-teams"></a>Eine Testaufgabenliste in Teams veröffentlichen

Die folgende Prozedur setzt voraus, dass Ihre Filialteams die Aufgabenverwaltungsintegration von Microsoft Teams mit Commerce zum ersten Mal verwenden.

Führen Sie die folgenden Schritte aus, um eine Testaufgabenliste in Teams zu veröffentlichen.

1. Melden Sie sich in Teams als Kommunikationsmanager an. In der Regel sind Kommunikationsmanager Benutzer, die über in Commerce über die Rolle **Regionalmanager** verfügen.
1. Wählen Sie im linken Navigationsbereich **Aufgaben aus Planner** aus.
1. Wählen Sie auf der Registerkarte **Veröffentlichte Listen** unten links **Neue Liste** aus und benennen Sie die neue Liste **Testaufgabenliste**.
1. Wählen Sie **Erstellen** aus. Die neue Liste wird unter **Entwürfe** angezeigt.
1. Geben Sie unter **Aufgabentitel** der ersten Aufgabe den Titel **Teams-Integration testen**. Wählen Sie dann **Eingeben** aus.
1. Wählen Sie in der Liste **Entwürfe** die Aufgabenliste aus. Dann wählen Sie dann  **Veröffentlichen**  in der oberen rechten Ecke.
1. Im Dialogfeld **Auswählen, an wen veröffentlicht werden soll** wählen Sie die Teams aus, die die Liste der Testaufgaben erhalten sollen.
1. Wählen Sie **Weiter**, um Ihren Veröffentlichungsplan zu überprüfen. Wenn Sie Änderungen vornehmen müssen, wählen Sie  **Zurück**. 
1. Wählen Sie **Bestätigen und fortfahren** und dann **Veröffentlichen**.
1. Nach Abschluss der Veröffentlichung wird oben auf der Registerkarte **Veröffentlichte Listen** eine Meldung angezeigt, ob Ihre Aufgabenliste erfolgreich zugestellt wurde.

Weitere Informationen finden Sie unter [Veröffentlichen von Aufgabenlisten zum Erstellen und Nachverfolgen der Arbeit in Ihrer Organisation](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

## <a name="link-pos-and-teams-for-task-management"></a>POS und Teams für die Aufgabenverwaltung verknüpfen

Um die POS- und Microsoft Teams-Anwendungen für die Aufgabenverwaltung in der Commerce-Zentralverwaltung zu verknüpfen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Einzelhandel und Handel \> Aufgabenverwaltung \> Aufgabenintegration mit Microsoft Teams**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Setzen Sie die Option **Aufgabenverwaltungsintegration aktivieren** auf **Ja**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Aufgabenverwaltung einrichten** aus. Sie sollten eine Benachrichtigung erhalten, die angibt, dass ein Stapelverarbeitungsauftrag namens **Teams-Bereitstellung** erstellt wird.
1. Gehen Sie zu **Systemadministration \> Anfragen \> Stapelverarbeitungsaufträge** und finden Sie den neuesten Auftrag mit der Beschreibung **Teams-Bereitstellung**. Warten Sie, bis dieser Auftrag ausgeführt wurde.
1. Führen Sie die den **CDX-Auftrag 1070** aus, um die Plan-ID zu veröffentlichen und Referenzen auf dem Retail Server zu speichern.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren](enable-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)
