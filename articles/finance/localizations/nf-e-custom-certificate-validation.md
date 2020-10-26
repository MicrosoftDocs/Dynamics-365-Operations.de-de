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
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973091"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="a1f81-103">Validierung von benutzerdefinierten NF-e-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="a1f81-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1f81-104">Wenn Sie die Funktion zur Überprüfung benutzerdefinierter NF-e-Zertifikate aktivieren, ermöglicht die benutzerdefinierte Validierung eine Verbindung mit den Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="a1f81-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="a1f81-105">Diese Verbindung ist erforderlich, um NF-e zu senden und eine Autorisierung von SEFAZ zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a1f81-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="a1f81-106">Die Eigenschaft **Zweck der Serverauthentifizierung** aus dem Zertifikat V5 wird von der brasilianischen Stammzertifizierungsstelle ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="a1f81-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="a1f81-107">Diese Eigenschaft ist standardmäßig deaktiviert und muss manuell aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a1f81-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="a1f81-108">Unter bestimmten Umständen kann die automatische Zertifikataktualisierung dazu führen, dass diese Eigenschaft nicht mehr aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="a1f81-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="a1f81-109">In diesem Fall ist die TLS-Verbindung betroffen und nicht mehr vertrauenswürdig.</span><span class="sxs-lookup"><span data-stu-id="a1f81-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="a1f81-110">Die Möglichkeit, NF-e in Produktionsumgebungen für die Bundesstaaten Minas Gerais (MG) und Paraná (PR) auszugeben, ist ebenfalls betroffen.</span><span class="sxs-lookup"><span data-stu-id="a1f81-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="a1f81-111">Dieses Update ermöglicht eine alternative Lösung für die Zertifikatvalidierung, sodass eine sichere Kommunikation hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1f81-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


