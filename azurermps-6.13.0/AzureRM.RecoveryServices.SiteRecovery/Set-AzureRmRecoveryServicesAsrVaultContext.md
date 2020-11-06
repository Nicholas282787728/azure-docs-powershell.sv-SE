---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573945"
---
# <span data-ttu-id="b296f-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b296f-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b296f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b296f-102">SYNOPSIS</span></span>
<span data-ttu-id="b296f-103">Ställer in sammanhanget för Recovery-tjänster som ska användas för efterföljande Azure Site Recovery-operationer i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="b296f-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b296f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b296f-104">SYNTAX</span></span>

### <span data-ttu-id="b296f-105">AzureRecoveryServicesVault (standard)</span><span class="sxs-lookup"><span data-stu-id="b296f-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b296f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b296f-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b296f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b296f-107">DESCRIPTION</span></span>
<span data-ttu-id="b296f-108">Cmdleten **set-AzureRmRecoveryServicesAsrVaultContext** anger kontext för Azure Site Recovery-Valve för fler åtgärder.</span><span class="sxs-lookup"><span data-stu-id="b296f-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="b296f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b296f-109">EXAMPLES</span></span>

### <span data-ttu-id="b296f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b296f-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="b296f-111">Ställer in valv kontexten till det angivna Recovery Services-valvet för efterföljande Azure Site Recovery-åtgärder i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="b296f-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="b296f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b296f-112">PARAMETERS</span></span>

### <span data-ttu-id="b296f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b296f-113">-DefaultProfile</span></span>
<span data-ttu-id="b296f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b296f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b296f-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b296f-115">-ResourceId</span></span>
<span data-ttu-id="b296f-116">Anger det recoveryservices valv resurs-ID som ska anges som valv kontext.</span><span class="sxs-lookup"><span data-stu-id="b296f-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b296f-117">-Valv</span><span class="sxs-lookup"><span data-stu-id="b296f-117">-Vault</span></span>
<span data-ttu-id="b296f-118">Valv objekt för Recovery-tjänster som motsvarar Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b296f-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b296f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b296f-119">-Confirm</span></span>
<span data-ttu-id="b296f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b296f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b296f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b296f-121">-WhatIf</span></span>
<span data-ttu-id="b296f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b296f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b296f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b296f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b296f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b296f-124">CommonParameters</span></span>
<span data-ttu-id="b296f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b296f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b296f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b296f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b296f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b296f-127">INPUTS</span></span>

### <span data-ttu-id="b296f-128">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b296f-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b296f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b296f-129">OUTPUTS</span></span>

### <span data-ttu-id="b296f-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b296f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b296f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b296f-131">NOTES</span></span>

## <span data-ttu-id="b296f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b296f-132">RELATED LINKS</span></span>
