---
title: Aufgabenverwaltung konfigurieren
description: In diesem Artikel wird beschrieben, wie Aufgabenverwaltungsfunktionen in Microsoft Dynamics 365 Commerce konfiguriert werden.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: cc2d75f52b183559de344982c8e4208000af786e
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746061"
---
# <a name="configure-task-management"></a>Aufgabenverwaltung konfigurieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Aufgabenverwaltungsfunktionen in Microsoft Dynamics 365 Commerce konfiguriert werden.

Bevor Dynamics 365 Commerce Manager und Mitarbeiter die Aufgabenverwaltungsfunktionen im Handel nutzen können, muss die Aufgabenverwaltung konfiguriert werden. Zu den Konfigurationsschritten gehören die Erteilung von Berechtigungen an Manager und Mitarbeiter, die Verteilung von Berechtigungen an POS-Kunden, die Einrichtung von POS-Benachrichtigungen und die Konfiguration der Kachel **Aufgaben** auf der Startseite einer POS-Anwendung.

## <a name="configure-permissions-for-store-managers"></a>Konfigurieren von Berechtigungen für Filialleiter

Jeder Mitarbeiter in einem bestimmten Geschäft kann alle Aufgaben, die diesem Geschäft zugeordnet sind, einsehen. Er kann auch den Status der ihm zugeordneten Aufgaben aktualisieren. Personen wie Filialleiter müssen jedoch über Aufgabenmanagementberechtigungen verfügen, um Aufgaben zu verwalten, die der Filiale zugeordnet sind, und um Einzweck-Aufgaben zu erstellen.

Führen Sie die folgenden Schritte aus, um Aufgabenverwaltungsberechtigungen für Filialleiter zu konfigurieren.

1. Gehen Sie zu **Retail and Commerce \> Mitarbeiter \> Berechtigungsgruppen**.
1. Wählen Sie eine bestimmte Berechtigungsgruppe (z.B. **Manager**) und wählen Sie dann **Bearbeiten**.
1. Setzen Sie auf der Registerkarte **Berechtigungen** die Option **Aufgabenverwaltung erlauben** auf **Ja**.
1. Fügen Sie auf der Registerkarte **Benachrichtigungen** den Vorgang **Aufgabenverwaltung** hinzu und geben Sie einen Wert in das Feld **Anzeigereihenfolge** ein. Geben Sie z.B. **2** ein, wenn die Operation **Auftragserfüllung** bereits einen Wert von **Anzeigereihenfolge** von **1** hat.
    
> [!NOTE]
> Wenn eine nicht leitende Person die Berechtigung zur Aufgabenverwaltung in der Kasse haben muss, können Sie der Person die Berechtigung erteilen. Alternativ dazu können Sie eine neue Berechtigungsgruppe für Nicht-Manager anlegen und die Option **Aufgabenverwaltung erlauben** auf **Ja** setzen.

Die folgende Abbildung zeigt, wie Sie Aufgabenverwaltungsberechtigungen für Filialleiter konfigurieren können.

![Konfigurieren von Aufgabenverwaltungsberechtigungen für Filialleiter.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Konfigurieren Sie Berechtigungen für Mitarbeiter

Die Mitarbeiter müssen über Berechtigungen zur Erstellung von Aufgabenlisten, zur Verwaltung von Zuordnungskriterien und zur Konfiguration der Wiederholung von Aufgabenlisten verfügen. Um diese Berechtigungen zu konfigurieren, ordnen Sie die Mitarbeiter der Rolle **Aufgabenmanager** zu.

Um die Berechtigungen für einen Mitarbeiter zu konfigurieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Retail and Commerce \> Mitarbeiter \> Benutzer**.
1. Wählen Sie einen Mitarbeiter aus.
1. Wählen Sie auf der Registerkarte **Rollen des Benutzers** **Rollen zuweisen**.
1. Wählen Sie im Dialogfenster **Rollen zu Benutzer** die Rolle **Retail Task Manager** und dann **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Berechtigungen an POS-Kunden verteilen

Bevor Mitarbeiter POS-Clients verwenden können, müssen die Berechtigungen an diese Clients verteilt und synchronisiert werden.

Führen Sie die folgenden Schritte aus, um Berechtigungen an POS-Clients zu verteilen.

1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Wählen Sie den Verteilungsplan **1060** (**Mitarbeiter**) und wählen Sie dann **Jetzt ausführen**.
1. Wählen Sie den Verteilungsplan **1070** (**Kanalkonfiguration**) und wählen Sie dann **Jetzt ausführen**.

## <a name="configure-pos-notifications-for-tasks"></a>Konfigurieren Sie POS-Benachrichtigungen für Aufgaben

Die Aufgabenverwaltung muss so konfiguriert werden, dass Benachrichtigungen in der POS-Anwendung verfügbar sind.

Um POS-Benachrichtigungen für Aufgaben zu konfigurieren, führen Sie folgende Schritte aus.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellung \> POS-Einrichtung \> POS \> POS-Operationen**.
1. Suchen Sie den Vorgang **1400** (**Taskmanagement**) und markieren Sie dafür das Ankreuzfeld **Benachrichtigungen aktivieren**.

Die folgende Abbildung zeigt die Operation **Aufgabenverwaltung** auf der Seite **POS-Operationen**.

![Vorgang der Aufgabenverwaltung auf der Seite POS-Operationen.](media/HQ-POS-Tasks-Notifications.png)

Weitere Informationen über die Konfiguration von POS-Benachrichtigungen finden Sie im Artikel [Bestellbenachrichtigungen in der Verkaufsstelle (POS)](notifications-pos.md) anzeigen.

> [!NOTE]
> Wenn Sie Ihre Änderungen speichern, wird die folgende Warnmeldung angezeigt: **Der Vorgangsparameter wird im Schaltflächenraster-Designer nicht für eine Vorgangs-ID aktiviert, die gleich oder geringer als 4000 ist. Wenn Sie einen benutzerdefinierten Vorgang erstellen und Parameter vom Schaltflächenraster-Designer übergeben möchten, dann verwenden Sie eine Vorgangs-ID, die höher als 4000 ist.** Klicken Sie auf **Schließen**, um das Dialogfeld zu schließen.


## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Konfigurieren Sie die Tasks-Kachel auf der Homepage einer POS-Anwendung

Bevor Sie die Kachel **Aufgaben** auf der Startseite einer POS-Anwendung konfigurieren, finden Sie unter [Bildschirm-Layouts für die Verkaufsstelle (POS)](pos-screen-layouts.md) Informationen über die Konfiguration und das Hinzufügen neuer Schaltflächen zu einem POS-Bildschirm-Layout.

Um die Kachel **Aufgaben** auf der Homepage einer POS-Anwendung zu konfigurieren, gehen Sie wie folgt vor.

1. Gehen Sie zu **Retail and Commerce \> Kanal-Einrichtung \> POS-Einrichtung \> POS \> Bildschirm-Layouts**.
1. Wählen Sie ein Bildschirmlayout, wählen Sie eine Layoutgröße und wählen Sie ein Schaltflächenraster.
1. Wählen Sie auf der Registerkarte **Schaltflächenraster** **Designer**, um das ausgewählte Schaltflächenraster zu bearbeiten.
1. Fügen Sie eine **Aufgaben** Kachel zum entsprechenden Abschnitt der Homepage hinzu.

Die folgende Abbildung zeigt ein Beispiel für eine Kachel **Aufgaben** auf einer POS-Homepage.

![Aufgaben-Kachel auf einer POS-Homepage.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Aufgabenverwaltung – Übersicht](task-mgmt-overview.md)

[Aufgabenlisten erstellen und Aufgaben hinzufügen](task-mgmt-create-lists.md)

[Arbeitspläne den Filialen oder Mitarbeitern zuweisen](task-mgmt-assign-lists.md)

[Aufgabenverwaltung in POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
