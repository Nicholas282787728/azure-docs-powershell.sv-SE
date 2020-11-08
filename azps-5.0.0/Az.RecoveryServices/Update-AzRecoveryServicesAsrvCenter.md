---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272398"
---
# <span data-ttu-id="e1b26-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="e1b26-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="e1b26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1b26-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b26-103">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="e1b26-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="e1b26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1b26-104">SYNTAX</span></span>

### <span data-ttu-id="e1b26-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="e1b26-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b26-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1b26-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1b26-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1b26-107">DESCRIPTION</span></span>
<span data-ttu-id="e1b26-108">Cmdleten **Update-AzRecoveryServicesAsrvCenter** uppdaterar identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="e1b26-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="e1b26-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1b26-109">EXAMPLES</span></span>

### <span data-ttu-id="e1b26-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1b26-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="e1b26-111">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="e1b26-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="e1b26-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1b26-112">PARAMETERS</span></span>

### <span data-ttu-id="e1b26-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="e1b26-113">-Account</span></span>
<span data-ttu-id="e1b26-114">konto för inloggnings uppgifter för vCenter.</span><span class="sxs-lookup"><span data-stu-id="e1b26-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="e1b26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b26-115">-DefaultProfile</span></span>
<span data-ttu-id="e1b26-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b26-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1b26-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1b26-117">-InputObject</span></span>
<span data-ttu-id="e1b26-118">VCenter-serverobjektet för att uppdatera identifierings information för.</span><span class="sxs-lookup"><span data-stu-id="e1b26-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="e1b26-119">-Port</span><span class="sxs-lookup"><span data-stu-id="e1b26-119">-Port</span></span>
<span data-ttu-id="e1b26-120">TCP-porten på vCenter-servern som ska användas för identifiering.</span><span class="sxs-lookup"><span data-stu-id="e1b26-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="e1b26-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1b26-121">-ResourceId</span></span>
<span data-ttu-id="e1b26-122">Anger resourceId för vCenter.</span><span class="sxs-lookup"><span data-stu-id="e1b26-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="e1b26-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1b26-123">-Confirm</span></span>
<span data-ttu-id="e1b26-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1b26-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b26-125">-WhatIf</span></span>
<span data-ttu-id="e1b26-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1b26-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1b26-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1b26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b26-128">CommonParameters</span></span>
<span data-ttu-id="e1b26-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b26-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1b26-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b26-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1b26-131">INPUTS</span></span>

### <span data-ttu-id="e1b26-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e1b26-132">System.String</span></span>

### <span data-ttu-id="e1b26-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="e1b26-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="e1b26-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1b26-134">OUTPUTS</span></span>

### <span data-ttu-id="e1b26-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e1b26-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e1b26-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1b26-136">NOTES</span></span>

## <span data-ttu-id="e1b26-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1b26-137">RELATED LINKS</span></span>
