---
title: Verschieben von NF-e-XML-Dateien als Anhänge
description: In diesem Artikel wird erläutert, wie Sie NF-e-XML-Dateien aus Ihrer Microsoft Microsoft Dynamics 365 Finance- oder Dynamics 365 Supply Chain Management-Datenbank verschieben und sie stattdessen als Anhänge zur Verfügung stellen.
author: gionoder
ms.date: 11/11/2021
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
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877896"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Verschieben von NF-e-XML-Dateien als Anhänge

[!include [banner](../includes/banner.md)] 


Bei der Ausstellung von elektronischen Steuerdokumenten (NF-e) werden XML-Dateien erstellt und in der Microsoft Dynamics 365 Finance- und Dynamics 365 Supply Chain Management-Datenbank gespeichert. In der brasilianischen Lokalisierung können Sie die **NF-e XML als Anhang verschieben**-Funktion verwenden, um den Datenbankspeicherplatz freizugeben, den diese XML-Dateien verbrauchen.

Für einen bestimmten Zeitraum und eine bestimmte steuerliche Einrichtung verschiebt die Funktion die NF-e-XML-Dateien aus Ihrer Finance- oder Supply Chain Management-Datenbank in den Blob-Speicher Ihres Azure-Abonnements. Diese Verschiebung macht die Dateien nur als Anhänge verfügbar. Nachdem die XML-Dateien erfolgreich in den Blob-Speicher verschoben wurden, werden die Originaldateien aus der Finance- oder Supply Chain Management-Datenbank gelöscht. Daher wird der von diesen Dateien verwendete Datenbankspeicherplatz freigegeben.

Um die **NF-e XML als Anhang verschieben**-Funktion zu aktivieren, führen Sie die folgenden Schritte aus.

1. Öffnen Sie in den Arbeitsbereich **Funktionsverwaltung** in Finance oder Supply Chain Management.
2. Auf der **Alle**-Registerkarte suchen und wählen Sie die Funktion **NF-e XML als Anhang verschieben**.
3. Wählen Sie **Jetzt aktivieren**.

Führen Sie diese Schritte aus, um NF-e-XML-Dateien als Anhänge zu verschieben.

1. Gehen Sie zu **Debitoren** \> **Steuerdokumente** \> **Elektronische Steuerdokumente** \> **NF-e-XML als Anhänge verschieben**.
2. Wählen Sie das Start- und Enddatum in den Feldern **Von Datum** und **Bis Datum** aus.
3. Wählen Sie im Feld **Kennung der steuerlichen Einrichtung** einen Wert aus.
4. Wählen Sie **OK** aus.

> [!IMPORTANT]
> Dieser Prozess ist nicht umkehrbar. Nachdem Sie die NF-e-XML-Dateien verschoben haben, können Benutzer sie nur anzeigen, indem sie **Anhänge** oben auf der Seite **Steuerdokument** auswählen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
