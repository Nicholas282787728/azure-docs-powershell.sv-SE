---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577508"
---
# <span data-ttu-id="46b1c-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="46b1c-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="46b1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="46b1c-103">Ändrar en definition för en princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="46b1c-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46b1c-104">SYNTAX</span></span>

### <span data-ttu-id="46b1c-105">Parameter uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="46b1c-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="46b1c-106">Vis</span><span class="sxs-lookup"><span data-stu-id="46b1c-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b1c-107">Parametern uppsättning med Definitions-ID för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="46b1c-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b1c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46b1c-108">DESCRIPTION</span></span>
<span data-ttu-id="46b1c-109">Cmdleten **set-AzureRmPolicySetDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="46b1c-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="46b1c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46b1c-110">EXAMPLES</span></span>

### <span data-ttu-id="46b1c-111">Exempel 1: Uppdatera beskrivningen av en definition för princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="46b1c-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="46b1c-112">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzureRmPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46b1c-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="46b1c-113">Kommandot lagrar objektet i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="46b1c-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="46b1c-114">Det andra kommandot uppdaterar beskrivningen av den definition av princip uppsättning som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="46b1c-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="46b1c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46b1c-115">PARAMETERS</span></span>

### <span data-ttu-id="46b1c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="46b1c-116">-ApiVersion</span></span>
<span data-ttu-id="46b1c-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="46b1c-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="46b1c-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="46b1c-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="46b1c-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="46b1c-119">-Description</span></span>
<span data-ttu-id="46b1c-120">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="46b1c-120">The description for policy set definition.</span></span>

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

### <span data-ttu-id="46b1c-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="46b1c-121">-DisplayName</span></span>
<span data-ttu-id="46b1c-122">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="46b1c-122">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="46b1c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="46b1c-123">-Id</span></span>
<span data-ttu-id="46b1c-124">Fullständigt kvalificerat ID för principer, inklusive abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="46b1c-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="46b1c-125">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="46b1c-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b1c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="46b1c-126">-Name</span></span>
<span data-ttu-id="46b1c-127">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="46b1c-127">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b1c-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46b1c-128">-PolicyDefinition</span></span>
<span data-ttu-id="46b1c-129">Den här definitionen av princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="46b1c-129">The policy set definition.</span></span> <span data-ttu-id="46b1c-130">Det kan antingen vara en sökväg till ett fil namn som innehåller princip definitionerna, eller så är princip uppsättnings definitionen som sträng.</span><span class="sxs-lookup"><span data-stu-id="46b1c-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="46b1c-131">-För</span><span class="sxs-lookup"><span data-stu-id="46b1c-131">-Pre</span></span>
<span data-ttu-id="46b1c-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="46b1c-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="46b1c-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46b1c-133">-Confirm</span></span>
<span data-ttu-id="46b1c-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46b1c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b1c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b1c-135">-DefaultProfile</span></span>
<span data-ttu-id="46b1c-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46b1c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46b1c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b1c-137">-WhatIf</span></span>
<span data-ttu-id="46b1c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46b1c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46b1c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46b1c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b1c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b1c-140">CommonParameters</span></span>
<span data-ttu-id="46b1c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b1c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b1c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b1c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b1c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46b1c-143">INPUTS</span></span>

### <span data-ttu-id="46b1c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="46b1c-144">System.String</span></span>

## <span data-ttu-id="46b1c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46b1c-145">OUTPUTS</span></span>

### <span data-ttu-id="46b1c-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="46b1c-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="46b1c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46b1c-147">NOTES</span></span>

## <span data-ttu-id="46b1c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46b1c-148">RELATED LINKS</span></span>

