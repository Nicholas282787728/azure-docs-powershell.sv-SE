---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100899"
---
# <span data-ttu-id="285d5-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="285d5-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="285d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="285d5-102">SYNOPSIS</span></span>
<span data-ttu-id="285d5-103">Hämtar definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="285d5-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="285d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="285d5-104">SYNTAX</span></span>

### <span data-ttu-id="285d5-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="285d5-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285d5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d5-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285d5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d5-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285d5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d5-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="285d5-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d5-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285d5-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="285d5-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285d5-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="285d5-111">DESCRIPTION</span></span>
<span data-ttu-id="285d5-112">Cmdleten **Get-AzPolicySetDefinition** hämtar en samling princip uppsättnings definitioner eller en specifik definition för princip uppsättning som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="285d5-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="285d5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="285d5-113">EXAMPLES</span></span>

### <span data-ttu-id="285d5-114">Exempel 1: Hämta alla definitioner för princip uppsättningar</span><span class="sxs-lookup"><span data-stu-id="285d5-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="285d5-115">Det här kommandot får alla definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="285d5-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="285d5-116">Exempel 2: Hämta definitionen av princip uppsättning från aktuell prenumeration efter namn</span><span class="sxs-lookup"><span data-stu-id="285d5-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="285d5-117">Det här kommandot hämtar princip uppsättnings definitionen med namnet VMPolicySetDefinition från den aktuella standard prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="285d5-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="285d5-118">Exempel 3: Hämta princip uppsättnings definition från abonnemang efter namn</span><span class="sxs-lookup"><span data-stu-id="285d5-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="285d5-119">Det här kommandot hämtar princip definitionen med namnet VMPolicySetDefinition från prenumerationen med ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="285d5-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="285d5-120">Exempel 4: Hämta alla definitioner för anpassade principer uppsättning från en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="285d5-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="285d5-121">Det här kommandot får alla anpassade princip uppsättnings definitioner från hanterings gruppen med namnet Dept42.</span><span class="sxs-lookup"><span data-stu-id="285d5-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="285d5-122">Exempel 5: Hämta princip uppsättnings definitioner från en viss kategori</span><span class="sxs-lookup"><span data-stu-id="285d5-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="285d5-123">Det här kommandot får alla definitioner för princip uppsättningar i kategorin "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="285d5-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="285d5-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="285d5-124">PARAMETERS</span></span>

### <span data-ttu-id="285d5-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="285d5-125">-ApiVersion</span></span>
<span data-ttu-id="285d5-126">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="285d5-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="285d5-127">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="285d5-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="285d5-128">-Inbyggt</span><span class="sxs-lookup"><span data-stu-id="285d5-128">-Builtin</span></span>
<span data-ttu-id="285d5-129">Begränsar listan med resultat till endast inbyggda definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="285d5-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285d5-130">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="285d5-130">-Custom</span></span>
<span data-ttu-id="285d5-131">Begränsar listan med resultat till endast anpassade definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="285d5-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285d5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285d5-132">-DefaultProfile</span></span>
<span data-ttu-id="285d5-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="285d5-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="285d5-134">-ID</span><span class="sxs-lookup"><span data-stu-id="285d5-134">-Id</span></span>
<span data-ttu-id="285d5-135">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="285d5-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="285d5-136">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="285d5-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="285d5-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="285d5-137">-ManagementGroupName</span></span>
<span data-ttu-id="285d5-138">Namnet på hanterings gruppen för de princip uppsättnings definitioner som ska visas.</span><span class="sxs-lookup"><span data-stu-id="285d5-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d5-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="285d5-139">-Name</span></span>
<span data-ttu-id="285d5-140">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="285d5-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d5-141">-För</span><span class="sxs-lookup"><span data-stu-id="285d5-141">-Pre</span></span>
<span data-ttu-id="285d5-142">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="285d5-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="285d5-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="285d5-143">-SubscriptionId</span></span>
<span data-ttu-id="285d5-144">Prenumerations-ID för de princip uppsättnings definitioner som ska visas.</span><span class="sxs-lookup"><span data-stu-id="285d5-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285d5-145">CommonParameters</span></span>
<span data-ttu-id="285d5-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285d5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285d5-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="285d5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285d5-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="285d5-148">INPUTS</span></span>

### <span data-ttu-id="285d5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="285d5-149">System.String</span></span>

### <span data-ttu-id="285d5-150">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="285d5-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="285d5-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="285d5-151">OUTPUTS</span></span>

### <span data-ttu-id="285d5-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="285d5-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="285d5-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="285d5-153">NOTES</span></span>

## <span data-ttu-id="285d5-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="285d5-154">RELATED LINKS</span></span>