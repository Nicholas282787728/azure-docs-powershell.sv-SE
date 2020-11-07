---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d0a1097407c9941b5be49b19ea7ba99e75b3fce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757353"
---
# <span data-ttu-id="38803-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="38803-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="38803-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38803-102">SYNOPSIS</span></span>
<span data-ttu-id="38803-103">Hämtar definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="38803-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38803-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38803-104">SYNTAX</span></span>

### <span data-ttu-id="38803-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="38803-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38803-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38803-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38803-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38803-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38803-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38803-108">IdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38803-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="38803-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38803-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="38803-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38803-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38803-111">DESCRIPTION</span></span>
<span data-ttu-id="38803-112">Cmdleten **Get-AzureRmPolicySetDefinition** hämtar en samling princip uppsättnings definitioner eller en specifik definition för princip uppsättning som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="38803-112">The **Get-AzureRmPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="38803-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38803-113">EXAMPLES</span></span>

### <span data-ttu-id="38803-114">Exempel 1: Hämta alla definitioner för princip uppsättningar</span><span class="sxs-lookup"><span data-stu-id="38803-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="38803-115">Det här kommandot får alla definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="38803-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="38803-116">Exempel 2: Hämta definitionen av princip uppsättning från aktuell prenumeration efter namn</span><span class="sxs-lookup"><span data-stu-id="38803-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="38803-117">Det här kommandot hämtar princip uppsättnings definitionen med namnet VMPolicySetDefinition från den aktuella standard prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="38803-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="38803-118">Exempel 3: Hämta princip uppsättnings definition från abonnemang efter namn</span><span class="sxs-lookup"><span data-stu-id="38803-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="38803-119">Det här kommandot hämtar princip definitionen med namnet VMPolicySetDefinition från prenumerationen med ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="38803-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="38803-120">Exempel 4: Hämta alla definitioner för anpassade principer uppsättning från en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="38803-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="38803-121">Det här kommandot får alla anpassade princip uppsättnings definitioner från hanterings gruppen med namnet Dept42.</span><span class="sxs-lookup"><span data-stu-id="38803-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="38803-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38803-122">PARAMETERS</span></span>

### <span data-ttu-id="38803-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38803-123">-ApiVersion</span></span>
<span data-ttu-id="38803-124">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="38803-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="38803-125">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="38803-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="38803-126">-Inbyggt</span><span class="sxs-lookup"><span data-stu-id="38803-126">-Builtin</span></span>
<span data-ttu-id="38803-127">Begränsar listan med resultat till endast inbyggda definitioner för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="38803-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="38803-128">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="38803-128">-Custom</span></span>
<span data-ttu-id="38803-129">Begränsar listan med resultat till endast anpassade definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="38803-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="38803-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38803-130">-DefaultProfile</span></span>
<span data-ttu-id="38803-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38803-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38803-132">-ID</span><span class="sxs-lookup"><span data-stu-id="38803-132">-Id</span></span>
<span data-ttu-id="38803-133">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="38803-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="38803-134">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="38803-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="38803-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="38803-135">-ManagementGroupName</span></span>
<span data-ttu-id="38803-136">Namnet på hanterings gruppen för de princip uppsättnings definitioner som ska visas.</span><span class="sxs-lookup"><span data-stu-id="38803-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="38803-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="38803-137">-Name</span></span>
<span data-ttu-id="38803-138">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="38803-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="38803-139">-För</span><span class="sxs-lookup"><span data-stu-id="38803-139">-Pre</span></span>
<span data-ttu-id="38803-140">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="38803-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="38803-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38803-141">-SubscriptionId</span></span>
<span data-ttu-id="38803-142">Prenumerations-ID för de princip uppsättnings definitioner som ska visas.</span><span class="sxs-lookup"><span data-stu-id="38803-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="38803-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38803-143">CommonParameters</span></span>
<span data-ttu-id="38803-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38803-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38803-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38803-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38803-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38803-146">INPUTS</span></span>

### <span data-ttu-id="38803-147">System. String</span><span class="sxs-lookup"><span data-stu-id="38803-147">System.String</span></span>

### <span data-ttu-id="38803-148">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38803-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="38803-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38803-149">OUTPUTS</span></span>

### <span data-ttu-id="38803-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="38803-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="38803-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38803-151">NOTES</span></span>

## <span data-ttu-id="38803-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38803-152">RELATED LINKS</span></span>
