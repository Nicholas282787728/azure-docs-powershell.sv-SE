---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583039"
---
# <span data-ttu-id="c1de9-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1de9-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="c1de9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1de9-102">SYNOPSIS</span></span>
<span data-ttu-id="c1de9-103">Ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="c1de9-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1de9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1de9-104">SYNTAX</span></span>

### <span data-ttu-id="c1de9-105">SetByPolicyAssignmentName (standard)</span><span class="sxs-lookup"><span data-stu-id="c1de9-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c1de9-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="c1de9-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c1de9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1de9-107">DESCRIPTION</span></span>
<span data-ttu-id="c1de9-108">Cmdleten **set-AzureRmPolicyAssignment** ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="c1de9-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="c1de9-109">Ange en tilldelning efter ID eller namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="c1de9-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="c1de9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1de9-110">EXAMPLES</span></span>

### <span data-ttu-id="c1de9-111">Exempel 1: uppdatera visnings namnet</span><span class="sxs-lookup"><span data-stu-id="c1de9-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="c1de9-112">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1de9-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="c1de9-113">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="c1de9-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="c1de9-114">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzureRmPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1de9-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="c1de9-115">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="c1de9-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="c1de9-116">Det sista kommandot uppdaterar visnings namnet på den princip tilldelning som identifieras av egenskapen **ResourceID** för $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="c1de9-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="c1de9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1de9-117">PARAMETERS</span></span>

### <span data-ttu-id="c1de9-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1de9-118">-ApiVersion</span></span>
<span data-ttu-id="c1de9-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c1de9-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1de9-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="c1de9-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1de9-121">-DefaultProfile</span></span>
<span data-ttu-id="c1de9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c1de9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c1de9-123">-Description</span></span>
<span data-ttu-id="c1de9-124">Beskrivning av princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="c1de9-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1de9-125">-DisplayName</span></span>
<span data-ttu-id="c1de9-126">Anger ett nytt visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="c1de9-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c1de9-127">-Id</span></span>
<span data-ttu-id="c1de9-128">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c1de9-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c1de9-129">-InformationAction</span></span>
<span data-ttu-id="c1de9-130">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c1de9-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c1de9-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c1de9-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c1de9-132">Vidare</span><span class="sxs-lookup"><span data-stu-id="c1de9-132">Continue</span></span>
- <span data-ttu-id="c1de9-133">Över</span><span class="sxs-lookup"><span data-stu-id="c1de9-133">Ignore</span></span>
- <span data-ttu-id="c1de9-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="c1de9-134">Inquire</span></span>
- <span data-ttu-id="c1de9-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c1de9-135">SilentlyContinue</span></span>
- <span data-ttu-id="c1de9-136">Stanna</span><span class="sxs-lookup"><span data-stu-id="c1de9-136">Stop</span></span>
- <span data-ttu-id="c1de9-137">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c1de9-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c1de9-138">-InformationVariable</span></span>
<span data-ttu-id="c1de9-139">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c1de9-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1de9-140">-Name</span></span>
<span data-ttu-id="c1de9-141">Anger namnet på den princip tilldelning som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c1de9-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="c1de9-142">-NotScope</span></span>
<span data-ttu-id="c1de9-143">Princip tilldelningen är inte begränsad.</span><span class="sxs-lookup"><span data-stu-id="c1de9-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-144">-För</span><span class="sxs-lookup"><span data-stu-id="c1de9-144">-Pre</span></span>
<span data-ttu-id="c1de9-145">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c1de9-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-146">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c1de9-146">-Scope</span></span>
<span data-ttu-id="c1de9-147">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="c1de9-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1de9-148">-Sku</span></span>
<span data-ttu-id="c1de9-149">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c1de9-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1de9-150">CommonParameters</span></span>
<span data-ttu-id="c1de9-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1de9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1de9-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1de9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1de9-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1de9-153">INPUTS</span></span>

### <span data-ttu-id="c1de9-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="c1de9-154">None</span></span>
<span data-ttu-id="c1de9-155">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c1de9-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1de9-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1de9-156">OUTPUTS</span></span>

### <span data-ttu-id="c1de9-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c1de9-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c1de9-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1de9-158">NOTES</span></span>

## <span data-ttu-id="c1de9-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1de9-159">RELATED LINKS</span></span>

[<span data-ttu-id="c1de9-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1de9-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c1de9-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1de9-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c1de9-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c1de9-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


