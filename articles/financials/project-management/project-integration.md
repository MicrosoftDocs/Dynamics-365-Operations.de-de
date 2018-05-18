---
title: Microsoft Project Client-Integration
description: "Die Planung und Verwaltung eines Projektzeitplans kann komplex sein. Deshalb müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe bewältigen können. Die Integration mit Microsoft Project Client bietet Unterstützung, um einen Projektstrukturplan zu öffnen und zu verwalten."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Microsoft Project Client-Integration

[!include [banner](../includes/banner.md)]

Die Planung und Verwaltung eines Projektzeitplans kann komplex sein. Deshalb müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe bewältigen können. Die Integration mit Microsoft Project Client bietet Unterstützung, um einen Projektstrukturplan zu öffnen und zu verwalten. Der Projektmanager kann beliebige Änderungen zurück zum Finance and Operations-Projektstrukturplan veröffentlichen.

> [!NOTE]
> Wenn Sie das Update vom Juli für Microsoft Dynamics 365 for Finance and Operations, verwenden, müssen Sie auch KB 4054797 und 4055884 installieren.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurieren des Microsoft Project Client-Add-Ins
Um die Integration mit Microsoft Project Client zu ermöglichen, muss ein Microsoft Dynamics 365-Add-In der Microsoft Project-Anwendung des Clients des Benutzers installiert werden. Dies erfolgt, indem der **Projektverwaltungsarbeitsbereich** geöffnet wird.

•   Klicken Sie auf **Project Client-Add-In konfigurieren** aus dem Abschnitt **Links** > **Setup** des Arbeitsbereichs.

•   Klicken Sie auf **Öffnen**, und klicken Sie dann auf **Ausführen**, wenn Sie dazu aufgefordert werden.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Öffnen und Bearbeiten eines vorhandenen Entwurfs-Projektstrukturplans in Microsoft Project Client
Wenn für ein Projekt in Finance and Operations bereits ein Projektstrukturplan erstellt wird, kann der Projektstrukturplan in der Microsoft Project Client-Anwendung geöffnet werden, wenn der Projektstrukturplan sich im Entwurfsstatus befindet. Um von der Seite **Project** aus zu öffnen, klicken Sie auf den Link **In Microsoft Project öffnen** von der Registerkarte **Plan**. Diese Seite kann auch von innerhalb der Microsoft Project Client-Anwendung aus geöffnet werden, indem Sie auf **Öffnen** in der Registerkarte **Microsoft Dynamics 365** klicken. Wählen Sie die **Juristische Person** und **Projekt** aus der Liste aus.

> [!NOTE]
> Wenn Sie Internet Explorer als Browser verwenden, müssen Sie auf **Speichern** klicken, um manuell vom Speicherplatz aus zu öffnen, zu dem die Datei heruntergeladen wird. Oder klicken Sie auf **Speichern und öffnen**, um die Datei in Microsoft Project Client zu öffnen. Benennen Sie den Dateinamen beim Speichern nicht um.

Bevor Sie irgendwelche Bearbeitungen an der Datei mithilfe von Microsoft Project Client vornehmen, müssen Sie sie zuerst auschecken. Klicken Sie auf **Auschecken** in der Registerkarte **Microsoft Dynamics 365**. Dadurch wird verhindert, dass andere Benutzer den Projektstrukturplan zur gleichen Zeit von innerhalb Finance and Operations aus bearbeiten. Um den Projektstrukturplan zu veröffentlichen, nachdem Sie irgendwelche Bearbeitungen abgeschlossen haben, klicken Sie auf **Einchecken** auf der Registerkarte **Microsoft Dynamics 365**.

Wenn ein Projektteam bereits dem Projekt in Finance and Operations hinzugefügt wurde, wird die Ressourcenliste mit den Teammitgliedern aufgefüllt. Wenn ein Projektteam noch nicht dem Projekt hinzugefügt wurde, können Sie Ressourcen auswählen und das Team innerhalb von Microsoft Project Client erstellen, indem Sie auf die Schaltfläche **Ressourcen** auf der Registerkarte **Microsoft Dynamics 365** klicken. 

Die folgenden Daten werden zurück zu Finance and Operations als Teil des Eincheckprozesses synchronisiert.

•   Aufgabenname

•   Anfangsdatum

•   Abschlussdatum

•   Vorherige Aktivitäten

•   Ressourcennamen

•   Kategorie:

•   Ressourcenkategorie

•   Arbeitsstunden

•   Notizen

•   Priorität

> [!NOTE]
> Wenn Sie irgendwelche weitere Spalten zu Ihrer Microsoft Project Client-Datei hinzufügen, werden sie nicht in der Datei gespeichert und werden nicht angezeigt, wenn die Datei wieder geöffnet wird.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Erstellen des Projektstrukturplans für ein vorhandenes Projekt mithilfe von Microsoft Project Client
Um einen neuen Projektstrukturplan mithilfe von Microsoft Project Client zu erstellen, folgen Sie diesen Schritten:


1.  Öffnen Sie Microsoft Project Client.

2.  Klicken Sie auf der Registerkarte **Microsoft Dynamics 365** auf **Öffnen**.

3.  Wählen Sie die **Juristische Person** für das Projekt aus.

4.  Wählen Sie das **Projekt** aus.

5.  Klicken Sie auf **Auschecken** auf der Registerkarte **Microsoft Dynamics 365**.

6.  Wenn Sie bereit sind, nach Finance and Operations zu veröffentlichen, klicken Sie auf **Einchecken** auf der Registerkarte **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Ersetzen des vorhandenen Projektstrukturplans für ein vorhandenes Projekt mithilfe von Microsoft Project Client
Um einen neuen Projektstrukturplan mithilfe von Microsoft Project Client zu erstellen und einen vorhandenen Projektstrukturplan für ein vorhandenes Projekt zu ersetzen, folgen Sie diesen Schritten:

1.  Öffnen Sie den Microsoft Project Client.

2.  Erstellen Sie den Zeitplan in Microsoft Project Client.

3.  Klicken Sie auf der Registerkarte **Microsoft Dynamics 365** auf **Änderungen speichern** > **Vorhandenes Projekt ersetzen**.

4.  Wählen Sie die **Juristische Person** für das Projekt aus.

5.  Wählen Sie das **Projekt** aus.

6.  Klicken Sie auf **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Erstellen eines neuen Projekts von Microsoft Project Client aus


1.  Öffnen Sie den Microsoft Project Client.

2.  Erstellen Sie den Zeitplan in Microsoft Project Client.

3.  Klicken Sie auf der Registerkarte **Microsoft Dynamics 365** auf **Änderungen speichern** > **In neuem Projekt speichern**.

4.  Wählen Sie die **Juristische Person** für das Projekt aus.

5.  Geben Sie die **Projektkennung** ein, falls erforderlich.

6.  Geben Sie den **Projektnamen** ein.

7.  Wählen Sie den **Projekttyp**, die **Projektgruppe** und die **Projektvertragskennung** aus. Alternativ können Sie einen neuen Projektvertrag erstellen, indem Sie auf **Neu** klicken.

8.  Wählen Sie den **Kalender** aus, der für die Ressourcenzuordnung zu verwenden ist.

11. Klicken Sie auf **OK**.

