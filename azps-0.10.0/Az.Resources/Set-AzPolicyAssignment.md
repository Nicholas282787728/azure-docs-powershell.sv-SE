---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 102d297f53fe51779f8831e4890c7d55bb59d2eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923781"
---
# <span data-ttu-id="5a373-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a373-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="5a373-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a373-102">SYNOPSIS</span></span>
<span data-ttu-id="5a373-103">Ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="5a373-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="5a373-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a373-104">SYNTAX</span></span>

### <span data-ttu-id="5a373-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5a373-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a373-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a373-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5a373-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a373-107">DESCRIPTION</span></span>
<span data-ttu-id="5a373-108">Cmdleten **set-AzPolicyAssignment** ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="5a373-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="5a373-109">Ange en tilldelning efter ID eller namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="5a373-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="5a373-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a373-110">EXAMPLES</span></span>

### <span data-ttu-id="5a373-111">Exempel 1: uppdatera visnings namnet</span><span class="sxs-lookup"><span data-stu-id="5a373-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="5a373-112">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a373-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="5a373-113">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="5a373-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="5a373-114">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a373-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="5a373-115">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="5a373-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="5a373-116">Det sista kommandot uppdaterar visnings namnet på princip tilldelningen i resurs gruppen som identifieras av egenskapen **ResourceID** för $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5a373-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="5a373-117">Exempel 2: lägga till en hanterad identitet i princip tilldelningen</span><span class="sxs-lookup"><span data-stu-id="5a373-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="5a373-118">Det första kommandot får princip tilldelningen med namnet PolicyAssignment från den aktuella prenumerationen med hjälp av Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a373-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="5a373-119">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="5a373-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="5a373-120">Det sista kommandot tilldelar en hanterad identitet till princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="5a373-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="5a373-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a373-121">PARAMETERS</span></span>

### <span data-ttu-id="5a373-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5a373-122">-ApiVersion</span></span>
<span data-ttu-id="5a373-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5a373-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5a373-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="5a373-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5a373-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5a373-125">-AssignIdentity</span></span>
<span data-ttu-id="5a373-126">Skapa och tilldela en Azure Active Directory-identitet för den här princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="5a373-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="5a373-127">Identiteten används när du kör distributioner för ' deployIfNotExists '-principer.</span><span class="sxs-lookup"><span data-stu-id="5a373-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="5a373-128">Plats krävs när du tilldelar en identitet.</span><span class="sxs-lookup"><span data-stu-id="5a373-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="5a373-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a373-129">-DefaultProfile</span></span>
<span data-ttu-id="5a373-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5a373-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a373-131">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5a373-131">-Description</span></span>
<span data-ttu-id="5a373-132">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="5a373-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="5a373-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a373-133">-DisplayName</span></span>
<span data-ttu-id="5a373-134">Anger ett nytt visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="5a373-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="5a373-135">-ID</span><span class="sxs-lookup"><span data-stu-id="5a373-135">-Id</span></span>
<span data-ttu-id="5a373-136">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5a373-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a373-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5a373-137">-InformationAction</span></span>
<span data-ttu-id="5a373-138">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="5a373-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="5a373-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5a373-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a373-140">Vidare</span><span class="sxs-lookup"><span data-stu-id="5a373-140">Continue</span></span>
- <span data-ttu-id="5a373-141">Över</span><span class="sxs-lookup"><span data-stu-id="5a373-141">Ignore</span></span>
- <span data-ttu-id="5a373-142">Inquire</span><span class="sxs-lookup"><span data-stu-id="5a373-142">Inquire</span></span>
- <span data-ttu-id="5a373-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5a373-143">SilentlyContinue</span></span>
- <span data-ttu-id="5a373-144">Stanna</span><span class="sxs-lookup"><span data-stu-id="5a373-144">Stop</span></span>
- <span data-ttu-id="5a373-145">Avbryt</span><span class="sxs-lookup"><span data-stu-id="5a373-145">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a373-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5a373-146">-InformationVariable</span></span>
<span data-ttu-id="5a373-147">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="5a373-147">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a373-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a373-148">-Location</span></span>
<span data-ttu-id="5a373-149">Sökvägen till princip tilldelningens resurs identitet.</span><span class="sxs-lookup"><span data-stu-id="5a373-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="5a373-150">Det här är obligatoriskt när växeln-AssignIdentity används.</span><span class="sxs-lookup"><span data-stu-id="5a373-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="5a373-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5a373-151">-Metadata</span></span>
<span data-ttu-id="5a373-152">De uppdaterade metadata för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="5a373-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="5a373-153">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="5a373-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="5a373-154">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a373-154">-Name</span></span>
<span data-ttu-id="5a373-155">Anger namnet på den princip tilldelning som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5a373-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5a373-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="5a373-156">-NotScope</span></span>
<span data-ttu-id="5a373-157">Princip tilldelningen är inte begränsad.</span><span class="sxs-lookup"><span data-stu-id="5a373-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="5a373-158">-För</span><span class="sxs-lookup"><span data-stu-id="5a373-158">-Pre</span></span>
<span data-ttu-id="5a373-159">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5a373-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5a373-160">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="5a373-160">-Scope</span></span>
<span data-ttu-id="5a373-161">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="5a373-161">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="5a373-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="5a373-162">-Sku</span></span>
<span data-ttu-id="5a373-163">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5a373-163">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a373-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a373-164">CommonParameters</span></span>
<span data-ttu-id="5a373-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a373-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a373-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a373-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a373-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a373-167">INPUTS</span></span>

## <span data-ttu-id="5a373-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a373-168">OUTPUTS</span></span>

## <span data-ttu-id="5a373-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a373-169">NOTES</span></span>

## <span data-ttu-id="5a373-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a373-170">RELATED LINKS</span></span>

[<span data-ttu-id="5a373-171">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a373-171">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="5a373-172">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a373-172">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="5a373-173">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5a373-173">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


