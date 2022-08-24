---
title: Eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine einrichten
description: Dieser Artikel erläutert, wie eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine (VM) eingerichtet wird.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 64e03c742f7095e2e485f32ad534f2a755ddd062
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277878"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine einrichten

[!include [banner](../../includes/banner.md)]

Dieser Artikel erläutert, wie eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine (VM) eingerichtet wird.

## <a name="description"></a>Beschreibung

Microsoft Dynamics 365 Commerce-Ebene 1-Umgebungen werden normalerweise für Commerce Runtime (CRT) und die Entwicklung von Verkaufsstellen (POS)-Erweiterungen bereitgestellt. Sie sind eigenständige Umgebungen. Aufgrund der SaaS-Natur (Software-as-a-Service) der Architektur enthalten sie keine E-Commerce-Komponenten.

In einigen Szenarien möchten Sie möglicherweise Aufrufe von Erweiterungen in einer Ebene 1-Umgebung testen, damit Sie Erweiterungen von E-Commerce-Komponenten debuggen können. Allgemeine Anweisungen finden Sie unter [In einer Commerce-Entwicklungsumgebung der Ebene 1 debuggen](../e-commerce-extensibility/debug-tier-1.md)

Wenn Sie in einer Ebene 1-Umgebung debuggen, da die Website jetzt einen anderen Retail Server aufruft, können serverübergreifende Aufrufe verschiedene Fehler verursachen, die mit der Inhaltssicherheitsrichtlinie zusammenhängen.

Die folgende Abbildung zeigt ein Beispiel für einen Fehler, der auftreten kann, wenn eine Variante auf einer Produktdetailseite ausgewählt wird.

![Fehler beim Auswählen einer Variante auf einer Produktdetailseite.](media/unhandled-rejection-error.jpg)

Die folgende Abbildung zeigt ein Beispiel für einen ähnlichen Fehler in den Debugger-Tools eines Browsers (F12-Entwicklertools). In der Fehlermeldung wird ein Verstoß gegen die Inhaltssicherheitsrichtlinie erwähnt.

![Debugger-Tool-Fehler.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Lösung

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Inhaltssicherheitsrichtlinie für die Website im Commerce-Website-Generator deaktivieren

1. Wählen Sie die Website aus, an der Sie arbeiten.
1. Wählen Sie **Einstellungen** und anschließend **Erweiterungen** aus.
1. Wählen Sie auf der Registerkarte **Inhaltssicherheitsrichtlinie** die Option **Inhaltssicherheitsrichtlinie deaktivieren** aus.
1. Wählen Sie **Speichern und veröffentlichen** aus.

> [!NOTE]
> Die Business-to-Consumer(B2C)-Anmeldung funktioniert in einer lokalen Entwicklungsumgebung nicht. Sie können jedoch als Gast auschecken oder Pseudoseiten erstellen, um eine Benutzeranmeldung nach Bedarf zu simulieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erste Schritte mit der Entwicklung der E-Commerce-Online-Erweiterbarkeit](../e-commerce-extensibility/sdk-getting-started.md)

[Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) auf E-Commerce-Website verwalten](../manage-csp.md)
