---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261963"
---
# <span data-ttu-id="28753-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="28753-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="28753-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28753-102">SYNOPSIS</span></span>
<span data-ttu-id="28753-103">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="28753-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="28753-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28753-104">SYNTAX</span></span>

### <span data-ttu-id="28753-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="28753-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28753-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="28753-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28753-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28753-107">DESCRIPTION</span></span>
<span data-ttu-id="28753-108">Cmdleten **Update-AzRecoveryServicesAsrvCenter** uppdaterar identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="28753-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="28753-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28753-109">EXAMPLES</span></span>

### <span data-ttu-id="28753-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28753-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="28753-111">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="28753-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="28753-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28753-112">PARAMETERS</span></span>

### <span data-ttu-id="28753-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="28753-113">-Account</span></span>
<span data-ttu-id="28753-114">konto för inloggnings uppgifter för vCenter.</span><span class="sxs-lookup"><span data-stu-id="28753-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="28753-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28753-115">-DefaultProfile</span></span>
<span data-ttu-id="28753-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28753-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28753-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28753-117">-InputObject</span></span>
<span data-ttu-id="28753-118">VCenter-serverobjektet för att uppdatera identifierings information för.</span><span class="sxs-lookup"><span data-stu-id="28753-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="28753-119">-Port</span><span class="sxs-lookup"><span data-stu-id="28753-119">-Port</span></span>
<span data-ttu-id="28753-120">TCP-porten på vCenter-servern som ska användas för identifiering.</span><span class="sxs-lookup"><span data-stu-id="28753-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="28753-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28753-121">-ResourceId</span></span>
<span data-ttu-id="28753-122">Anger resourceId för vCenter.</span><span class="sxs-lookup"><span data-stu-id="28753-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="28753-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28753-123">-Confirm</span></span>
<span data-ttu-id="28753-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28753-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28753-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28753-125">-WhatIf</span></span>
<span data-ttu-id="28753-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28753-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28753-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28753-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28753-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28753-128">CommonParameters</span></span>
<span data-ttu-id="28753-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28753-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28753-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28753-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28753-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28753-131">INPUTS</span></span>

### <span data-ttu-id="28753-132">System. String</span><span class="sxs-lookup"><span data-stu-id="28753-132">System.String</span></span>

### <span data-ttu-id="28753-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="28753-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="28753-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28753-134">OUTPUTS</span></span>

### <span data-ttu-id="28753-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="28753-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28753-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28753-136">NOTES</span></span>

## <span data-ttu-id="28753-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28753-137">RELATED LINKS</span></span>
