---
title: Erstellen Sie ein Azure-Speicherkonto im Azure-Portal
description: Dieses Thema erklärt, wie Sie ein Azure Speicherkonto für die Elektronische Rechnungsstellung erstellen.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3d9647e234b3603ef6305ec6031a793b744bbe98
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371679"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Erstellen Sie ein Azure-Speicherkonto im Azure-Portal

[!include [banner](../includes/banner.md)]

Alle elektronischen Dateien, die vom Dienst für die elektronische Rechnungsstellung erzeugt werden oder während der Verarbeitung an den Dienst gehen, werden in Ihren Containern des Speicherkontos Microsoft Azure gespeichert. Um sicherzustellen, dass die elektronische Rechnungsstellung auf diese Container zugreifen kann, müssen Sie dem Dienst für die elektronische Rechnungsstellung das Token für die gemeinsame Zugriffssignatur (SAS) des Speicherkontos zur Verfügung stellen. Um sicherzustellen, dass das Token sicher gespeichert wird, sollten Sie das SAS-Token nicht direkt bereitstellen. Speichern Sie sie stattdessen in einem Azure Key Vault, und geben Sie ein Azure Key Vault Geheimnis an.

1. Öffnen Sie das Speicherkonto, das Sie mit dem Dienst für die elektronische Rechnungsstellung verwenden möchten.
2. Gehen Sie zu **Einstellungen** \> **Konfiguration** und vergewissern Sie sich, dass der Parameter **Öffentlichen Zugriff auf Blob zulassen** auf **Aktiviert** festgelegt ist.
3. Gehen Sie zu **Datenspeicher** \> **Containers** und erstellen Sie einen Container.
4. Geben Sie einen Namen für den Container ein und legen Sie das Feld **Öffentliche Zugriffsebene** auf **Privat (kein anonymer Zugriff)** fest.
5. Öffnen Sie den neuen Container, und gehen Sie auf **Einstellungen** \> **Zugriffsrichtlinie**.
6. Wählen Sie **Richtlinie hinzufügen** aus, um eine gespeicherte Zugriffsrichtlinie hinzuzufügen.
7. Legen Sie das Feld **Bezeichner** entsprechend fest.
8. Wählen Sie im Feld **Berechtigungen** alle Berechtigungen aus.

    ![Alle Berechtigungen, die im Feld Berechtigungen im Dialogfeld Richtlinie hinzufügen ausgewählt wurden.](media/e-invoicing-azure-1.png)

9. Geben Sie das Start- und das Enddatum ein. Das Enddatum sollte in der Zukunft liegen.
10. Wählen Sie **OK** aus, um die Richtlinie zu speichern. Anschließend speichern Sie Ihre Änderungen im Container.
11. Gehen Sie zu **Einstellungen** \> **Gemeinsame Zugriffstoken** und legen Sie die Feldwerte fest.
12. Geben Sie das Start- und das Enddatum ein. Das Enddatum sollte in der Zukunft liegen.
13. Wählen Sie im Feld **Berechtigungen** die folgenden Berechtigungen aus:

    - Lesen
    - Einfügen
    - Erstellen
    - Schreiben
    - Löschen
    - Liste

14. Wählen Sie **SAS-Token und URL erzeugen** aus.
15. Kopieren und speichern Sie den Wert im Feld **Blob-SAS-URL**. Dieser Wert wird später in diesem Verfahren verwendet und als *Gemeinsame Zugriffssignatur URI* bezeichnet.
16. Öffnen Sie den Schlüsseltresor, den Sie mit der elektronischen Rechnungsstellung verwenden möchten.
17. Gehen Sie zu **Einstellungen** \> **Geheimnisse**, und wählen Sie **Erzeugen/Importieren**, um ein Geheimnis zu erstellen.
18. Wählen Sie auf der Seite **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.
19. Geben Sie den Namen für das Geheimnis ein. Dieser Name wird bei der Einrichtung des Dienstes im Regulatory Configuration Service (RCS) verwendet und als *Schlüsseltresor-Geheimname* bezeichnet. Weitere Informationen darüber, wie Sie RCS festlegen, finden Sie unter [Regulatory Configuration Service (RCS) einrichten](e-invoicing-set-up-rcs.md).
20. Geben Sie in das Feld **Wert** die URI der gemeinsamen Zugriffssignatur ein, die Sie zuvor kopiert haben.
21. Wählen Sie **Erstellen** aus.
