---
title: Ausprobieren von Scale-Units in einer verteilten hybriden Topologie
description: In diesem Thema finden Sie Informationen darüber, wie Sie die Scale-Units in der Cloud und am Edge für Workloads in der Fertigung und in der Lagerortverwaltung ausprobieren können.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 658948d94cd012b95812a786433967f5cadc3a15
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711885"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Ausprobieren von Scale-Units in einer verteilten hybriden Topologie

[!include [banner](../includes/banner.md)]

Der Prozess des Ausprobierens der verteilten Hybridtopologie ist einfach. In der ersten Phase sollten Sie Ihre Anpassungen validieren, um sicherzustellen, dass sie in der verteilten Topologie funktionieren. Sie haben zwei Möglichkeiten.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Option 1: Evaluieren Sie angepasste Anpassungen in Entwicklungsumgebungen

Bevor Sie mit dem Onboarding Ihrer Sandbox-Umgebungen beginnen, empfehlen wir Ihnen, Scale-Units in einer Entwicklungsumgebung zu testen, z.B. in einer One-Box-Umgebung (auch als Tier-1-Umgebung bekannt), damit Sie Prozesse, Anpassungen und Lösungen validieren können. In dieser Phase werden Daten und Anpassungen auf die Umgebungen mit einem Feld angewendet. Sie können in einer einzigen Umgebung ausführen, die sowohl die Rolle des Enterprise Hub als auch die der Scale-Unit übernehmen kann. Alternativ können Sie auch zwei Entwicklungsumgebungen haben, von denen eine die Rolle des Hubs und die andere die Rolle einer Scale-Unit übernimmt. Diese Einstellung bietet die beste Möglichkeit, um Probleme zu identifizieren und zu beheben. Die letzte [Vorschauversion](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) kann auch verwendet werden, um diese Phase abzuschließen.

Sie sollten die [Scale-Unit Deployment Tools für One-Box-Entwicklungsumgebungen](https://github.com/microsoft/SCMScaleUnitDevTools) verwenden, um die Umgebungen zu installieren und zu pflegen. Mit diesen Tools können Sie Hub- und Scale-Units in einer oder zwei One-Box-Umgebungen konfigurieren. Die Tools werden sowohl als Binärversion als auch im Quellcode auf GitHub bereitgestellt. Studieren Sie das Projekt-Wiki, das eine [Schritt-für-Schritt-Anleitung](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) enthält, in der die Verwendung der Tools beschrieben wird. Wenn Sie [Edge Scale-Units auf angepasster Hardware unter Verwendung lokaler Geschäftsdaten (LBD)](cloud-edge-edge-scale-units-lbd.md) bereitstellen, müssen Sie einen anderen Prozess befolgen.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Option 2: Erwerben Sie Add-ins und stellen Sie sie in Ihren Sandbox-Umgebungen bereit

Um die verteilte Hybrid-Topologie auszuprobieren, benötigen Sie zwei Sandbox-Umgebungen (Tier 2), von denen eine Ihre Daten enthält (Enterprise Hub) und die andere für die Scale-Unit bestimmt ist und „leere Daten“ enthält.

Sie müssen Add-Ins für mindestens eine Cloud- oder Edge-Scale-Einheit erwerben. Die entsprechenden Projekt- und Umgebungsslots werden dann in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) vergeben, so dass die Umgebungen der Scale-Units über das Portal [Scale-Unit-Manager](https://aka.ms/SCMSUM) bereitgestellt werden können.

Wenden Sie sich an den Microsoft Support, um die Aktivierung der Sandbox-Umgebungen zu beantragen.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
