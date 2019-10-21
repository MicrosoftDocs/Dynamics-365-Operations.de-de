---
title: Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen
description: Die Schritte in diesem Thema erläutern, wie ein Regulatory configuration service (RCS)-Benutzer eine neue Modellzuordnung für elektronische Berichterstellung (ER) entwerfen kann, indem er die Metadaten in Finance and Operations verwendet.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a476163ba6f66ab60ed8bfea6198d02f13ac5136
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182714"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Regulatory Configuration Service (RCS)-Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Modellzuordnung für „Elektronische Berichterstellung (ER)“ entwerfen kann, indem er die Metadaten in Finance and Operations verwendet. Zugriff auf Anwendungs-Metadaten erfolgt online über die RCS verbundene Anwendungen. Beispiel-ER-Modellzuordnung wird konfiguriert, um auf Außenhandelstransaktionen zuzugreifen. Um diese Schritte auszuführen, müssen Sie in RCS zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. Wenn Sie die Schritte im Thema [Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](access-application-metadata-er-configuration.md) abgeschlossen haben, fahren Sie mit der [Beispielseite für elektronische Berichterstellung](https://go.microsoft.com/fwlink/?linkid=862266) fort, um die folgenden ER-Konfigurationen herunterzuladen und zu speichern: Außenhandelsmetadaten.xml; Außenhandelsmodel.xml; Außenhandelszuordnung.xml und führen Sie dann die Schritte in der Prozedur aus.

## <a name="prerequisites"></a>Voraussetzungen
1. Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**. 
2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. 

## <a name="get-required-er-configurations"></a>Erforderliche ER-Konfigurationen abrufen
1. Klicken Sie auf **Berichterstellungskonfigurationen**. 
2. Wenn Sie die Schritte in der Prozedur [(RCS) Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](access-application-metadata-er-configuration.md) bereits abgeschlossen haben, haben Sie bereits alle erforderlichen ER-Konfigurationen (Außenhandelsmetadaten, Modell- und Zuordnungskonfigurationen) in der aktuellen RCS-Instanz. Sie können alle übrigen Schritte dieser Unteraufgabe überspringen. 
3. Klicken Sie auf **Austauschen**. 
4. Klicken Sie auf **Aus XML-Datei laden**. 
5. Klicken Sie auf **Durchsuchen** und wählen die Datei **metadata.xml für Außenhandel** aus. 
6. Klicken Sie auf **OK**. 
7. Klicken Sie auf **Austauschen**. 
8. Klicken Sie auf **Aus XML-Datei laden**. 
9. Klicken Sie auf **Durchsuchen** und wählen die Datei **model.xml für Außenhandel** aus. 
10. Klicken Sie auf **OK**. 
11. Klicken Sie auf **Austauschen**. 
12. Klicken Sie auf **Aus XML-Datei laden**. 
13. Klicken Sie auf **Durchsuchen** und wählen die Datei **mapping.xml für Außenhandel** aus. 
14. Klicken Sie auf **OK**. 

## <a name="register-a-connected-application"></a>Registrieren Sie eine verbundene Anwendung.
1. Schließen Sie die Seite. 
2. Schließen Sie die Seite. 
3. Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**. 
4. Klicken Sie auf **Verbundene Anwendung**. 
5. Überprüfen Sie, dass die konfigurierte Anwendung Azura-basiert ist und der aktuelle RCS-Benutzer darauf zugreifen kann. Es ist auch erforderlich, dass der aktuelle RCS-Benutzer Zugriff auf die ausgewählte Anwendung und als Benutzer dieser Anwendung registriert wurde. Dies spielt eine Rolle bei seinen Rechten für den Zugriff auf die Metadaten der Anwendung. 
6. Klicken Sie auf **Neu**. 
7. Geben Sie im Feld **Name** „MyConnectedApp“ ein. 
8. Geben Sie im Feld **Anwendung** „https:// mycompany.operations.dynamics.com“ ein. 
9. Geben Sie im Feld **Mandant** „mycompany.onmicrosoft.com“ ein. 
10. Klicken Sie auf **Speichern**. 
11. Wenn Sie Verbindungen zur konfigurierten Anwendung überprüfen, klicken Sie auf der Seite **Mit Remote-Anwendung verbinden** auf den Link **Hier klicken, um Verindung mit der ausgewählten Remote-Anwendung herzustellen**. 
12. Klicken Sie auf **Verbindung prüfen**. 
13. Klicken Sie auf **Schließen**. 
14. Wenn die Verbindungsprüfung erfolgreich war, werden Versions- und Mandantendetails für die konfigurierte Anwendung im aktuellen Raster aktualisiert. 

## <a name="review-existing-model-mapping-configuration"></a>Überprüfen einer vorhandenen Modellzuordnungskonfiguration
1. Schließen Sie die Seite. 
2. Klicken Sie auf **Berichterstellungskonfigurationen**. 
3. Erweitern Sie **Außenhandelsmodell** in der Struktur. 
4. Wählen Sie in der Struktur **Außenhandelsmodell\Außenhandelszuordnung** aus. 
5. Erweitern Sie den Abschnitt **Voraussetzungen**. 

> [!NOTE]
> Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration. Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird. 

6. Klicken Sie auf **Designer**. 
7. Klicken Sie auf **Designer**. 
8. Wählen Sie in der Struktur **Dynamics 365 for Operations\Tabellendatensätze** aus. 
9. Klicken Sie auf **Stamm hinzufügen**. 
10. Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus. 

> [!NOTE]
> Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration. Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird. 

11. Klicken Sie auf **Abbrechen**. 
12. Schließen Sie die Seite. 
13. Schließen Sie die Seite. 

## <a name="assign-connected-application-to-model-mapping"></a>Weisen Sie die verbundene Anwendung der Modellzuordnung zu 
1. Klicken Sie auf **Bearbeiten**. 
2. Wählen Sie die **MyConnectedApp**-Anwendung aus. 

> [!NOTE]
> Momentan bezieht sich diese Zuordnung auf die Metadaten der ausgewählten verbundenen Anwendung. Wenn sich dieselbe Zuordnung gleichzeitig auf die Metadatenkonfiguration sowie die verbundene Anwendung bezieht, werden Metadaten der verbundenen Anwendung verwendet. 

3. Klicken Sie auf **Designer**. 
4. Klicken Sie auf **Designer**. 
5. Wählen Sie in der Struktur **Dynamics 365 for Operations\Tabellendatensätze** aus. 
6. Klicken Sie auf **Stamm hinzufügen**. 
7. Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus. 

> [!NOTE]
> Mehr als zwei Anwendungstabellen wurden nun angeboten, da diese Zuordnung alle Metadaten der verbundenen Anwendung verwenden, die ihr zugeordnet ist. 

8. Klicken Sie auf **Abbrechen**. 
9. Klicken Sie auf **Überprüfen**. 

> [!NOTE]
> Es wurden erfolgreich Elemente des Datenmodells mit Datenquellenelementen gebunden, die mit Details aus Metadaten der verbundenen Anwendung verwendet, die dieser Zuordnung zugewiesen wurde. 

10. Schließen Sie die Seite. 
11. Schließen Sie die Seite. 

Wenn Sie diese Modellzuordnung überprüfen müssen, indem Sie Metadaten einer anderen Versionsanwendung verwenden, registrieren Sie eine andere verbundene Anwendung, weisen Sie sie dieser Modellzuordnung zu und prüfen Sie sie anhand der neuen Metadaten.