---
title: Azure-Ressourcen für die Elektronische Rechnungsstellung festlegen
description: Dieser Artikel gibt Ihnen einen Überblick über die Einrichtung der Microsoft Azure-Ressourcen für die Elektronische Rechnungsstellung.
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283084"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Azure-Ressourcen für die Elektronische Rechnungsstellung festlegen

[!include [banner](../includes/banner.md)]

Der Prozess zur Einrichtung von Microsoft Azure-Ressourcen für die Elektronische Rechnungsstellung besteht aus drei Schritten. Die ersten beiden Schritte, „Erstellen Sie einen Azure Key Vault im Azure-Portal“ und „Erstellen Sie ein Azure-Speicherkonto im Azure-Portal“, sind obligatorisch. Der dritte Schritt, „Konfigurieren Sie eine SharePoint Verbindung“, ist optional.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Erzeugen Sie einen Azure Key Vault im Azure-Portal

Erzeugen Sie einen Key Vault in Ihrem Azure Abonnement. Wir empfehlen Ihnen, für die Elektronische Rechnungsstellung einen eigenen Key Vault zu erstellen und Geheimnisse nicht mit anderen Anwendungen zu kombinieren. Erstellen Sie in elektronischen Belegen so viele Geheimnisse und Zertifikate, wie Sie für Ihre Szenarien benötigen. Sie müssen mindestens ein Geheimnis erstellen, um das Token für die gemeinsame Zugriffssignatur (SAS) des Azure-Speicherkontos zu speichern, das Sie im nächsten Schritt erstellen werden.

Wie Sie diesen Schritt ausführen, erfahren Sie unter [Erstellen eines Azure Key Vault im Azure-Portal](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Erstellen Sie ein Azure-Speicherkonto im Azure-Portal

Sie sind Eigentümer aller elektronischen Belege und Dateien, die durch den Dienst für die elektronische Rechnungsstellung erzeugt werden, oder Sie geben den Dienst ein. Diese Dokumente und Dateien werden in einem Azure-Speicherkonto gespeichert, das Sie im Rahmen Ihres Azure-Abonnements erstellen. Der Dienst greift auf Ihr Speicherkonto zu, indem er das SAS-Token verwendet, das Ihrem Key Vault Geheimnis entnommen wird.

Informationen darüber, wie Sie diesen Schritt ausführen, finden Sie unter [Erstellen eines Azure-Speicherkontos im Azure-Portal](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Konfigurieren Sie eine SharePoint-Verbindung

In einigen Szenarien müssen Sie möglicherweise elektronische Dateien auf SharePoint speichern und von SharePoint abrufen. Um sicherzustellen, dass der Dienst für die elektronische Rechnungsstellung auf Ihre SharePoint-Ordner zugreifen kann, konfigurieren Sie den Zugriff auf SharePoint.

Wie Sie diesen Schritt ausführen, erfahren Sie unter [Konfigurieren einer SharePoint-Verbindung](e-invoicing-create-sharepoint-connection.md).
