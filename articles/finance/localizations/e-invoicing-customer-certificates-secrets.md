---
title: Kundenzertifikate und Geheimnisse
description: In diesem Artikel wird erklärt, wie Sie in der Elektronischen Rechnungsstellung Kundenzertifikate und Geheimnisse festlegen.
author: gionoder
ms.date: 02/07/2022
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
ms.openlocfilehash: 3943e7cb43cc6bf93995f0b3957766227cc3ec99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279839"
---
# <a name="customer-certificates-and-secrets"></a>Kundenzertifikate und Geheimnisse

[!include [banner](../includes/banner.md)]

Wenn Sie bereits eine Microsoft Azure Key Vault-Referenz im Regulatory Configuration Service (RCS) haben, können Sie Referenzen auf die Key Vault-Zertifikate und Geheimnisse erstellen. Wenn Sie noch keine Key Vault-Referenz haben, finden Sie unter [Serviceumgebungen](e-invoicing-service-environments.md) Informationen darüber, wie Sie eine solche erstellen können.

## <a name="create-certificates-and-secrets"></a>Erstellen Sie Zertifikate und Geheimnisse

Um Zertifikate und Geheimnisse zu erstellen und festzulegen, folgen Sie diesen Schritten.

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Einrichtung der Umgebung** im Aktionsbereich **Dienstumgebungen**.
4. Wählen Sie auf der Seite **Dienstumgebungen** im Aktionsbereich **Key Vault Parameter**.
5. Wählen Sie auf der Seite **Schlüsseltresor-Parameter** eine Key Vault-Referenz und dann im Abschnitt **Zertifikate** die Option **Hinzufügen**.
6. Geben Sie in das Feld **Name** den Namen des Key Vault Zertifikats oder des Geheimnisses ein. Weitere Informationen finden Sie unter [Erstellen eines Azure-Speicherkontos im Azure-Portal](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
8. Wählen Sie im Feld **Typ** **Zertifikat**, wenn Sie auf das Zertifikat verweisen, das im Key Vault gespeichert ist. Wählen Sie **Geheimnis**, wenn Sie sich auf das Geheimnis beziehen, das im Key Vault gespeichert ist.
9. Wählen Sie **Speichern** aus.

> [!NOTE]
> In einigen Szenarien müssen Sie öffentliche Zertifikate verwenden, die die Dateinamenerweiterung .cer haben. Key Vault unterstützt jedoch nicht den Import und die Speicherung von Zertifikaten dieses Typs als Key Vault Zertifikate. In diesen Szenarien sollten Sie die .cer-Datei als Base-64-kodierten X.509 (.CER) String speichern. Speichern Sie dann in einem Key Vault-Geheimnis die Zeichenfolge, die zwischen der Zeile **BEGIN CERTIFICATE** und der Zeile **END CERTIFICATE** in der Datei steht. In der Umgebung des Dienstes sollten Sie dennoch einen Verweis auf den Datensatz Key Vault erstellen und das Feld **Typ** auf **Zertifikat** festlegen.

## <a name="create-a-chain-of-certificates"></a>Erzeugen Sie eine Kette von Zertifikaten

Wenn Ihre länder-/regionenspezifischen Rechnungen eine Kette von Zertifikaten erfordern, um digitale Signaturen anzuwenden oder eine sichere (Secure Sockets Layer \[SSL\]) Verbindung zu externen Webdiensten herzustellen, erstellen Sie eine Kette von Zertifikaten, bei der die Zertifikate in der folgenden Reihenfolge angeordnet sind:

1. Root-Zertifikate
2. Zwischengeschaltete Zertifikate
3. Zertifikate für Endbenutzer

Root-Zertifizierungsstellen (CAs) sind eine vertrauenswürdige Quelle für Zertifikate. CA-Zwischenzertifikate sind Brücken, die die Zertifikate der Endbenutzer mit den Zertifikaten der Stammzertifizierungsstellen verbinden.

Um eine Kette von Zertifikaten zu erstellen und festzulegen, folgen Sie diesen Schritten.

1. Auf der Seite **Key Vault Parameter** wählen Sie im Aktionsbereich die Option **Kette der Zertifikate**.
2. Wählen Sie **Neu** aus, um eine Zertifikatskette zu erstellen.
3. Geben Sie in das Feld **Name** den Namen der Kette von Zertifikaten ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie im Abschnitt **Zertifikate** die Option **Hinzufügen** aus, um der Kette ein Zertifikat hinzuzufügen.
6. Verwenden Sie die Schaltflächen **Oben**- oder **Unten**-Schaltfläche, um die Position des Zertifikats in der Kette zu ändern. Behalten Sie das CA-Root-Zertifikat am Anfang der Liste und das Zertifikat für den Endbenutzer am Ende.
7. Wählen Sie **Speichern** aus.

Sie können so viele Key Vault-Referenzen in RCS erstellen, wie Sie möchten. Denken Sie daran, dass das Geheimnis für die Storage Shared Access Signature (SAS) Token verwendet wird, um eine bestimmte Umgebung mit der Key Vault Referenz zu verknüpfen. Sie können auf die Key Vault Zertifikate und Geheimnisse verweisen, die in einem Key Vault gespeichert sind, der auch das Geheimnis für den Storage SAS Token enthält, den Sie bei der Einrichtung der Service Umgebung verwenden.
