---
title: Vanliga frågor och svar
description: Vanliga frågor och svar om Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "98574041"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Vanliga frågor och svar om Azure PowerShell

## <a name="what-is-azure-powershell"></a>Vad är Azure PowerShell?

Azure PowerShell är en uppsättning cmdletar som du kan använda för att hantera Azure-resurser direkt med PowerShell. Az PowerShell-modulen blev allmänt tillgänglig i december 2018. Den är nu den rekommenderade PowerShell-modulen för att interagera med Azure. Mer information om Az PowerShell-modulen finns i [Introduktion till den nya Azure PowerShell Az-modulen](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Hur gör jag för att inaktivera varningsmeddelanden om icke-bakåtkompatibla ändringar i Azure PowerShell?

Om du inte vill att varningsmeddelanden om icke-bakåtkompatibla ändringar ska visas i Azure PowerShell måste du ange miljövariabeln `SuppressAzurePowerShellBreakingChangeWarnings` till `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
