---
title: Vergütungsaufstellung
description: Im Bericht „Vergütungsaufstellung“ werden die Vergütungen erläutert, für die ein Mitarbeiter zurzeit registriert ist.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 65bf91faba049b3fed4d80e020d77b82e48cceb6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068994"
---
# <a name="benefit-statement"></a>Vergütungsaufstellung


[!INCLUDE [PEAP](../includes/peap-2.md)]

Der Bericht **Vergütungsaufstellung** stellt eine eine Aufstellung der Vergütungen zur Verfügung, für den ein Mitarbeiter zurzeit registriert ist. Der Bericht kann von einem Mitarbeiter direkt oder vom Vergütungsadministrator aufgerufen werden. Die **Vergütungsaufstellung** umfasst eine Liste der Vergütungen, für die der Mitarbeiter registriert ist, der Abdeckungsoptionen, der Kosten sowie der registrierten Unterhaltsberechtigten oder Begünstigten. Die Aufstellung kann für einen einzelnen oder für mehrere Mitarbeiter gedruckt werden.

> [!NOTE]
Die Funktion **Vergütungsaufstellung** muss im Arbeitsbereich **Funktionsmanagement** aktiviert werden. Dazu muss die Funktion **Vergütungsverwaltung** in der Funktionsverwaltung aktiviert sein. 


## <a name="importing-the-benefit-statement"></a>Importieren der Vergütungsaufstellung 

Sie müssen die **Vergütungsaufstellung** anhand der Berichtskonfiguration impoertieren, bevor die **Vergütungsaufstellung** verfügbar ist. Führen Sie dazu die folgenden Schritte aus:

1.  Wechseln Sie zum Arbeitsbereich **Systemadministration**.

2.  Wählen Sie die Kachel **Elektronische Berichterstellung** aus.

3.  Wechseln Sie zu **Konfigurationsanbieter**, und wählen Sie **Repositorys** aus.

  ![Auswahl der Repositorys.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Wählen Sie **HR-Ressourcen** aus der Liste aus, und wählen Sie dann **Öffnen** aus.

    ![Konfigurations-Repositorys.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Wählen Sie im linken Bereich das **Vergütungsaufstellungsmodell** aus, und erweitern Sie es, sodass **Vergütungsaufstellungsformat** angezeigt wird.

6.  Wählen Sie im linken Bereich **Vergütungsaufstellungsformat** aus.

7.  Auf der rechten Seite des Bildschirms befindet sich das Inforegister **Versionen**. **Import** auswählen

    ![Inforegister „Versionen“.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Die Vergütungsaufstellung als PDF-Datei generieren

Die **Vergütungsaufstellung** wird standardmäßig als Microsoft Word-Dokument gedruckt. Zum Drucken in einem PDF-Format müssen Sie die PDF-Option in **Zielort für elektronische Berichterstellung** konfigurieren. 

1. Wechseln Sie dazu zu **Arbeitsbereich zur Systemverwaltung** > **Elektronische Berichterstellung** > **Zugehörige Links** > **Zielort für elektronische Berichterstellung**.

1.  Wählen Sie **Neu** aus.

2.  Wählen Sie im Feld **Referenz** die Option **Vergütungsaufstellungsformat** aus.

3.  Wählen Sie im Inforegister **Dateiziel** die Option **Neu** aus.

4.  Geben Sie im Feld **Name** **Vergütungsaufstellungs-PDF** ein.

5.  Wählen Sie im Feld **Name der Dateikomponente** die Option **Vergütungsaufstellung** aus.

6.  Aktivieren Sie das Kontrollkästchen **In PDF konvertieren**.

7.  Wählen Sie **Einstellungen** über die Menüoption aus. 

    ![Dateiziel.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Wählen Sie das Inforegister **Datei** und anschließend **Aktiviert** aus.

9.  Wählen Sie **OK** aus.
   
> [!NOTE]
> Die Vergütungsverwaltungsfunktion befindet sich in einem Vorschaufunktionsstatus. Im Zusammenhang mit der Verwendung der Einstellung für das E-Mail-Ziel im Bericht **Zielort für elektronische Berichterstellung** besteht ein bekanntes Problem. Sie erhalten möglicherweise eine Fehlermeldung, und die E-Mail kann nicht gesendet werden.

Die **Vergütungsaufstellung** kann über die folgenden Seiten generiert werden:

-   **Arbeitsbereich für Vergütungsverwaltung** > **Links** > **Berichte** > **Vergütungsaufstellung**

-   **Mitarbeiter (altes Formular)** > **Registerkare „Persönliche Informationen“** > **Vergütungsaufstellung**

-   **Optimierter Mitarbeitereintrag** > **Vergütungsberichte** > **Vergütungsaufstellung**

-   **Mitarbeiter-Self-Service** > **Vergütungen** > **Vergütungsaufstellung anzeigen**

> [!NOTE]
>  Der Zugriff auf die **Vergütungsaufstellung** in **Mitarbeiter-Self-Service** wird durch die Berechtigung **Vergütungsaufstellung anzeigen** gesteuert. Dies befindet sich unter der Berechtigung **Mitarbeiter-Self-Service-Vergütungen**. Diese Berechtigung wird Mitarbeitern standardmäßig gewährt.

## <a name="report-contents"></a>Berichtsinhalte

Die **Vergütungsaufstellung** druckt die bestätigte Planauswahl des Mitarbeiters einschließlich aller aufgehobenen Pläne. Das folgende Bild zeigt ein Beispiel für diesen Bericht. 

![Vergütungsaufstellungsbericht.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Der Bericht zeigt den **Plan**, die **Abdeckungsoption**, die **Mitarbeiterkosten** und die **Arbeitgeberkosten** an. Der Bericht enthält außerdem eine Liste der abgedeckten Unterhaltsberechtigten. Wenn Begünstigte mit dem Plan verknüpft sind, werden die Begünstigten und deren Verteilungspriorität sowie der Prozentsatz angezeigt.

Der Bericht **Vergütungsaufstellung** kann über das Inforegister **Einzuschließende Datensätze** FastTab auf der Seite **Vergütungsaufstellung** für mehrere Mitarbeiter gleichzeitig gedruckt werden.
