---
title: Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors
description: In diesem Thema wird erläutert, wie Sie ein Azure-Speicherkonto und einen Schlüsseltresor erstellen.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463856"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema abschließen können, müssen Sie sicherstellen, dass die folgenden Aufgaben abgeschlossen werden:

- Erstellen Sie eine Schlüsseltresor-Ressource in Azure. Weitere Informationen finden Sie unter [Über Azure Key Vault](/azure/key-vault/general/overview).
- Erstellen Sie ein Azure-Speicherkonto (Blob-Speicher). Weitere Informationen finden Sie unter [Verwalten des Azure-Speicherkontos](/azure/storage/blobs/).

## <a name="overview"></a>Übersicht

In diesem Thema führen Sie zwei Hauptschritte aus:

- Richten Sie das Azure-Speicherkonto ein, um den URI des Speicherkontos abzurufen.
- Richten Sie den Schlüsseltresor zum Speichern des Speicherkonto-URI ein.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Einrichten des Azure-Speicherkontos, um den URI des Speicherkontos abzurufen

1. Öffnen Sie das Speicherkonto, das Sie mit der elektronischen Rechnungsstellung verwenden möchten.
2. Gehen Sie zu **Datenspeicher** > **Container** und erstellen Sie einen neuen Container.
3. Geben Sie einen Namen für den Container ein und legen Sie das Feld **Öffentliche Zugriffsebene** auf **Privat (kein anonymer Zugriff)** fest.
4. Öffnen Sie den Container und gehen Sie zu **Einstellungen** > **Zugriffsrichtlinie**.
5. Wählen Sie **Richtlinie hinzufügen** aus, um eine gespeicherte Zugriffsrichtlinie hinzuzufügen.
6. Legen Sie die Felder **Bezeichner** und **Berechtigungen** nach Bedarf fest. Im Feld **Berechtigungen** sollten Sie alle Berechtigungen auswählen.

    ![Erteilen der Blob-Storage-Berechtigung.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Geben Sie das Start- und das Ablaufdatum ein. Das Ablaufdatum sollte in der Zukunft liegen.
8. Wählen Sie **OK** aus, um die Richtlinie zu speichern. Anschließend speichern Sie Ihre Änderungen im Container.
9. Gehen Sie zu **Einstellungen** > **Gemeinsame Zugriffstoken** und legen Sie die Feldwerte fest. 
10. Geben Sie das Start- und das Enddatum ein. Das Enddatum sollte in der Zukunft liegen.
11. Wählen Sie im Feld **Berechtigungen** die folgenden Berechtigungen aus: **Lesen**, **Hinzufügen**, **Erstellen**, **Schreiben**, **Löschen** und **Auflisten**. 
12. Wählen Sie **SAS-Token und URL erzeugen** aus.
13. Kopieren und speichern Sie den Wert im Feld **Blob-SAS-URL**. Dieser Wert wird in der nächsten Prozedur verwendet und als *URI für die Shared Access Signature* bezeichnet.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Einrichten des Schlüsseltresor zum Speichern des Speicherkonto-URI

1. Öffnen Sie den Schlüsseltresor, den Sie mit der elektronischen Rechnungsstellung verwenden möchten.
2. Navigieren Sie zu **Einstellungen** \> **Geheimnisse** und wählen Sie dann **Generieren/Importieren** aus, um ein neues Geheimnis zu erstellen.
3. Wählen Sie auf der Seite **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.
4. Geben Sie den Namen für das Geheimnis ein. Dieser Name wird während der Einrichtung des Service im Regulatory Configuration Service (RCS) verwendet und als *geheimer Name des Schlüsseltresors* bezeichnet.
5. Geben Sie im Feld **Wert** die URI für die Shared Access Signature ein, die Sie in der vorherigen Prozedur kopiert haben, und wählen Sie dann **Erstellen** aus.
6. Richten Sie die Zugriffsrichtlinie ein, um der elektronischen Rechnungsstellung die richtige Ebene für den sicheren Zugriff auf das von Ihnen erstellte Geheimnis zu gewähren. Navigieren Sie zu **Einstellungen \> Zugriffsrichtlinie** und wählen Sie **Zugriffsrichtlinie hinzufügen** aus.
7. Legen Sie die geheimen Berechtigungen für die Vorgänge **Abrufen** und **Auflisten** fest.

    ![Gewähren des Servicezugriffs.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Legen Sie die Zertifikatsberechtigungen für die Vorgänge **Abrufen** und **Auflisten** fest.

    ![Gewähren der Zertifikatsberechtigung.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. In dem **Prinzipal auswählen**-Feld wählen Sie **Nichts ausgewählt** aus.
10. Wählen Sie im Dialogfeld **Prinzipal** den Prinzipal aus, indem Sie **E-Invoicing-Dienst** hinzufügen.
11. Wählen Sie **Hinzufügen** und dann **Speichern** aus.
12. Kopieren Sie auf der Seite **Übersicht** den Wert von **DNS-Name** für den Schlüsseltresor. Dieser Wert wird während der Einrichtung des Service in RCS verwendet und als *Schlüsseltresor-URI* bezeichnet.

> [!NOTE]
> Für zusätzliche Sicherheit auf dem Speicherkonto, konfigurieren Sie den Azure Defender for Storage.
> 
> Weitere Informationen finden Sie unter [Einführung in Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
