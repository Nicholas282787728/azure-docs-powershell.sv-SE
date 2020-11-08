---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263429"
---
# <span data-ttu-id="89d3c-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="89d3c-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="89d3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="89d3c-103">Ställer in sammanhanget för Recovery-tjänster som ska användas för efterföljande Azure Site Recovery-operationer i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="89d3c-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="89d3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89d3c-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89d3c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89d3c-105">DESCRIPTION</span></span>
<span data-ttu-id="89d3c-106">Cmdleten **set-AzRecoveryServicesAsrVaultContext** anger kontext för Azure Site Recovery-Valve för fler åtgärder.</span><span class="sxs-lookup"><span data-stu-id="89d3c-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="89d3c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89d3c-107">EXAMPLES</span></span>

### <span data-ttu-id="89d3c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89d3c-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="89d3c-109">Ställer in valv kontexten till det angivna Recovery Services-valvet för efterföljande Azure Site Recovery-åtgärder i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="89d3c-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="89d3c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89d3c-110">PARAMETERS</span></span>

### <span data-ttu-id="89d3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d3c-111">-DefaultProfile</span></span>
<span data-ttu-id="89d3c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89d3c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d3c-113">-Valv</span><span class="sxs-lookup"><span data-stu-id="89d3c-113">-Vault</span></span>
<span data-ttu-id="89d3c-114">Valv objekt för Recovery-tjänster som motsvarar Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="89d3c-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89d3c-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89d3c-115">-Confirm</span></span>
<span data-ttu-id="89d3c-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89d3c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d3c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d3c-117">-WhatIf</span></span>
<span data-ttu-id="89d3c-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89d3c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d3c-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89d3c-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d3c-120">CommonParameters</span></span>
<span data-ttu-id="89d3c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d3c-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89d3c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d3c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89d3c-123">INPUTS</span></span>

### <span data-ttu-id="89d3c-124">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="89d3c-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="89d3c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89d3c-125">OUTPUTS</span></span>

### <span data-ttu-id="89d3c-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="89d3c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="89d3c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89d3c-127">NOTES</span></span>

## <span data-ttu-id="89d3c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89d3c-128">RELATED LINKS</span></span>
