---
title: Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren
description: In diesem Artikel wird beschrieben, wie Sie die Aufgabenverwaltung zwischen Microsoft Teams und der Verkaufsstelle (POS) in Dynamics 365 Commerce synchronisieren.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746096"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie die Aufgabenverwaltung zwischen Microsoft Teams und der Verkaufsstelle (POS) in Dynamics 365 Commerce synchronisieren.

Einer der Hauptzwecke der Teams-Integration besteht darin, die Synchronisierung der Aufgabenverwaltung zwischen der POS-Anwendung und Teams zu ermöglichen. Auf diese Weise können Filialmitarbeiter entweder die POS-Anwendung oder Teams zum Verwalten von Aufgaben verwenden und müssen nicht zwischen Anwendungen wechseln.

Da Planner als Repository für Aufgaben in Teams verwendet wird, muss eine Verknüpfung zwischen Teams und Dynamics 365 Commerce bestehen. Diese Verknüpfung wird mithilfe einer bestimmten Plan-ID für ein bestimmtes Filialteam hergestellt.

Die folgenden Prozeduren zeigen, wie Sie die Synchronisierung der Aufgabenverwaltung zwischen der POS- und der Teams-Anwendung einrichten.

## <a name="link-pos-and-teams-for-task-management"></a>POS und Teams für die Aufgabenverwaltung verknüpfen

Um die POS- und Microsoft Teams-Anwendungen für die Aufgabenverwaltung in der Commerce-Zentralverwaltung zu verknüpfen, gehen Sie wie folgt vor.

> [!NOTE]
> Bevor Sie versuchen, die Aufgabenverwaltung mit Teams zu integrieren, vergewissern Sie sich, dass Sie die [Dynamics 365 Commerce und Microsoft Teams Integration](enable-teams-integration.md) aktiviert haben. 

1. Gehen Sie zu **Einzelhandel und Handel \> Aufgabenverwaltung \> Aufgabenintegration mit Microsoft Teams**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Setzen Sie die Option **Aufgabenverwaltungsintegration aktivieren** auf **Ja**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Aufgabenverwaltung einrichten** aus. Sie sollten eine Benachrichtigung erhalten, die angibt, dass ein Stapelverarbeitungsauftrag namens **Teams-Bereitstellung** erstellt wird.
1. Gehen Sie zu **Systemadministration \> Anfragen \> Stapelverarbeitungsaufträge** und finden Sie den neuesten Auftrag mit der Beschreibung **Teams-Bereitstellung**. Warten Sie, bis dieser Auftrag ausgeführt wurde.
1. Führen Sie die den **CDX-Auftrag 1070** aus, um die Plan-ID zu veröffentlichen und Referenzen auf dem Retail Server zu speichern.

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

> [!NOTE]
> Nachdem die Aufgabenliste erfolgreich in Teams veröffentlicht wurde, werden die Aufgaben in POS angezeigt. POS-Manager und Kassierer müssen dann Azure AD Anmeldung am POS aktivieren. Weitere Informationen finden Sie unter [Azure Active Directory Authentifizierung für die POS-Anmeldung aktivieren](aad-pos-logon.md) Artikel. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick Integration Dynamics 365 Commerce und Microsoft Teams](commerce-teams-integration.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren](enable-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)
