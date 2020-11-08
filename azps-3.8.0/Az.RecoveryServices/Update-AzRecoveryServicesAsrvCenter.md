---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091237"
---
# <span data-ttu-id="1d91c-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="1d91c-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="1d91c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d91c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d91c-103">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="1d91c-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="1d91c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d91c-104">SYNTAX</span></span>

### <span data-ttu-id="1d91c-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="1d91c-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d91c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d91c-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d91c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d91c-107">DESCRIPTION</span></span>
<span data-ttu-id="1d91c-108">Cmdleten **Update-AzRecoveryServicesAsrvCenter** uppdaterar identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="1d91c-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="1d91c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d91c-109">EXAMPLES</span></span>

### <span data-ttu-id="1d91c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d91c-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="1d91c-111">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="1d91c-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="1d91c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d91c-112">PARAMETERS</span></span>

### <span data-ttu-id="1d91c-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="1d91c-113">-Account</span></span>
<span data-ttu-id="1d91c-114">konto för inloggnings uppgifter för vCenter.</span><span class="sxs-lookup"><span data-stu-id="1d91c-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d91c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d91c-115">-DefaultProfile</span></span>
<span data-ttu-id="1d91c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d91c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d91c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d91c-117">-InputObject</span></span>
<span data-ttu-id="1d91c-118">VCenter-serverobjektet för att uppdatera identifierings information för.</span><span class="sxs-lookup"><span data-stu-id="1d91c-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91c-119">-Port</span><span class="sxs-lookup"><span data-stu-id="1d91c-119">-Port</span></span>
<span data-ttu-id="1d91c-120">TCP-porten på vCenter-servern som ska användas för identifiering.</span><span class="sxs-lookup"><span data-stu-id="1d91c-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d91c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d91c-121">-ResourceId</span></span>
<span data-ttu-id="1d91c-122">Anger resourceId för vCenter.</span><span class="sxs-lookup"><span data-stu-id="1d91c-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="1d91c-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d91c-123">-Confirm</span></span>
<span data-ttu-id="1d91c-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d91c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d91c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d91c-125">-WhatIf</span></span>
<span data-ttu-id="1d91c-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d91c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d91c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d91c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d91c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d91c-128">CommonParameters</span></span>
<span data-ttu-id="1d91c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d91c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d91c-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d91c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d91c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d91c-131">INPUTS</span></span>

### <span data-ttu-id="1d91c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1d91c-132">System.String</span></span>

### <span data-ttu-id="1d91c-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="1d91c-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="1d91c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d91c-134">OUTPUTS</span></span>

### <span data-ttu-id="1d91c-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1d91c-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1d91c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d91c-136">NOTES</span></span>

## <span data-ttu-id="1d91c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d91c-137">RELATED LINKS</span></span>
