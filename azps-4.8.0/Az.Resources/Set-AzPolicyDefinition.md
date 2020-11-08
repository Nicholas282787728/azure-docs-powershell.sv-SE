---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259136"
---
# <span data-ttu-id="075b1-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="075b1-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="075b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="075b1-102">SYNOPSIS</span></span>
<span data-ttu-id="075b1-103">Ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="075b1-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="075b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="075b1-104">SYNTAX</span></span>

### <span data-ttu-id="075b1-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="075b1-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075b1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="075b1-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075b1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="075b1-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075b1-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="075b1-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075b1-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="075b1-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="075b1-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="075b1-110">DESCRIPTION</span></span>
<span data-ttu-id="075b1-111">Cmdleten **set-AzPolicyDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="075b1-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="075b1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="075b1-112">EXAMPLES</span></span>

### <span data-ttu-id="075b1-113">Exempel 1: Uppdatera beskrivningen av en princip definition</span><span class="sxs-lookup"><span data-stu-id="075b1-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="075b1-114">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="075b1-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="075b1-115">Kommandot lagrar objektet i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="075b1-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="075b1-116">Det andra kommandot uppdaterar beskrivningen av princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="075b1-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="075b1-117">Exempel 2: uppdatera läget för en princip definition</span><span class="sxs-lookup"><span data-stu-id="075b1-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="075b1-118">Det här kommandot uppdaterar princip definitionen med namnet VMPolicyDefinition med hjälp av Set-AzPolicyDefinition cmdlet för att ange egenskapen mode till "alla".</span><span class="sxs-lookup"><span data-stu-id="075b1-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="075b1-119">Exempel 3: uppdatera metadata för en princip definition</span><span class="sxs-lookup"><span data-stu-id="075b1-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="075b1-120">Det här kommandot uppdaterar metadata för en princip definition med namnet VMPolicyDefinition för att visa att kategorin är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="075b1-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="075b1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="075b1-121">PARAMETERS</span></span>

### <span data-ttu-id="075b1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="075b1-122">-ApiVersion</span></span>
<span data-ttu-id="075b1-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="075b1-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="075b1-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="075b1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075b1-125">-DefaultProfile</span></span>
<span data-ttu-id="075b1-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="075b1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="075b1-127">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="075b1-127">-Description</span></span>
<span data-ttu-id="075b1-128">Anger en ny beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="075b1-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="075b1-129">-DisplayName</span></span>
<span data-ttu-id="075b1-130">Anger ett nytt visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="075b1-131">-ID</span><span class="sxs-lookup"><span data-stu-id="075b1-131">-Id</span></span>
<span data-ttu-id="075b1-132">Anger fullständigt resurs-ID för princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="075b1-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="075b1-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="075b1-133">-InputObject</span></span>
<span data-ttu-id="075b1-134">Det princip definitions objekt som ska uppdateras från en annan cmdlet.</span><span class="sxs-lookup"><span data-stu-id="075b1-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="075b1-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="075b1-135">-ManagementGroupName</span></span>
<span data-ttu-id="075b1-136">Namnet på hanterings gruppen för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="075b1-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="075b1-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="075b1-137">-Metadata</span></span>
<span data-ttu-id="075b1-138">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-138">The metadata for policy definition.</span></span> <span data-ttu-id="075b1-139">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="075b1-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="075b1-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="075b1-140">-Mode</span></span>
<span data-ttu-id="075b1-141">Läget för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="075b1-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="075b1-142">-Name</span></span>
<span data-ttu-id="075b1-143">Anger namnet på princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="075b1-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="075b1-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="075b1-144">-Parameter</span></span>
<span data-ttu-id="075b1-145">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="075b1-146">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="075b1-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="075b1-147">-Princip</span><span class="sxs-lookup"><span data-stu-id="075b1-147">-Policy</span></span>
<span data-ttu-id="075b1-148">Anger en ny princip regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="075b1-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="075b1-149">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="075b1-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="075b1-150">-För</span><span class="sxs-lookup"><span data-stu-id="075b1-150">-Pre</span></span>
<span data-ttu-id="075b1-151">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="075b1-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="075b1-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="075b1-152">-SubscriptionId</span></span>
<span data-ttu-id="075b1-153">Abonnemangs-ID för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="075b1-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="075b1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075b1-154">CommonParameters</span></span>
<span data-ttu-id="075b1-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="075b1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075b1-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="075b1-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075b1-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="075b1-157">INPUTS</span></span>

### <span data-ttu-id="075b1-158">System. String</span><span class="sxs-lookup"><span data-stu-id="075b1-158">System.String</span></span>

### <span data-ttu-id="075b1-159">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="075b1-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="075b1-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="075b1-160">OUTPUTS</span></span>

### <span data-ttu-id="075b1-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="075b1-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="075b1-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="075b1-162">NOTES</span></span>

## <span data-ttu-id="075b1-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="075b1-163">RELATED LINKS</span></span>

[<span data-ttu-id="075b1-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="075b1-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="075b1-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="075b1-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="075b1-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="075b1-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


