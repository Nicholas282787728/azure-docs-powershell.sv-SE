---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819719"
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

## <a name="version-129"></a>Version 1.2.9

Ändringar i den här versionen

* Modulen AzureRm.AzureStackAdmin
    + Ändringar i cmdleten Add-AzureRmResourceProviderRegistration för stöd av delning av admin och klient för Azure Resource Manager. En ny parameter, -ResourceManagerType, har lagts till.
    + Parametrarna -AdminUri, -ApiVersion, -SubscriptionId och -Token har tagits bort från varje cmdlet. Vi har förvarnat om att dessa parametrar kommer att bli inaktuella och nu har de tagits bort.
* Modulen AzureStackStorage
    + Nya cmdletar har lagts till för behållarmigreringsscenarier.
    + Cmdletar som refererar till interna komponenter och underliggande funktioner har tagits bort.
* AzureRM.BootStrapper
    + En ny modul har skapats för att hantera versioner av Azure PowerShell-cmdletar med hjälp av versionsprofiler