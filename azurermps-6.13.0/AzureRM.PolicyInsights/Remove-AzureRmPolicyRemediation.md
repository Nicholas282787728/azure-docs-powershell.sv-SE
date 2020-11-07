---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755531"
---
# <span data-ttu-id="913bb-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="913bb-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="913bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="913bb-102">SYNOPSIS</span></span>
<span data-ttu-id="913bb-103">Tar bort en policy åtgärd.</span><span class="sxs-lookup"><span data-stu-id="913bb-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="913bb-104">SYNTAX</span></span>

### <span data-ttu-id="913bb-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="913bb-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913bb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="913bb-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913bb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="913bb-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913bb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="913bb-108">DESCRIPTION</span></span>
<span data-ttu-id="913bb-109">Cmdleten **Remove-AzureRmPolicyRemediation** tar bort en policy åtgärd.</span><span class="sxs-lookup"><span data-stu-id="913bb-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="913bb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="913bb-110">EXAMPLES</span></span>

### <span data-ttu-id="913bb-111">Exempel 1: ta bort en policy reparation i resurs gruppens omfattning</span><span class="sxs-lookup"><span data-stu-id="913bb-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="913bb-112">Detta kommando tar bort reparations åtgärden "remediation1" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="913bb-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="913bb-113">Exempel 2: ta bort en hanterings grupps reparation via ledning</span><span class="sxs-lookup"><span data-stu-id="913bb-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="913bb-114">Detta kommando tar bort reparationen med namnet "remediation1" från hanterings gruppen ' MG1 '.</span><span class="sxs-lookup"><span data-stu-id="913bb-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="913bb-115">Ett bekräftelse meddelande visas innan resursen tas bort.</span><span class="sxs-lookup"><span data-stu-id="913bb-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="913bb-116">Exempel 3: Avbryt och ta bort en policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="913bb-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="913bb-117">Detta kommando tar bort reparations åtgärden "remediation1" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="913bb-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="913bb-118">Om reparationen pågår avbryts den innan den raderas.</span><span class="sxs-lookup"><span data-stu-id="913bb-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="913bb-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="913bb-119">PARAMETERS</span></span>

### <span data-ttu-id="913bb-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="913bb-120">-AllowStop</span></span>
<span data-ttu-id="913bb-121">Tillåt att åtgärden avbryts om den pågår.</span><span class="sxs-lookup"><span data-stu-id="913bb-121">Allow the remediation to be canceled if it is in-progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="913bb-122">-AsJob</span></span>
<span data-ttu-id="913bb-123">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="913bb-123">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913bb-124">-DefaultProfile</span></span>
<span data-ttu-id="913bb-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="913bb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913bb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="913bb-126">-InputObject</span></span>
<span data-ttu-id="913bb-127">Reparations objekt.</span><span class="sxs-lookup"><span data-stu-id="913bb-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="913bb-128">-ManagementGroupName</span></span>
<span data-ttu-id="913bb-129">Hanterings grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="913bb-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="913bb-130">-Name</span></span>
<span data-ttu-id="913bb-131">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="913bb-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="913bb-132">-PassThru</span></span>
<span data-ttu-id="913bb-133">Returnera SANT om kommandot har slutförts.</span><span class="sxs-lookup"><span data-stu-id="913bb-133">Return True if the command completes successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913bb-134">-ResourceGroupName</span></span>
<span data-ttu-id="913bb-135">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="913bb-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="913bb-136">-ResourceId</span></span>
<span data-ttu-id="913bb-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="913bb-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-138">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="913bb-138">-Scope</span></span>
<span data-ttu-id="913bb-139">Omfattning av resursen.</span><span class="sxs-lookup"><span data-stu-id="913bb-139">Scope of the resource.</span></span>
<span data-ttu-id="913bb-140">Namn@example.com.</span><span class="sxs-lookup"><span data-stu-id="913bb-140">E.g.</span></span>
<span data-ttu-id="913bb-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="913bb-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bb-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="913bb-142">-Confirm</span></span>
<span data-ttu-id="913bb-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="913bb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913bb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913bb-144">-WhatIf</span></span>
<span data-ttu-id="913bb-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="913bb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="913bb-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="913bb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913bb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913bb-147">CommonParameters</span></span>
<span data-ttu-id="913bb-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913bb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913bb-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913bb-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913bb-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="913bb-150">INPUTS</span></span>

### <span data-ttu-id="913bb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="913bb-151">System.String</span></span>

### <span data-ttu-id="913bb-152">Microsoft. Azure. commands. PolicyInsights. Models. remedling. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="913bb-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="913bb-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="913bb-153">OUTPUTS</span></span>

### <span data-ttu-id="913bb-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="913bb-154">System.Boolean</span></span>

## <span data-ttu-id="913bb-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="913bb-155">NOTES</span></span>

## <span data-ttu-id="913bb-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="913bb-156">RELATED LINKS</span></span>
