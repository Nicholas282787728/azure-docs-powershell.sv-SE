---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 148f7b22a9df77532f574457da453e9e4b07a846
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923821"
---
# <span data-ttu-id="c4724-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c4724-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c4724-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4724-102">SYNOPSIS</span></span>
<span data-ttu-id="c4724-103">Tar bort en uppsättning definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="c4724-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="c4724-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4724-104">SYNTAX</span></span>

### <span data-ttu-id="c4724-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4724-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4724-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4724-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4724-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4724-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4724-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4724-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4724-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4724-109">DESCRIPTION</span></span>
<span data-ttu-id="c4724-110">Cmdleten **Remove-AzPolicySetDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="c4724-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="c4724-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4724-111">EXAMPLES</span></span>

### <span data-ttu-id="c4724-112">Exempel 1: ta bort princip uppsättnings definition efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c4724-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="c4724-113">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4724-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="c4724-114">Kommandot sparar det i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="c4724-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="c4724-115">Det andra kommandot tar bort princip uppsättnings definitionen som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c4724-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="c4724-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4724-116">PARAMETERS</span></span>

### <span data-ttu-id="c4724-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c4724-117">-ApiVersion</span></span>
<span data-ttu-id="c4724-118">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c4724-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c4724-119">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="c4724-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c4724-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4724-120">-DefaultProfile</span></span>
<span data-ttu-id="c4724-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c4724-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4724-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c4724-122">-Force</span></span>
<span data-ttu-id="c4724-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c4724-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c4724-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c4724-124">-Id</span></span>
<span data-ttu-id="c4724-125">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c4724-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="c4724-126">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c4724-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="c4724-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c4724-127">-ManagementGroupName</span></span>
<span data-ttu-id="c4724-128">Namnet på hanterings gruppen för princip uppsättnings definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c4724-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="c4724-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4724-129">-Name</span></span>
<span data-ttu-id="c4724-130">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="c4724-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="c4724-131">-För</span><span class="sxs-lookup"><span data-stu-id="c4724-131">-Pre</span></span>
<span data-ttu-id="c4724-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c4724-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c4724-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4724-133">-SubscriptionId</span></span>
<span data-ttu-id="c4724-134">Abonnemangs-ID för princip uppsättnings definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c4724-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="c4724-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4724-135">-Confirm</span></span>
<span data-ttu-id="c4724-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4724-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4724-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4724-137">-WhatIf</span></span>
<span data-ttu-id="c4724-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4724-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4724-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4724-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4724-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4724-140">CommonParameters</span></span>
<span data-ttu-id="c4724-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4724-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4724-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4724-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4724-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4724-143">INPUTS</span></span>

### <span data-ttu-id="c4724-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c4724-144">System.String</span></span>

### <span data-ttu-id="c4724-145">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c4724-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c4724-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4724-146">OUTPUTS</span></span>

### <span data-ttu-id="c4724-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4724-147">System.Boolean</span></span>

## <span data-ttu-id="c4724-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4724-148">NOTES</span></span>

## <span data-ttu-id="c4724-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4724-149">RELATED LINKS</span></span>
