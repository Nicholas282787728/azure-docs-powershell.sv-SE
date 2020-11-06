---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575887"
---
# <span data-ttu-id="0fcbf-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="0fcbf-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="0fcbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fcbf-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcbf-103">Ställer in sammanhanget för Recovery-tjänster som ska användas för efterföljande Azure Site Recovery-operationer i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fcbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fcbf-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fcbf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fcbf-105">DESCRIPTION</span></span>
<span data-ttu-id="0fcbf-106">Cmdleten **set-AzureRmRecoveryServicesAsrVaultContext** anger kontext för Azure Site Recovery-Valve för fler åtgärder.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="0fcbf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fcbf-107">EXAMPLES</span></span>

### <span data-ttu-id="0fcbf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fcbf-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="0fcbf-109">Ställer in valv kontexten till det angivna Recovery Services-valvet för efterföljande Azure Site Recovery-åtgärder i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="0fcbf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fcbf-110">PARAMETERS</span></span>

### <span data-ttu-id="0fcbf-111">-Valv</span><span class="sxs-lookup"><span data-stu-id="0fcbf-111">-Vault</span></span>
<span data-ttu-id="0fcbf-112">Valv objekt för Recovery-tjänster som motsvarar Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fcbf-113">-Confirm</span></span>
<span data-ttu-id="0fcbf-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fcbf-115">-WhatIf</span></span>
<span data-ttu-id="0fcbf-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fcbf-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcbf-118">CommonParameters</span></span>
<span data-ttu-id="0fcbf-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcbf-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fcbf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcbf-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fcbf-121">INPUTS</span></span>

### <span data-ttu-id="0fcbf-122">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="0fcbf-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0fcbf-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fcbf-123">OUTPUTS</span></span>

### <span data-ttu-id="0fcbf-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0fcbf-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0fcbf-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fcbf-125">NOTES</span></span>

## <span data-ttu-id="0fcbf-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fcbf-126">RELATED LINKS</span></span>

