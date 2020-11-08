---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 9f6f23babc1dfaf947a7eb8cea88011ff184cce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089463"
---
# <span data-ttu-id="ef950-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef950-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="ef950-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef950-102">SYNOPSIS</span></span>
<span data-ttu-id="ef950-103">Ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="ef950-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="ef950-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef950-104">SYNTAX</span></span>

### <span data-ttu-id="ef950-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ef950-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef950-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef950-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef950-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef950-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef950-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef950-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef950-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef950-109">DESCRIPTION</span></span>
<span data-ttu-id="ef950-110">Cmdleten **set-AzPolicyDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="ef950-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="ef950-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef950-111">EXAMPLES</span></span>

### <span data-ttu-id="ef950-112">Exempel 1: Uppdatera beskrivningen av en princip definition</span><span class="sxs-lookup"><span data-stu-id="ef950-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="ef950-113">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef950-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ef950-114">Kommandot lagrar objektet i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="ef950-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="ef950-115">Det andra kommandot uppdaterar beskrivningen av princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ef950-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="ef950-116">Exempel 2: uppdatera läget för en princip definition</span><span class="sxs-lookup"><span data-stu-id="ef950-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="ef950-117">Det här kommandot uppdaterar princip definitionen med namnet VMPolicyDefinition med hjälp av Set-AzPolicyDefinition cmdlet för att ange egenskapen mode till "alla".</span><span class="sxs-lookup"><span data-stu-id="ef950-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="ef950-118">Exempel 3: uppdatera metadata för en princip definition</span><span class="sxs-lookup"><span data-stu-id="ef950-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="ef950-119">Det här kommandot uppdaterar metadata för en princip definition med namnet VMPolicyDefinition för att visa att kategorin är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="ef950-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="ef950-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef950-120">PARAMETERS</span></span>

### <span data-ttu-id="ef950-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef950-121">-ApiVersion</span></span>
<span data-ttu-id="ef950-122">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ef950-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef950-123">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ef950-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef950-124">-DefaultProfile</span></span>
<span data-ttu-id="ef950-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ef950-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef950-126">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ef950-126">-Description</span></span>
<span data-ttu-id="ef950-127">Anger en ny beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="ef950-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ef950-128">-DisplayName</span></span>
<span data-ttu-id="ef950-129">Anger ett nytt visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="ef950-130">-ID</span><span class="sxs-lookup"><span data-stu-id="ef950-130">-Id</span></span>
<span data-ttu-id="ef950-131">Anger fullständigt resurs-ID för princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ef950-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ef950-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ef950-132">-ManagementGroupName</span></span>
<span data-ttu-id="ef950-133">Namnet på hanterings gruppen för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ef950-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="ef950-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ef950-134">-Metadata</span></span>
<span data-ttu-id="ef950-135">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-135">The metadata for policy definition.</span></span> <span data-ttu-id="ef950-136">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="ef950-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="ef950-137">-Mode</span><span class="sxs-lookup"><span data-stu-id="ef950-137">-Mode</span></span>
<span data-ttu-id="ef950-138">Läget för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="ef950-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef950-139">-Name</span></span>
<span data-ttu-id="ef950-140">Anger namnet på princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ef950-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ef950-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ef950-141">-Parameter</span></span>
<span data-ttu-id="ef950-142">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="ef950-143">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="ef950-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="ef950-144">-Princip</span><span class="sxs-lookup"><span data-stu-id="ef950-144">-Policy</span></span>
<span data-ttu-id="ef950-145">Anger en ny princip regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ef950-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="ef950-146">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="ef950-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="ef950-147">-För</span><span class="sxs-lookup"><span data-stu-id="ef950-147">-Pre</span></span>
<span data-ttu-id="ef950-148">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ef950-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ef950-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef950-149">-SubscriptionId</span></span>
<span data-ttu-id="ef950-150">Abonnemangs-ID för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ef950-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="ef950-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef950-151">CommonParameters</span></span>
<span data-ttu-id="ef950-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef950-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef950-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef950-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef950-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef950-154">INPUTS</span></span>

### <span data-ttu-id="ef950-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ef950-155">System.String</span></span>

### <span data-ttu-id="ef950-156">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef950-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ef950-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef950-157">OUTPUTS</span></span>

### <span data-ttu-id="ef950-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ef950-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ef950-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef950-159">NOTES</span></span>

## <span data-ttu-id="ef950-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef950-160">RELATED LINKS</span></span>

[<span data-ttu-id="ef950-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef950-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="ef950-162">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef950-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="ef950-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ef950-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


