---
title: Översikt över Azure Stack PowerShell | Microsoft Docs
description: Översikt över installation och konfiguration av Azure Stack PowerShell.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

Azure Stack kräver följande två PowerShell-moduler:  

1. Den Azure Stack-kompatibla **AzureRM**-modulen som blir tillgänglig genom att installera API-versionsprofilen **2017-03-09-profile**. De cmdletar som installerats med den här profilen kan användas av Azure Stack-användare och -operatörer.

2. Den senaste versionen är **1.2.11**-installationen av **AzureStack**-modulen. De cmdletar som installerats med den hör modulen kan endast användas av Azure Stack-operatörer. Administratörer kan utföra åtgärder som att hantera erbjudanden, planer, tjänster, kvoter och annat med de PowerShell-cmdletar som tillhandahålls i modulen. Mer information om PowerShell-cmdletarna i den här modulen finns i [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin)- och [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage)-referensinnehållet.

## <a name="next-steps"></a>Nästa steg

* [Installera PowerShell för Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [Konfigurera PowerShell för användning med Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
