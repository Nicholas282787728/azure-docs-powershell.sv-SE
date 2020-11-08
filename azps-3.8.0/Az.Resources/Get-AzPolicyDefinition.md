---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090347"
---
# <span data-ttu-id="3beb4-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3beb4-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="3beb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3beb4-102">SYNOPSIS</span></span>
<span data-ttu-id="3beb4-103">Hämtar princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="3beb4-103">Gets policy definitions.</span></span>

## <span data-ttu-id="3beb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3beb4-104">SYNTAX</span></span>

### <span data-ttu-id="3beb4-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3beb4-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3beb4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beb4-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3beb4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beb4-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3beb4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beb4-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3beb4-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beb4-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3beb4-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beb4-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3beb4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3beb4-111">DESCRIPTION</span></span>
<span data-ttu-id="3beb4-112">Cmdleten **Get-AzPolicyDefinition** hämtar en samling princip definitioner eller en specifik princip definition som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="3beb4-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="3beb4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3beb4-113">EXAMPLES</span></span>

### <span data-ttu-id="3beb4-114">Exempel 1: Hämta alla princip definitioner</span><span class="sxs-lookup"><span data-stu-id="3beb4-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="3beb4-115">Det här kommandot får alla princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="3beb4-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="3beb4-116">Exempel 2: Hämta princip definition från aktuell prenumeration efter namn</span><span class="sxs-lookup"><span data-stu-id="3beb4-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="3beb4-117">Det här kommandot hämtar princip definitionen med namnet VMPolicyDefinition från den aktuella standard prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3beb4-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="3beb4-118">Exempel 3: Hämta princip definition från hanterings grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="3beb4-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="3beb4-119">Det här kommandot hämtar princip definitionen med namnet VMPolicyDefinition från hanterings gruppen med namnet Dept42.</span><span class="sxs-lookup"><span data-stu-id="3beb4-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="3beb4-120">Exempel 4: Hämta alla inbyggda princip definitioner från abonnemang</span><span class="sxs-lookup"><span data-stu-id="3beb4-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="3beb4-121">Det här kommandot får alla inbyggda princip definitioner från prenumerationen med ID-3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="3beb4-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="3beb4-122">Exempel 5: Hämta princip definitioner från en viss kategori</span><span class="sxs-lookup"><span data-stu-id="3beb4-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="3beb4-123">Det här kommandot får alla princip definitioner i kategorin "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="3beb4-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="3beb4-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3beb4-124">PARAMETERS</span></span>

### <span data-ttu-id="3beb4-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3beb4-125">-ApiVersion</span></span>
<span data-ttu-id="3beb4-126">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3beb4-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3beb4-127">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="3beb4-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3beb4-128">-Inbyggt</span><span class="sxs-lookup"><span data-stu-id="3beb4-128">-Builtin</span></span>
<span data-ttu-id="3beb4-129">Begränsar resultat listan till endast inbyggda princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="3beb4-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="3beb4-130">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="3beb4-130">-Custom</span></span>
<span data-ttu-id="3beb4-131">Begränsar listan med resultat till endast anpassade princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="3beb4-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="3beb4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3beb4-132">-DefaultProfile</span></span>
<span data-ttu-id="3beb4-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3beb4-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3beb4-134">-ID</span><span class="sxs-lookup"><span data-stu-id="3beb4-134">-Id</span></span>
<span data-ttu-id="3beb4-135">Anger det fullständigt kvalificerade resurs-ID för princip definitionen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="3beb4-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3beb4-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3beb4-136">-ManagementGroupName</span></span>
<span data-ttu-id="3beb4-137">Namnet på hanterings gruppen för de princip definitioner som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="3beb4-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="3beb4-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="3beb4-138">-Name</span></span>
<span data-ttu-id="3beb4-139">Anger namnet på den princip definition som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="3beb4-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3beb4-140">-För</span><span class="sxs-lookup"><span data-stu-id="3beb4-140">-Pre</span></span>
<span data-ttu-id="3beb4-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3beb4-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3beb4-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3beb4-142">-SubscriptionId</span></span>
<span data-ttu-id="3beb4-143">Prenumerations-ID för de princip definitioner som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="3beb4-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="3beb4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3beb4-144">CommonParameters</span></span>
<span data-ttu-id="3beb4-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3beb4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3beb4-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3beb4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3beb4-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3beb4-147">INPUTS</span></span>

### <span data-ttu-id="3beb4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3beb4-148">System.String</span></span>

### <span data-ttu-id="3beb4-149">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3beb4-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3beb4-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3beb4-150">OUTPUTS</span></span>

### <span data-ttu-id="3beb4-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3beb4-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3beb4-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3beb4-152">NOTES</span></span>

## <span data-ttu-id="3beb4-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3beb4-153">RELATED LINKS</span></span>

[<span data-ttu-id="3beb4-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3beb4-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="3beb4-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3beb4-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="3beb4-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3beb4-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)

