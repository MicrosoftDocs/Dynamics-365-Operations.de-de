---
title: Client wurde getrennt
description: Dieser Artikel erklärt, was zu tun ist, wenn Kunden nicht mehr mit der Umgebung verbunden sind.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40605fd14384dbeed933057621d0160b698c938a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869864"
---
# <a name="client-disconnects"></a>Client wurde getrennt


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Umgebungsdetails** 

Dieses Problem kann in allen Umgebungen auftreten.
 
**Symptom** 

Kunden sind von der Umgebung getrennt und kennen den Grund nicht. Der Kunde erhält eine der folgenden Fehlermeldungen:

- Die Verbindung wurde getrennt Klicken Sie auf „Schließen”, um die Arbeit fortzusetzen.
- Die Netzwerkverbindung wurde anscheinend unterbrochen. Klicken Sie auf 'Wiederholen', um es erneut zu versuchen.

**Rote Markierung**

Dieses Problem tritt häufig auf, wenn Benutzer sich in der Implementierungsphase befinden, nachdem sie Informationen über Produktions- und Testumgebungen hinweg verglichen haben und dabei vergessen, dass sie sich zwischen Sitzungen hin- und herbewegen. Wenn Benutzer in dieser Phase sind, erfahren sie höchstwahrscheinlich dieses Problem.

**Abgang** 

**Browsertypen:** Google Chrome, Internet Explorer und Microsoft Edge

Microsoft Dynamics 365 Human Resources trennt die Verbindung von Benutzern, wenn verschiedene Sitzungen gleichzeitig für denselben Benutzer und denselben Browsertyp geöffnet sind. (Benutzer A zeigt beispielsweise sowohl Umgebung 1 als auch Umgebung 2 in Chrome an.) Es spielt keine Rolle, ob die Benutzer verschiedene Browserfenster oder Registerkarten öffnen. Wenn dieselben Benutzeranmeldeinformationen verwendet werden, um sich sowohl in Umgebung 1 als auch in Umgebung 2 gleichzeitig und im selben Browsertyp anzumelden, trennt Human Resources die Verbindung für eine der Sitzungen.

**Lösung**

Stellen Sie sicher, dass nur eine Umgebung gleichzeitig für einen bestimmten Browsertyp geöffnet ist. Benutzer können mehrere Sitzungen für die gleiche Umgebung öffnen (das heißt, mehrere Registerkarten im selben Browser).

Benutzer, die zwischen zwei Umgebung gleichzeitig hin- und herwechseln möchten, sollten jede Umgebung in einem anderen Browsertyp öffnen. (Beispielsweise kann Benutzer A Umgebung 1 in Chrome und Umgebung 2 in Microsoft Edge anzeigen.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
