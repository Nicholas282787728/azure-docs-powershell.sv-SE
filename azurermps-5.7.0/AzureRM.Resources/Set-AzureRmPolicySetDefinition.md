---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573288"
---
# <span data-ttu-id="0fb4a-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="0fb4a-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="0fb4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb4a-103">Ändrar en definition för en princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="0fb4a-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fb4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fb4a-104">SYNTAX</span></span>

### <span data-ttu-id="0fb4a-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="0fb4a-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb4a-106">SetById</span><span class="sxs-lookup"><span data-stu-id="0fb4a-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb4a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fb4a-107">DESCRIPTION</span></span>
<span data-ttu-id="0fb4a-108">Cmdleten **set-AzureRmPolicySetDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="0fb4a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fb4a-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb4a-110">Exempel 1: Uppdatera beskrivningen av en definition för princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="0fb4a-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="0fb4a-111">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzureRmPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="0fb4a-112">Kommandot lagrar objektet i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="0fb4a-113">Det andra kommandot uppdaterar beskrivningen av den definition av princip uppsättning som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="0fb4a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fb4a-114">PARAMETERS</span></span>

### <span data-ttu-id="0fb4a-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0fb4a-115">-ApiVersion</span></span>
<span data-ttu-id="0fb4a-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0fb4a-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb4a-118">-DefaultProfile</span></span>
<span data-ttu-id="0fb4a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0fb4a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0fb4a-120">-Description</span></span>
<span data-ttu-id="0fb4a-121">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0fb4a-122">-DisplayName</span></span>
<span data-ttu-id="0fb4a-123">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="0fb4a-124">-Id</span></span>
<span data-ttu-id="0fb4a-125">Fullständigt kvalificerat ID för principer, inklusive abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="0fb4a-126">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0fb4a-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fb4a-127">-Name</span></span>
<span data-ttu-id="0fb4a-128">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0fb4a-129">-PolicyDefinition</span></span>
<span data-ttu-id="0fb4a-130">Den här definitionen av princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-130">The policy set definition.</span></span> <span data-ttu-id="0fb4a-131">Det kan antingen vara en sökväg till ett fil namn som innehåller princip definitionerna, eller så är princip uppsättnings definitionen som sträng.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-132">-För</span><span class="sxs-lookup"><span data-stu-id="0fb4a-132">-Pre</span></span>
<span data-ttu-id="0fb4a-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb4a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fb4a-134">-Confirm</span></span>
<span data-ttu-id="0fb4a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb4a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb4a-136">-WhatIf</span></span>
<span data-ttu-id="0fb4a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fb4a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb4a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb4a-139">CommonParameters</span></span>
<span data-ttu-id="0fb4a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fb4a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb4a-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb4a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb4a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fb4a-142">INPUTS</span></span>

### <span data-ttu-id="0fb4a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0fb4a-143">System.String</span></span>

## <span data-ttu-id="0fb4a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fb4a-144">OUTPUTS</span></span>

### <span data-ttu-id="0fb4a-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0fb4a-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0fb4a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fb4a-146">NOTES</span></span>

## <span data-ttu-id="0fb4a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fb4a-147">RELATED LINKS</span></span>
