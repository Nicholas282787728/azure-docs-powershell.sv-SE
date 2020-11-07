---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747042"
---
# <span data-ttu-id="e2cc1-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e2cc1-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="e2cc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cc1-103">Ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="e2cc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2cc1-104">SYNTAX</span></span>

### <span data-ttu-id="e2cc1-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e2cc1-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2cc1-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2cc1-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2cc1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="e2cc1-108">Cmdleten **set-AzPolicyAssignment** ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="e2cc1-109">Ange en tilldelning efter ID eller namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="e2cc1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="e2cc1-111">Exempel 1: uppdatera visnings namnet</span><span class="sxs-lookup"><span data-stu-id="e2cc1-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="e2cc1-112">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e2cc1-113">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e2cc1-114">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e2cc1-115">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e2cc1-116">Det sista kommandot uppdaterar visnings namnet på princip tilldelningen i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="e2cc1-117">Exempel 2: lägga till en hanterad identitet i princip tilldelningen</span><span class="sxs-lookup"><span data-stu-id="e2cc1-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="e2cc1-118">Det första kommandot får princip tilldelningen med namnet PolicyAssignment från den aktuella prenumerationen med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e2cc1-119">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e2cc1-120">Det sista kommandot tilldelar en hanterad identitet till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="e2cc1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2cc1-121">PARAMETERS</span></span>

### <span data-ttu-id="e2cc1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2cc1-122">-ApiVersion</span></span>
<span data-ttu-id="e2cc1-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e2cc1-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e2cc1-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e2cc1-125">-AssignIdentity</span></span>
<span data-ttu-id="e2cc1-126">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="e2cc1-127">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="e2cc1-128">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="e2cc1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2cc1-129">-DefaultProfile</span></span>
<span data-ttu-id="e2cc1-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e2cc1-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2cc1-131">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e2cc1-131">-Description</span></span>
<span data-ttu-id="e2cc1-132">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="e2cc1-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="e2cc1-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e2cc1-133">-DisplayName</span></span>
<span data-ttu-id="e2cc1-134">Anger ett nytt visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="e2cc1-135">-ID</span><span class="sxs-lookup"><span data-stu-id="e2cc1-135">-Id</span></span>
<span data-ttu-id="e2cc1-136">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e2cc1-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="e2cc1-137">-Location</span></span>
<span data-ttu-id="e2cc1-138">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="e2cc1-139">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="e2cc1-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e2cc1-140">-Metadata</span></span>
<span data-ttu-id="e2cc1-141">De uppdaterade metadata för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="e2cc1-142">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="e2cc1-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2cc1-143">-Name</span></span>
<span data-ttu-id="e2cc1-144">Anger namnet på den princip tilldelning som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e2cc1-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="e2cc1-145">-NotScope</span></span>
<span data-ttu-id="e2cc1-146">Princip tilldelningen är inte begränsad.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-146">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2cc1-147">-För</span><span class="sxs-lookup"><span data-stu-id="e2cc1-147">-Pre</span></span>
<span data-ttu-id="e2cc1-148">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e2cc1-149">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="e2cc1-149">-Scope</span></span>
<span data-ttu-id="e2cc1-150">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-150">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="e2cc1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cc1-151">CommonParameters</span></span>
<span data-ttu-id="e2cc1-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2cc1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cc1-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2cc1-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cc1-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2cc1-154">INPUTS</span></span>

### <span data-ttu-id="e2cc1-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e2cc1-155">System.String</span></span>

### <span data-ttu-id="e2cc1-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="e2cc1-156">System.String[]</span></span>

## <span data-ttu-id="e2cc1-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2cc1-157">OUTPUTS</span></span>

### <span data-ttu-id="e2cc1-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e2cc1-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e2cc1-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2cc1-159">NOTES</span></span>

## <span data-ttu-id="e2cc1-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2cc1-160">RELATED LINKS</span></span>

[<span data-ttu-id="e2cc1-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e2cc1-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="e2cc1-162">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e2cc1-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="e2cc1-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e2cc1-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


