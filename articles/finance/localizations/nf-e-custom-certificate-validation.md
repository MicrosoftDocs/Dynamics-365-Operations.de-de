---
title: Validierung von benutzerdefinierten NF-e-Zertifikaten
description: Dieses Thema enthält Informationen zum Aktivieren und Verwenden des benutzerdefinierten NF-e-Zertifikats.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240578"
---
# <a name="nf-e-custom-certificate-validation"></a>Validierung von benutzerdefinierten NF-e-Zertifikaten

[!include [banner](../includes/banner.md)]

Wenn Sie die Funktion zur Überprüfung benutzerdefinierter NF-e-Zertifikate aktivieren, ermöglicht die benutzerdefinierte Validierung eine Verbindung mit den Webdiensten. Diese Verbindung ist erforderlich, um NF-e zu senden und eine Autorisierung von SEFAZ zu erhalten.

Die Eigenschaft **Zweck der Serverauthentifizierung** aus dem Zertifikat V5 wird von der brasilianischen Stammzertifizierungsstelle ausgestellt. Diese Eigenschaft ist standardmäßig deaktiviert und muss manuell aktiviert werden. Unter bestimmten Umständen kann die automatische Zertifikataktualisierung dazu führen, dass diese Eigenschaft nicht mehr aktiviert wird. In diesem Fall ist die TLS-Verbindung betroffen und nicht mehr vertrauenswürdig. Die Möglichkeit, NF-e in Produktionsumgebungen für die Bundesstaaten Minas Gerais (MG) und Paraná (PR) auszugeben, ist ebenfalls betroffen.

Dieses Update ermöglicht eine alternative Lösung für die Zertifikatvalidierung, sodass eine sichere Kommunikation hergestellt werden kann.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]