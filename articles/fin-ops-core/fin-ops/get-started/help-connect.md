---
title: Verbinden des Hilfesystems
description: Dieses Thema beschreibt die Komponenten des Hilfe-Systems für Finance and Operations-Apps und bietet einen Überblick darüber, wie sie verbunden werden, und eine Zusammenfassung darüber, wie eine benutzerdefinierte Hilfe erstellt werden kann.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006171"
---
# <a name="connect-the-help-system"></a>Verbinden des Hilfesystems

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Komponenten des Hilfesystems für Finance and Operations-Apps wie Dynamics 365 Finance, Supply Chain Management, Commerce und Human Resources beschrieben. Es bietet einen Überblick darüber, wie diese Komponenten und eine Zusammenfassung zu aus, wie Sie benutzerdefinierte Hilfe erstellt.

## <a name="help-architecture"></a>Hilfearchitektur

Die folgende Abbildung zeigt Teile des Hilfesystems. Das Hilfesystem zieht Artikel aus https://docs.microsoft.com und zeigt Aufgabenleitfäden aus dem Geschäftsprozessmodellierer in Microsoft Dynamics Lifecycle Services (LCS) an.

> [!NOTE]
> Die Funktionen, die im Diagramm mit einem Sternchen (\*) aufgeführt sind (), sind geplant, aber noch nicht verfügbar.

[![Hilfearchitektur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Verbindung des Hilfesystems

> [!NOTE]
> Die Registerkarte **Aufgabenleitfäden** ist derzeit nicht in Dynamics 365 Human Resources oder Commerce verfügbar. Wir arbeiten derzeit daran, diese Funktion in einer künftigen Version zu ermöglichen. Die Aufgabenleitfäden in der Erste Schritte-Erfahrung in Human Resources bleiben verfügbar, um Grundfunktionen abzudecken. Prozedurale Hilfe ist für Human Resources und Commerce auch auf der Website docs.microsoft.com verfügbar.

Mit dem Formular "**Systemparameter**" verbinden Systemadministratoren die Teile des Hilfesystems für eine Implementierung.

[![Systemparameterformular mit Hilfe-Einstellungen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Gehen Sie auf der Seite **Systemparameter** folgendermaßen vor:

> [!IMPORTANT]
> Beim erstmaligen Öffnen der Registerkarte **Hilfe** müssen Sie die Verbindung zu den Lifecycle Services herstellen. Klicken Sie auf den Link mitten im Formular, warten Sie auf die Verbindung, schließen Sie das Dialogfeld, und klicken Sie anschließend auf **OK**, um zur Seite **Systemparameter** zu gelangen.
>
> [![Mit LCS verbinden](./media/connect-to-lcs-crop-1024x365.png "Mit LCS verbinden")](./media/connect-to-lcs-crop.png)

1. Wählen Sie das Projekt Lifecycle Services, um eine Verbindung herzustellen.
2. Wählen Sie die BPM-Bibliotheken (innerhalb des ausgewählten Projekts) aus, von denen Sie die Aufgabenaufzeichnungen abrufen wollen.
3. Wählen Sie die Anzeigereihenfolge der BMP-Bibliotheken aus. So können Sie bestimmen, in welcher Reihenfolge Aufgabenaufzeichnungen aus den Bibliotheken im Bereich **Hilfe** angezeigt werden.

Nach der Durchführung dieser Schritte können Sie den Bereich **Hilfe** öffnen und auf die Registerkarte **Aufgabenleitfäden** klicken. Sie sehen dann die Aufgabenleitfäden, die für die Seite gelten, auf der Sie derzeit in Finance and Operations-Apps sind. Wenn keine Aufgabenhandbücher gefunden werden, können Sie Schlüsselwörter eingeben, um die Suche genauer zu definieren.

### <a name="showing-translated-task-guides"></a>Zeigt übersetzte Aufgabenleitfäden

Übersetzte Aufgabenleitfäden wurden mit der APQC Unified Bibliothek (Mai 2016) und der Erste Schritte-Bibliothek zuerst geliefert. Stellen Sie in Finance and Operations-Apps sicher, dass die mit der Mai-Bibliothek verbunden sind, damit Sie die lokalisierte Aufgabenleitfaden-Hilfe sehen können. Die im Aufgabenleitfaden angezeigte Sprache wird für jeden Benutzer durch Spracheinstellungen unter **Optionen** &gt; **Voreinstellungen** gesteuert.

> [!NOTE]
> Auch wenn viele Aufgabenleitfäden übersetzt wurden, zeigt der Client im Moment nicht die übersetzten Namen der Aufgabenleitfäden an. Außerdem sind zum jetzigen Zeitpunkt nur die im Februar 2016 veröffentlichten Aufgabenleitfäden als Übersetzung in der Mai-Bibliothek verfügbar. Wir werden eine aktualisierte Bibliothek mit zusätzlichen Übersetzung veröffentlichen.
>
> - Wenn ein Aufgabenleitfaden übersetzt wurde, wird beim Öffnen der gesamte Text des Leitfadens in der ausgewählten Sprache angezeigt.
> - Wenn ein Aufgabenleitfaden noch nicht übersetzt wurde, wird beim Öffnen nur ein Teil des Texts (der Text der Steuerelemente) in der ausgewählten Sprache angezeigt.

## <a name="creating-custom-help"></a>Erstellen einer benutzerdefinierten Hilfe

Sie können Aufgabenleitfäden verwenden, um benutzerdefinierte Hilfe zu erstellen, oder eine Verbindung zwischen einer Website und dem Hilfebereich erstellen.

### <a name="create-custom-help-with-task-guides"></a>Benutzerdefinierte Hilfe mit Aufgabenleitfäden erstellen

Sie können eine benutzerdefinierte Hilfe für Finance, Supply Chain Management und Commerce erstellen, indem Sie Aufgabenaufzeichnungen erstellen, die Ihre Implementierung widerspiegeln, und diese in einer LCS Business Process Library speichern. Sie können keine benutzerdefinierten Aufgabenleitfäden für Human Resources erstellen.

Wenn Partner eine Bibliothek auf eine Unternehmensbibliothek hochstufen und in eine Lösung aufnehmen, wir diese für die Kunden verfügbar. Sie können eine Kopie der globalen APQC Unified Bibliothek für Dynamics AX erstellen und dann Ihre Kopie öffnen, Aufgabenaufzeichnungen aus dieser öffnen, sie ändern und dann Aufzeichnungen mit den Änderungen speichern. Weitere Informationen finden Sie unter [Aufgaberecorder-Ressourcen](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Benutzerdefinierte Website verbinden

Microsoft hat ein Whitepaper und einen Beispielcode bereitgestellt, die beschreiben wie ein benutzerdefinierter Hilfewebsite mit dem Hilfebereich verbunden wird. Weitere Informationen finden Sie hier:

- [Erstellen benutzerdefinierter Hilfe für Finance and Operations-Apps (Whitepaper)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Benutzerdefiniertes Hilfe-GitHub-Repository](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hilfesystem](help-overview.md)

[Aufgaberecorder-Ressourcen](../../dev-itpro/user-interface/task-recorder.md)

[Dokumentation oder Schulung mit der Aufgabenaufzeichnung erstellen](../../dev-itpro/user-interface/task-recorder-training-docs.md)
