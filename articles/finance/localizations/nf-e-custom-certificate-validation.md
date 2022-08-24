---
title: Validierung von benutzerdefinierten NF-e-Zertifikaten
description: Dieser Artikel enthält Informationen zum Aktivieren und Verwenden des benutzerdefinierten NF-e-Zertifikats.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288543"
---
# <a name="nf-e-custom-certificate-validation"></a>Validierung von benutzerdefinierten NF-e-Zertifikaten

[!include [banner](../includes/banner.md)]

Die Eigenschaft **Zweck der Serverauthentifizierung** aus den von der brasilianischen Stammzertifizierungsstelle ausgestellten Zertifikaten ist standardmäßig deaktiviert und muss manuell aktiviert werden. Unter bestimmten Umständen kann die automatische Zertifikataktualisierung dazu führen, dass diese Eigenschaft nicht mehr aktiviert wird. In diesem Fall ist die TLS-Verbindung betroffen und ihr kann nicht mehr vertraut werden. Die Möglichkeit, das brasilianische elektronische Steuerdokument vom Modell 55 (NF-e) in Produktionsumgebungen für die Bundesstaaten Minas Gerais (MG) und Paraná (PR) auszugeben, ist ebenfalls betroffen.

Um die Fehlerbehebung für **Überprüfung von benutzerdefinierten NF-e-Zertifikaten** zu aktivieren, gehen Sie zu **Funktionsverwaltung**. Diese Funktion ermöglicht eine alternative Lösung für die Überprüfung der V5- und V10-Zertifikate und ermöglicht eine vertrauenswürdige Verbindung mit den Webdiensten, die für die sichere Übertragung der NF-e und den Erhalt der Autorisierung von SEFAZ erforderlich ist.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
