---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2630b438fa9c5aaa691422be2da2d32e08112fba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747548"
---
# <span data-ttu-id="3614f-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="3614f-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="3614f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3614f-102">SYNOPSIS</span></span>
<span data-ttu-id="3614f-103">Avbryter en pågående princip korrigering.</span><span class="sxs-lookup"><span data-stu-id="3614f-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="3614f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3614f-104">SYNTAX</span></span>

### <span data-ttu-id="3614f-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="3614f-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3614f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3614f-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3614f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3614f-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3614f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3614f-108">DESCRIPTION</span></span>
<span data-ttu-id="3614f-109">Cmdleten **Stop-AzPolicyRemediation** avbryter en pågående princip korrigering.</span><span class="sxs-lookup"><span data-stu-id="3614f-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="3614f-110">Aktiva distributioner avbryts och inga nya distributioner skapas.</span><span class="sxs-lookup"><span data-stu-id="3614f-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="3614f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3614f-111">EXAMPLES</span></span>

### <span data-ttu-id="3614f-112">Exempel 1: Avbryt en policy åtgärd i resurs gruppens omfattning</span><span class="sxs-lookup"><span data-stu-id="3614f-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="3614f-113">Det här kommandot avbryter reparationen med namnet "remediation1" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="3614f-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="3614f-114">Exempel 2: annullera en hanterings grupps reparation via ledning</span><span class="sxs-lookup"><span data-stu-id="3614f-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="3614f-115">Det här kommandot avbryter reparationen med namnet "remediation1" i hanterings gruppen ' MG1 '.</span><span class="sxs-lookup"><span data-stu-id="3614f-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="3614f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3614f-116">PARAMETERS</span></span>

### <span data-ttu-id="3614f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3614f-117">-AsJob</span></span>
<span data-ttu-id="3614f-118">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="3614f-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3614f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3614f-119">-DefaultProfile</span></span>
<span data-ttu-id="3614f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3614f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3614f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3614f-121">-InputObject</span></span>
<span data-ttu-id="3614f-122">Reparations objekt.</span><span class="sxs-lookup"><span data-stu-id="3614f-122">The Remediation object.</span></span>

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

### <span data-ttu-id="3614f-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3614f-123">-ManagementGroupName</span></span>
<span data-ttu-id="3614f-124">Hanterings grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="3614f-124">Management group ID.</span></span>

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

### <span data-ttu-id="3614f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3614f-125">-Name</span></span>
<span data-ttu-id="3614f-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="3614f-126">Resource name.</span></span>

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

### <span data-ttu-id="3614f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3614f-127">-PassThru</span></span>
<span data-ttu-id="3614f-128">Returnera SANT om kommandot har slutförts.</span><span class="sxs-lookup"><span data-stu-id="3614f-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="3614f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3614f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3614f-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3614f-130">Resource group name.</span></span>

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

### <span data-ttu-id="3614f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3614f-131">-ResourceId</span></span>
<span data-ttu-id="3614f-132">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3614f-132">Resource ID.</span></span>

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

### <span data-ttu-id="3614f-133">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="3614f-133">-Scope</span></span>
<span data-ttu-id="3614f-134">Omfattning av resursen.</span><span class="sxs-lookup"><span data-stu-id="3614f-134">Scope of the resource.</span></span>
<span data-ttu-id="3614f-135">Namn@example.com.</span><span class="sxs-lookup"><span data-stu-id="3614f-135">E.g.</span></span>
<span data-ttu-id="3614f-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="3614f-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="3614f-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3614f-137">-Confirm</span></span>
<span data-ttu-id="3614f-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3614f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3614f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3614f-139">-WhatIf</span></span>
<span data-ttu-id="3614f-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3614f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3614f-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3614f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3614f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3614f-142">CommonParameters</span></span>
<span data-ttu-id="3614f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3614f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3614f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3614f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3614f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3614f-145">INPUTS</span></span>

### <span data-ttu-id="3614f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3614f-146">System.String</span></span>

### <span data-ttu-id="3614f-147">Microsoft. Azure. commands. PolicyInsights. Models. remedling. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="3614f-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="3614f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3614f-148">OUTPUTS</span></span>

### <span data-ttu-id="3614f-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3614f-149">System.Boolean</span></span>

## <span data-ttu-id="3614f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3614f-150">NOTES</span></span>

## <span data-ttu-id="3614f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3614f-151">RELATED LINKS</span></span>
