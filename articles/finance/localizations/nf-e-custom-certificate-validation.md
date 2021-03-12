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
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990085"
---
# <a name="nf-e-custom-certificate-validation"></a>Validierung von benutzerdefinierten NF-e-Zertifikaten

[!include [banner](../includes/banner.md)]

Wenn Sie die Funktion zur Überprüfung benutzerdefinierter NF-e-Zertifikate aktivieren, ermöglicht die benutzerdefinierte Validierung eine Verbindung mit den Webdiensten. Diese Verbindung ist erforderlich, um NF-e zu senden und eine Autorisierung von SEFAZ zu erhalten.

Die Eigenschaft **Zweck der Serverauthentifizierung** aus dem Zertifikat V5 wird von der brasilianischen Stammzertifizierungsstelle ausgestellt. Diese Eigenschaft ist standardmäßig deaktiviert und muss manuell aktiviert werden. Unter bestimmten Umständen kann die automatische Zertifikataktualisierung dazu führen, dass diese Eigenschaft nicht mehr aktiviert wird. In diesem Fall ist die TLS-Verbindung betroffen und nicht mehr vertrauenswürdig. Die Möglichkeit, NF-e in Produktionsumgebungen für die Bundesstaaten Minas Gerais (MG) und Paraná (PR) auszugeben, ist ebenfalls betroffen.

Dieses Update ermöglicht eine alternative Lösung für die Zertifikatvalidierung, sodass eine sichere Kommunikation hergestellt werden kann.


