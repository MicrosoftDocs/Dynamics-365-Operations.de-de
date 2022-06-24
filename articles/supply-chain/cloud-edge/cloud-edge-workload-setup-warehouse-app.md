---
title: Konfigurieren Sie die Warehouse Management Mobile-App für Scale-Units in der Cloud und am Rand
description: Dieser Artikel erklärt, wie Sie Ihre Warehouse Management Mobile-App für Lager festlegen, die von einer Cloud- oder Edge-Scale-Unit bedient werden.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865237"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurieren Sie die Warehouse Management Mobile-App für Scale-Units in der Cloud und am Rand

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie Sie Ihre Warehouse Management Mobile-App so festlegen, dass sie in Lagern verwendet werden können, die von einer Cloud- oder Edge-Scale-Unit bedient werden.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie Ihre mobilen Geräte für die Verbindung mit einer Cloud- oder Edge-Scale-Einheit festlegen, sollten Sie sich vergewissern, dass sie sich mit dem Enterprise Hub verbinden können. Anleitungen finden Sie unter [Installieren und Verbinden der Warehouse Management Mobile-App](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Zusätzliche Einrichtung, wenn Sie die Warehouse Management Mobile-App gegen eine Scale-Unit ausführen

Als Teil des [Bereitstellungsprozesses für die Workloads der Lager-Scale-Unit](cloud-edge-landing-page.md#scale-unit-manager-portal) werden die meisten Daten, die für die Verbindung Ihrer mobile Warehouse Management Apps erforderlich sind, automatisch vom Enterprise Hub mit der Scale-Unit synchronisiert. Sie müssen die Daten jedoch auf der Seite **Azure Active Directory Anwendungen** (**Systemadministration \> Einrichtung \> Azure Active Directory Anwendungen**) bei der Bereitstellung der Scale-Unit eingeben. Zusätzlich müssen Sie eventuell den Standardwert **Firma** für die Benutzer-ID aktualisieren oder einen neuen Benutzer erstellen. Benutzer, die mit einer Firma verbunden sind, die in einer bereitgestellten Scale-Unit nicht existiert, können sich nicht anmelden, wenn die Mobile-App von Warehouse Management mit dieser Scale-Unit verbunden ist.

> [!NOTE]
> Da die Daten auf der Seite **Azure Active Directory Anwendungen** nicht synchronisiert werden, müssen Sie diese Daten manuell pflegen, wenn Sie Ihre Lager-Workloads in eine andere Scale-Unit verschieben möchten.

Denken Sie daran, dass im Rahmen der Einrichtung der Verbindung jeder Warehouse Management Mobile-App die angegebene Azure Active Directory-Ressourcen-URL für die Scale-Unit und nicht für den Enterprise Hub sein muss.
