---
title: Konfigurieren Sie die Hilfefunktion für Finanz- und Betriebs-Apps
description: Dieser Artikel enthält Informationen zu den Komponenten des Hilfesystems für einige Microsoft Dynamics 365-Apps.
author: edupont04
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.form: SystemParameters
ms.openlocfilehash: 75f3cc1b76b2a38d4004c4fa3f86a528a7eebc3f
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538522"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Konfigurieren Sie die Hilfefunktion für Finanz- und Betriebs-Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In diesem Artikel finden Sie eine Übersicht über die Komponenten des Hilfesystems für Finanz- und Betriebs-Apps, wie Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce und Dynamics 365 Human Resources. In diesem Artikel wird auch erläutert, wie diese Apps verbunden werden, und es wird eine Zusammenfassung des Prozesses zum Erstellen einer benutzerdefinierten Hilfe bereitgestellt.

## <a name="help-architecture"></a>Hilfearchitektur

Finanz- und Betriebs-Apps enthalten konzeptionelle Übersichten und andere Themen, die auf der [Microsoft Dynamics 365 Dokumentation](/dynamics365/) Seite veröffentlicht werden. Auf diesen Inhalt kann dann über den Bereich **Hilfe** des Produkts zugegriffen werden. Die folgende Abbildung zeigt Teile des Hilfesystems.

[![Hilfearchitektur.](./media/help-architecture.png)](./media/help-architecture.png)

Das produktinterne Hilfesystem zieht Artikel von Microsoft Learn und anderen verbundenen Websites. Außerdem werden Aufgabenleitfäden abgerufen, die im Business Process Modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS) gespeichert sind.

## <a name="adding-task-guides"></a>Hinzufügen von Aufgabenleitfäden

> [!NOTE]
> Die Registerkarte **Aufgabenleitfäden** ist derzeit nicht in Human Resources oder Commerce verfügbar. <!--We are currently working to enable this functionality in a future release.--> Die Aufgabenleitfäden in der Umgebung „Erste Schritte“ in Human Resources bleiben verfügbar, um die grundlegenden Funktionen abzudecken. Auf der Website [Microsoft Dynamics 365-Dokumentation](/dynamics365/) sind Verfahrensweisen für Human Resources und für Commerce verfügbar.

Auf der Seite **Systemparameter** können Systemadministratoren den Zugriff auf die relevanten Aufgabenleitfadenbibliotheken für eine Implementierung konfigurieren.

> [!NOTE]
> - Zum Konfigurieren der Hilfe müssen Sie sich mit einem Konto des Mandanten anmelden, für den die App bereitgestellt ist.
> - Eine LCS-Bibliothek kann nicht aus einer Instanz der App verbunden werden, die auf einer lokalen virtuellen Festplatte (VHD) ausgeführt wird.

[![Systemparameterformular mit Hilfe-Einstellungen.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Führen Sie die folgenden Schritte auf der Seite **Systemparameter** aus, um Aufgabenleitfäden für eine Lösung zu konfigurieren.

> [!IMPORTANT]
> Beim erstmaligen Öffnen der Registerkarte **Hilfe** müssen Sie die Verbindung zu den Lifecycle Services herstellen. Wählen Sie den Link in der Mitte des Formulars aus, warten Sie, bis die Verbindung hergestellt wurde, schließen Sie das Dialogfeld, und wählen Sie dann **OK** aus, um zur Seite **Systemparameter** zu gelangen.
>
> [![Mit LCS verbinden](./media/connect-to-lcs-crop-1024x365.png "Mit LCS verbinden.")](./media/connect-to-lcs-crop.png)

1. Wählen Sie das Projekt Lifecycle Services, um eine Verbindung herzustellen.
2. Wählen Sie die BPM-Bibliotheken (innerhalb des ausgewählten Projekts) aus, von denen Sie die Aufgabenaufzeichnungen abrufen wollen.
3. Wählen Sie die Anzeigereihenfolge der BMP-Bibliotheken aus. Anhand der Anzeigereihenfolge wird die Reihenfolge definiert, in der Aufgabenaufzeichnungen aus den Bibliotheken im Bereich **Hilfe** angezeigt werden.

Nachdem Sie diese Schritte durchgeführt haben, können Sie den Bereich **Hilfe** öffnen und die Registerkarte **Aufgabenanleitungen** auswählen. Sie sehen nun die Anleitungen, die für die Seite gelten, auf der Sie sich gerade in Finanz- und Betriebs-Apps befinden. Wenn keine Aufgabenhandbücher gefunden werden, können Sie Schlüsselwörter eingeben, um die Suche genauer zu definieren.

### <a name="showing-translated-task-guides"></a>Zeigt übersetzte Aufgabenleitfäden

Übersetzte Aufgabenleitfäden wurden zuerst in der APQC Unified Bibliothek (Mai 2016) und der Erste Schritte-Bibliothek veröffentlicht. Stellen Sie sicher, dass Ihre Dynamics 365-Lösung mit der Bibliothek vom Mai 2016 verbunden ist, um die lokalisierte Hilfe zu Aufgabenleitfäden anzuzeigen. Benutzer können die Sprache ändern, in der ein Aufgabenleitfaden angezeigt wird, indem Sie die Spracheinstellungen unter **Optionen** &gt; **Einstellungen** ändern.

> [!NOTE]
> Obwohl viele Aufgabenleitfäden übersetzt wurden, zeigt der Client die übersetzten Namen der Aufgabenleitfäden derzeit nicht an. Außerdem sind nur die im Februar 2016 veröffentlichten Aufgabenleitfäden als Übersetzung in der Bibliothek vom Mai 2016 verfügbar. Microsoft wird eine aktualisierte Bibliothek mit zusätzlichen Übersetzungen veröffentlichen.
>
> - Wenn ein Aufgabenleitfaden übersetzt wurde, wird beim Öffnen der gesamte Text des Leitfadens in der ausgewählten Sprache angezeigt.
> - Wenn ein Aufgabenleitfaden noch nicht übersetzt wurde, wird beim Öffnen nur ein Teil des Texts (der Text der Steuerelemente) in der ausgewählten Sprache angezeigt.

## <a name="adding-custom-help"></a>Hinzufügen einer benutzerdefinierten Hilfe

Sie können Aufgabenleitfäden verwenden, um eine benutzerdefinierte Hilfe zu erstellen, oder eine Verbindung zwischen einer Website und dem Bereich **Hilfe** herstellen.

### <a name="create-custom-help-by-using-task-guides"></a>Benutzerdefinierte Hilfe mit Aufgabenleitfäden erstellen

Sie können eine benutzerdefinierte Hilfe für die unterstützten Apps erstellen, indem Sie Aufgabenaufzeichnungen erstellen, die die Implementierung widerspiegeln, und diese anschließend in einer Geschäftsprozessbibliothek in LCS speichern. Sie können keine benutzerdefinierten Aufgabenleitfäden für Human Resources erstellen.

Wenn Partner eine Bibliothek auf eine Unternehmensbibliothek hochstufen und in eine Lösung aufnehmen, wird diese für die Kunden verfügbar. Sie können auch eine Kopie der APQC Unified-Bibliothek erstellen und dann Ihre Aufgabenaufzeichnungen in der Kopie öffnen, bearbeiten und Ihre Änderungen anschließend speichern. Weitere Informationen finden Sie unter [Aufgaberecorder-Ressourcen](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Benutzerdefinierte Hilfewebsite verbinden

Finanz- und Betriebs-Apps werden selten in ihrem standardmäßigen Formular verwendet. Stattdessen wird die Lösung den Anforderungen der Organisation entsprechend angepasst und erweitert. Sie können die Hilfeumgebung auch anpassen und erweitern. Sie können dem Bereich **Hilfe** des Produkts beispielsweise eine benutzerdefinierte Hilfe hinzufügen.

Microsoft hat ein Toolkit bereitgestellt, mit dem Sie benutzerdefinierte Hilfe bereitstellen und mit dem Bereich **Hilfe** verbinden können. Weitere Informationen zum Einrichten einer benutzerdefinierten Hilfelösung, die mit dem Bereich **Hilfe** verbunden ist, findne Sie unter [Übersicht über benutzerdefinierte Hilfe](../../dev-itpro/help/custom-help-overview.md).

Wenn Sie mit Microsoft an Tools und Prozessen zum Anpassen der Hilfe zusammenarbeiten möchten, füllen Sie das Formular unter [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) aus.

## <a name="see-also"></a>Siehe auch

[Hilfesystem](help-overview.md)  
[Übersicht über benutzerdefinierte Hilfe](../../dev-itpro/help/custom-help-overview.md)  
[Aufgaberecorder-Ressourcen](../../dev-itpro/user-interface/task-recorder.md)  
[Dokumentation oder Schulung mit der Aufgabenaufzeichnung erstellen](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Benutzerdefiniertes Hilfe-GitHub-Repository](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
