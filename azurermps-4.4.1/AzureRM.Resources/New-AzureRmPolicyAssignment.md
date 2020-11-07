---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756861"
---
# <span data-ttu-id="6c2c4-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6c2c4-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6c2c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2c4-103">Skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c2c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c2c4-104">SYNTAX</span></span>

### <span data-ttu-id="6c2c4-105">Princip tilldelning utan parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="6c2c4-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6c2c4-106">Princip tilldelning med parametrar via princip parameter objekt</span><span class="sxs-lookup"><span data-stu-id="6c2c4-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6c2c4-107">Princip tilldelning med parametrar via princip parameter sträng</span><span class="sxs-lookup"><span data-stu-id="6c2c4-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6c2c4-108">Princip tilldelning med parametrar via princip uppsättningens parameter objekt</span><span class="sxs-lookup"><span data-stu-id="6c2c4-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6c2c4-109">Princip tilldelning med parametrar via princip uppsättningens parameter sträng</span><span class="sxs-lookup"><span data-stu-id="6c2c4-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c2c4-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c2c4-110">DESCRIPTION</span></span>
<span data-ttu-id="6c2c4-111">Cmdleten **New-AzureRmPolicyAssignment** skapar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="6c2c4-112">Ange en princip och ett omfång.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="6c2c4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c2c4-113">EXAMPLES</span></span>

### <span data-ttu-id="6c2c4-114">Exempel 1: princip tilldelning på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="6c2c4-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="6c2c4-115">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="6c2c4-116">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6c2c4-117">Det andra kommandot hämtar princip definitionen med namnet VirtualMachinePolicy med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="6c2c4-118">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="6c2c4-119">Det slutliga kommandot tilldelar principen i $Policy på nivån för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="6c2c4-120">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="6c2c4-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c2c4-121">PARAMETERS</span></span>

### <span data-ttu-id="6c2c4-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6c2c4-122">-ApiVersion</span></span>
<span data-ttu-id="6c2c4-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6c2c4-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6c2c4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6c2c4-125">-DisplayName</span></span>
<span data-ttu-id="6c2c4-126">Anger ett visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-126">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="6c2c4-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6c2c4-127">-InformationAction</span></span>
<span data-ttu-id="6c2c4-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6c2c4-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6c2c4-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c2c4-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="6c2c4-130">Continue</span></span>
- <span data-ttu-id="6c2c4-131">Över</span><span class="sxs-lookup"><span data-stu-id="6c2c4-131">Ignore</span></span>
- <span data-ttu-id="6c2c4-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="6c2c4-132">Inquire</span></span>
- <span data-ttu-id="6c2c4-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6c2c4-133">SilentlyContinue</span></span>
- <span data-ttu-id="6c2c4-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="6c2c4-134">Stop</span></span>
- <span data-ttu-id="6c2c4-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6c2c4-135">Suspend</span></span>

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

### <span data-ttu-id="6c2c4-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6c2c4-136">-InformationVariable</span></span>
<span data-ttu-id="6c2c4-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6c2c4-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="6c2c4-138">-Name</span></span>
<span data-ttu-id="6c2c4-139">Anger ett namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2c4-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="6c2c4-140">-NotScope</span></span>
<span data-ttu-id="6c2c4-141">Inga omfattningar för princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-141">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="6c2c4-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6c2c4-142">-PolicyDefinition</span></span>
<span data-ttu-id="6c2c4-143">Anger en princip som ett **PSObject** -objekt som innehåller policy regeln.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2c4-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="6c2c4-144">-PolicyParameter</span></span>
<span data-ttu-id="6c2c4-145">Princip parameterns fil Sök väg eller princip parameter sträng.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2c4-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="6c2c4-146">-PolicyParameterObject</span></span>
<span data-ttu-id="6c2c4-147">Princip parameter objekt.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2c4-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6c2c4-148">-PolicySetDefinition</span></span>
<span data-ttu-id="6c2c4-149">Definitions objekt för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2c4-150">-För</span><span class="sxs-lookup"><span data-stu-id="6c2c4-150">-Pre</span></span>
<span data-ttu-id="6c2c4-151">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6c2c4-152">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="6c2c4-152">-Scope</span></span>
<span data-ttu-id="6c2c4-153">Anger det område där du vill tilldela principen.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="6c2c4-154">Om du till exempel vill tilldela en princip till en resurs grupp anger du följande:</span><span class="sxs-lookup"><span data-stu-id="6c2c4-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="6c2c4-155">`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="6c2c4-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2c4-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2c4-156">-DefaultProfile</span></span>
<span data-ttu-id="6c2c4-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c2c4-158">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6c2c4-158">-Description</span></span>
<span data-ttu-id="6c2c4-159">Beskrivningen av princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-159">The description for policy assignment.</span></span>

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

### <span data-ttu-id="6c2c4-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="6c2c4-160">-Sku</span></span>
<span data-ttu-id="6c2c4-161">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="6c2c4-162">Standard är gratis SKU: namn = a0, nivå = gratis</span><span class="sxs-lookup"><span data-stu-id="6c2c4-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

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

### <span data-ttu-id="6c2c4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2c4-163">CommonParameters</span></span>
<span data-ttu-id="6c2c4-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2c4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2c4-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c2c4-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2c4-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c2c4-166">INPUTS</span></span>

## <span data-ttu-id="6c2c4-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c2c4-167">OUTPUTS</span></span>

### <span data-ttu-id="6c2c4-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6c2c4-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6c2c4-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c2c4-169">NOTES</span></span>

## <span data-ttu-id="6c2c4-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c2c4-170">RELATED LINKS</span></span>

[<span data-ttu-id="6c2c4-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6c2c4-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6c2c4-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6c2c4-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6c2c4-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6c2c4-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6c2c4-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6c2c4-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


