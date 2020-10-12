---
title: Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors
description: In diesem Thema wird erläutert, wie Sie ein Azure-Speicherkonto und einen Schlüsseltresor erstellen.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b8e39539f767cc2944a9a7fdda09121921c64763
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835963"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Der Add-On-Service für die elektronische Rechnungsstellung übernimmt die Zuständigkeit für die Speicherung aller Ihrer Geschäftsdaten in den Microsoft Azure-Ressourcen, die Ihrem Unternehmen gehören. Um sicherzustellen, dass der Service ordnungsgemäß funktioniert und auf alle Geschäftsdaten, die für das Add-On für die elektronische Rechnungsstellung benötigt und von ihm generiert werden, nur vom Add-On zugegriffen wird, müssen Sie zwei Azure-Hauptressourcen erstellen:

- Ein Azure-Speicherkonto (Blob-Speicher) zum Speichern elektronischer Rechnungen
- Ein Azure-Schlüsseldepot zum Speichern von Zertifikaten und des URI (Uniform Resource Identifier) des Speicherkontos

> [!NOTE]
> Eine dedizierte Schlüsseltresorressource und ein Blob-Speicher für den Kunden müssen speziell für die Verwendung mit dem Add-On für die elektronische Rechnungsstellung zugewiesen werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema abschließen können, müssen Sie sicherstellen, dass die folgenden Aufgaben abgeschlossen werden:

- Erstellen Sie eine Schlüsseltresor-Ressource in Azure. Weitere Informationen finden Sie unter [Über Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).
- Erstellen Sie ein Azure-Speicherkonto (Blob-Speicher). Weitere Informationen finden Sie unter [Verwalten des Azure-Speicherkontos](https://docs.microsoft.com/azure/storage/blobs/).

## <a name="overview"></a>Übersicht

In diesem Thema führen Sie zwei Hauptschritte aus:

- Richten Sie das Azure-Speicherkonto ein, um den URI des Speicherkontos abzurufen.
- Richten Sie den Schlüsseltresor zum Speichern des Speicherkonto-URI ein.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Einrichten des Azure-Speicherkontos, um den URI des Speicherkontos abzurufen

1. Öffnen Sie das Speicherkonto, das Sie mit dem Add-On für die elektronische Rechnungsstellung verwenden möchten.
2. Navigieren Sie zu **Blob-Dienst** \> **Container** und erstellen Sie einen neuen Container.
3. Geben Sie einen Namen für den Container ein und legen Sie das Feld **Öffentliche Zugriffsebene** auf **Privat (kein anonymer Zugriff)** fest.
4. Öffnen Sie den Container und navigieren Sie zu **Einstellungen \> Zugriffsrichtlinie**.
5. Wählen Sie **Richtlinie hinzufügen** aus, um eine gespeicherte Zugriffsrichtlinie hinzuzufügen.
6. Legen Sie die Felder **Bezeichner** und **Berechtigungen** nach Bedarf fest. Im Feld **Berechtigungen** sollten Sie alle Berechtigungen auswählen.

    ![Erteilen der Blob-Speicherberechtigung](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Geben Sie das Start- und das Ablaufdatum ein. Das Ablaufdatum sollte in der Zukunft liegen.
8. Wählen Sie **OK** aus, um die Richtlinie zu speichern. Anschließend speichern Sie Ihre Änderungen im Container.
9. Kehren Sie zum Speicherkonto zurück und öffnen Sie **Storage-Explorer (Vorschau)**.
10. Klicken Sie mit der rechten Maustaste auf den Container und wählen Sie **Shared Access Signature abrufen** aus.
11. Kopieren und speichern Sie im Dialogfeld **Shared Access Signatur** den Wert im Feld **URI**. Dieser Wert wird in der nächsten Prozedur verwendet und als *URI für die Shared Access Signature* bezeichnet.

    ![Auswählen und Kopieren des URI-Werts](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Einrichten des Schlüsseltresor zum Speichern des Speicherkonto-URI

1. Öffnen Sie den Schlüsseltresor, den Sie mit dem Add-On für die elektronische Rechnungsstellung verwenden möchten.
2. Navigieren Sie zu **Einstellungen** \> **Geheimnisse** und wählen Sie dann **Generieren/Importieren** aus, um ein neues Geheimnis zu erstellen.
3. Wählen Sie auf der Seite **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.
4. Geben Sie den Namen für das Geheimnis ein. Dieser Name wird während der Einrichtung des Service im Regulatory Configuration Service (RCS) verwendet und als *geheimer Name des Schlüsseltresors* bezeichnet.
5. Wählen Sie im Feld **Wert** die Option **URI für die Shared Access Signature** aus und wählen Sie dann **Erstellen** aus.
6. Richten Sie die Zugriffsrichtlinie ein, um dem Add-On für die elektronische Rechnungsstellung die richtige Zugriffsebene für den sicheren Zugriff auf das von Ihnen erstellte Geheimnis zu gewähren. Navigieren Sie zu **Einstellungen \> Zugriffsrichtlinie** und wählen Sie **Zugriffsrichtlinie hinzufügen** aus.
7. Legen Sie die geheimen Berechtigungen für die Vorgänge **Abrufen** und **Auflisten** fest.

    ![Gewähren des Servicezugriffs](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Legen Sie die Zertifikatsberechtigungen für die Vorgänge **Abrufen** und **Auflisten** fest.

    ![Gewähren der Zertifikatsberechtigung](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Wählen Sie im Dialogfeld **Prinzipal** den Prinzipal aus, indem Sie das **Add-On für die elektronische Rechnungsstellung** hinzufügen.
10. Wählen Sie **Hinzufügen** aus und wählen Sie dann **Änderungen am Schlüsseltresor speichern** aus.
11. Kopieren Sie auf der Seite **Übersicht** den Wert von **DNS-Name** für den Schlüsseltresor. Dieser Wert wird während der Einrichtung des Service in RCS verwendet und als *Schlüsseltresor-URI* bezeichnet.
