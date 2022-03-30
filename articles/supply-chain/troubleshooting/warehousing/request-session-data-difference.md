---
title: Unerwarteter Unterschied zwischen Anforderungs- und Sitzungsdaten während des Tests
description: In den Validierungsergebnissen der Warehouse-App-Aufgabe tritt ein unerwarteter Unterschied zwischen Anforderungs- und Sitzungsdaten auf.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456938"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Unerwarteter Unterschied zwischen Anforderungs- und Sitzungsdaten während des Tests

Fehlercode: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Symptome

Wenn Sie das [Warehouse-App-Aufgabenüberprüfungs-Framework](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat) verwenden, gibt die Validierung die folgende Fehlermeldung zurück:

> Unerwarteter Unterschied zwischen Anforderungs- und Sitzungsdaten. XML-Protokoll für Warehouse Mobile Devices verletzt.REQUEST_XML_TAMPERING

## <a name="cause"></a>Ursache

Der Fehler tritt auf, wenn die Ausgabe des letzten Schritts, der im Testlauf erfolgreich ausgeführt wurde, nicht mit der aufgezeichneten Eingabe für den nächsten Schritt übereinstimmt. Diese Situation kann entstehen, weil der Aufgabenvalidierer die Ausgabe eines vorherigen Schritts nicht als Eingabe für einen nachfolgenden Schritt verwendet. Stattdessen verwendet er aufgezeichnetes XML als Eingabe für jeden Schritt.

In den meisten Fällen tritt der Fehler auf, wenn Sie eine Aufgabe erneut ausführen, aber für den Test einige Datensätze erforderlich sind, die bei einer vorherigen Ausführung derselben Aufgabe geändert oder entfernt wurden.

## <a name="resolution"></a>Lösung

Der Validierungstestlauf der Warehouse-App-Aufgabe ist kein idempotenter Vorgang, sondern ändert die zugrunde liegenden Daten. Bevor Sie eine Aufgabe erneut ausführen, müssen Sie daher möglicherweise die relevanten Daten zurücksetzen.

1. Überprüfen Sie die Ausgabe-XML des letzten erfolgreichen Testschritts, um festzustellen, wo Ihr Testlauf aufgehört hat.
1. Überprüfen Sie Ihren Test und stellen Sie sicher, dass alle erforderlichen Aufträge, Umlagerungsaufträge, Arbeitskopfzeilen und andere Datensätze noch vorhanden sind und sich im erwarteten Zustand befinden.
1. Erstellen Sie die fehlenden oder geänderten Datensätze neu oder bearbeiten Sie sie. Alternativ können Sie einen neuen Testaufbau erstellen und den Test so gestalten, dass gültige vorhandene Datensätze verwendet werden.
