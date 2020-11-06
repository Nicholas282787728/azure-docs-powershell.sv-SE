---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9fcae03dba32aff18d2863c557c5827cf3e9d95e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575102"
---
# <span data-ttu-id="8f393-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8f393-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="8f393-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f393-102">SYNOPSIS</span></span>
<span data-ttu-id="8f393-103">Tar bort en uppsättning definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="8f393-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f393-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f393-104">SYNTAX</span></span>

### <span data-ttu-id="8f393-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8f393-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f393-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f393-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f393-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f393-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f393-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f393-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f393-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f393-109">DESCRIPTION</span></span>
<span data-ttu-id="8f393-110">Cmdleten **Remove-AzureRmPolicySetDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="8f393-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="8f393-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f393-111">EXAMPLES</span></span>

### <span data-ttu-id="8f393-112">Exempel 1: ta bort princip uppsättnings definition efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="8f393-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="8f393-113">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzureRmPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f393-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="8f393-114">Kommandot sparar det i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="8f393-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="8f393-115">Det andra kommandot tar bort princip uppsättnings definitionen som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="8f393-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="8f393-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f393-116">PARAMETERS</span></span>

### <span data-ttu-id="8f393-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f393-117">-ApiVersion</span></span>
<span data-ttu-id="8f393-118">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8f393-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f393-119">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="8f393-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8f393-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f393-120">-DefaultProfile</span></span>
<span data-ttu-id="8f393-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8f393-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f393-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8f393-122">-Force</span></span>
<span data-ttu-id="8f393-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8f393-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8f393-124">-ID</span><span class="sxs-lookup"><span data-stu-id="8f393-124">-Id</span></span>
<span data-ttu-id="8f393-125">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8f393-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="8f393-126">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8f393-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="8f393-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8f393-127">-ManagementGroupName</span></span>
<span data-ttu-id="8f393-128">Namnet på hanterings gruppen för princip uppsättnings definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8f393-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="8f393-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f393-129">-Name</span></span>
<span data-ttu-id="8f393-130">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="8f393-130">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f393-131">-För</span><span class="sxs-lookup"><span data-stu-id="8f393-131">-Pre</span></span>
<span data-ttu-id="8f393-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8f393-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8f393-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f393-133">-SubscriptionId</span></span>
<span data-ttu-id="8f393-134">Abonnemangs-ID för princip uppsättnings definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8f393-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="8f393-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f393-135">-Confirm</span></span>
<span data-ttu-id="8f393-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f393-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f393-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f393-137">-WhatIf</span></span>
<span data-ttu-id="8f393-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f393-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f393-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f393-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f393-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f393-140">CommonParameters</span></span>
<span data-ttu-id="8f393-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f393-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f393-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f393-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f393-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f393-143">INPUTS</span></span>

### <span data-ttu-id="8f393-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8f393-144">System.String</span></span>

### <span data-ttu-id="8f393-145">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8f393-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8f393-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f393-146">OUTPUTS</span></span>

### <span data-ttu-id="8f393-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f393-147">System.Boolean</span></span>

## <span data-ttu-id="8f393-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f393-148">NOTES</span></span>

## <span data-ttu-id="8f393-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f393-149">RELATED LINKS</span></span>
