---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 2e5bc38e8fa98160df66cdfc29bbd249ab56b809
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931109"
---
# <span data-ttu-id="f931c-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f931c-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="f931c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f931c-102">SYNOPSIS</span></span>
<span data-ttu-id="f931c-103">Ändrar en definition för en princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="f931c-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f931c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f931c-104">SYNTAX</span></span>

### <span data-ttu-id="f931c-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f931c-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f931c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f931c-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f931c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f931c-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f931c-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f931c-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f931c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f931c-109">DESCRIPTION</span></span>
<span data-ttu-id="f931c-110">Cmdleten **set-AzureRmPolicySetDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="f931c-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f931c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f931c-111">EXAMPLES</span></span>

### <span data-ttu-id="f931c-112">Exempel 1: Uppdatera beskrivningen av en definition för princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="f931c-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f931c-113">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzureRmPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f931c-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f931c-114">Kommandot lagrar objektet i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="f931c-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="f931c-115">Det andra kommandot uppdaterar beskrivningen av den definition av princip uppsättning som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f931c-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="f931c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f931c-116">PARAMETERS</span></span>

### <span data-ttu-id="f931c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f931c-117">-ApiVersion</span></span>
<span data-ttu-id="f931c-118">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f931c-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f931c-119">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f931c-119">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f931c-120">-DefaultProfile</span></span>
<span data-ttu-id="f931c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f931c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f931c-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f931c-122">-Description</span></span>
<span data-ttu-id="f931c-123">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="f931c-123">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f931c-124">-DisplayName</span></span>
<span data-ttu-id="f931c-125">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="f931c-125">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f931c-126">-Id</span></span>
<span data-ttu-id="f931c-127">Fullständigt kvalificerat ID för principer, inklusive abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f931c-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="f931c-128">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f931c-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f931c-129">-ManagementGroupName</span></span>
<span data-ttu-id="f931c-130">Namnet på hanterings gruppen för princip uppsättnings definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f931c-130">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f931c-131">-Metadata</span></span>
<span data-ttu-id="f931c-132">Metadata för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="f931c-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="f931c-133">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="f931c-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="f931c-134">-Name</span></span>
<span data-ttu-id="f931c-135">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="f931c-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f931c-136">-Parameter</span></span>
<span data-ttu-id="f931c-137">Parameter deklarationen för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="f931c-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="f931c-138">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som en sträng.</span><span class="sxs-lookup"><span data-stu-id="f931c-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f931c-139">-PolicyDefinition</span></span>
<span data-ttu-id="f931c-140">Den här definitionen av princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="f931c-140">The policy set definition.</span></span> <span data-ttu-id="f931c-141">Det kan antingen vara en sökväg till ett fil namn som innehåller princip definitionerna, eller så är princip uppsättnings definitionen som sträng.</span><span class="sxs-lookup"><span data-stu-id="f931c-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-142">-För</span><span class="sxs-lookup"><span data-stu-id="f931c-142">-Pre</span></span>
<span data-ttu-id="f931c-143">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f931c-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f931c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f931c-144">-SubscriptionId</span></span>
<span data-ttu-id="f931c-145">Prenumerations-ID för princip uppsättnings definitionen att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="f931c-145">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931c-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f931c-146">-Confirm</span></span>
<span data-ttu-id="f931c-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f931c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f931c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f931c-148">-WhatIf</span></span>
<span data-ttu-id="f931c-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f931c-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f931c-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f931c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f931c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f931c-151">CommonParameters</span></span>
<span data-ttu-id="f931c-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f931c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f931c-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f931c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f931c-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f931c-154">INPUTS</span></span>

### <span data-ttu-id="f931c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f931c-155">System.String</span></span>

### <span data-ttu-id="f931c-156">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f931c-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f931c-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f931c-157">OUTPUTS</span></span>

### <span data-ttu-id="f931c-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f931c-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f931c-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f931c-159">NOTES</span></span>

## <span data-ttu-id="f931c-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f931c-160">RELATED LINKS</span></span>
