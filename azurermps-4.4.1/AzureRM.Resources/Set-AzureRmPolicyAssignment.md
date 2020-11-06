---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575855"
---
# <span data-ttu-id="6aa0f-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6aa0f-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6aa0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6aa0f-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa0f-103">Ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aa0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6aa0f-104">SYNTAX</span></span>

### <span data-ttu-id="6aa0f-105">Parametern för princip tilldelnings namn.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="6aa0f-106">Vis</span><span class="sxs-lookup"><span data-stu-id="6aa0f-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6aa0f-107">ID-parametern för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6aa0f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6aa0f-108">DESCRIPTION</span></span>
<span data-ttu-id="6aa0f-109">Cmdleten **set-AzureRmPolicyAssignment** ändrar en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="6aa0f-110">Ange en tilldelning efter ID eller namn och omfattning.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="6aa0f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6aa0f-111">EXAMPLES</span></span>

### <span data-ttu-id="6aa0f-112">Exempel 1: uppdatera visnings namnet</span><span class="sxs-lookup"><span data-stu-id="6aa0f-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="6aa0f-113">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="6aa0f-114">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6aa0f-115">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment med hjälp av Get-AzureRmPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6aa0f-116">Kommandot lagrar objektet i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="6aa0f-117">Det sista kommandot uppdaterar visnings namnet på den princip tilldelning som identifieras av egenskapen **ResourceID** för $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="6aa0f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6aa0f-118">PARAMETERS</span></span>

### <span data-ttu-id="6aa0f-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6aa0f-119">-ApiVersion</span></span>
<span data-ttu-id="6aa0f-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6aa0f-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6aa0f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6aa0f-122">-DisplayName</span></span>
<span data-ttu-id="6aa0f-123">Anger ett nytt visnings namn för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="6aa0f-124">-ID</span><span class="sxs-lookup"><span data-stu-id="6aa0f-124">-Id</span></span>
<span data-ttu-id="6aa0f-125">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0f-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6aa0f-126">-InformationAction</span></span>
<span data-ttu-id="6aa0f-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6aa0f-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6aa0f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6aa0f-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="6aa0f-129">Continue</span></span>
- <span data-ttu-id="6aa0f-130">Över</span><span class="sxs-lookup"><span data-stu-id="6aa0f-130">Ignore</span></span>
- <span data-ttu-id="6aa0f-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="6aa0f-131">Inquire</span></span>
- <span data-ttu-id="6aa0f-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6aa0f-132">SilentlyContinue</span></span>
- <span data-ttu-id="6aa0f-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="6aa0f-133">Stop</span></span>
- <span data-ttu-id="6aa0f-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6aa0f-134">Suspend</span></span>

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

### <span data-ttu-id="6aa0f-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6aa0f-135">-InformationVariable</span></span>
<span data-ttu-id="6aa0f-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6aa0f-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="6aa0f-137">-Name</span></span>
<span data-ttu-id="6aa0f-138">Anger namnet på den princip tilldelning som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0f-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="6aa0f-139">-NotScope</span></span>
<span data-ttu-id="6aa0f-140">Princip tilldelningen är inte begränsad.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0f-141">-För</span><span class="sxs-lookup"><span data-stu-id="6aa0f-141">-Pre</span></span>
<span data-ttu-id="6aa0f-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6aa0f-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="6aa0f-143">-Scope</span></span>
<span data-ttu-id="6aa0f-144">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa0f-145">-DefaultProfile</span></span>
<span data-ttu-id="6aa0f-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa0f-147">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6aa0f-147">-Description</span></span>
<span data-ttu-id="6aa0f-148">Beskrivningen av princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="6aa0f-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="6aa0f-149">-Sku</span></span>
<span data-ttu-id="6aa0f-150">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-150">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="6aa0f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa0f-151">CommonParameters</span></span>
<span data-ttu-id="6aa0f-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa0f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa0f-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa0f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa0f-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6aa0f-154">INPUTS</span></span>

## <span data-ttu-id="6aa0f-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6aa0f-155">OUTPUTS</span></span>

### <span data-ttu-id="6aa0f-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6aa0f-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6aa0f-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6aa0f-157">NOTES</span></span>

## <span data-ttu-id="6aa0f-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6aa0f-158">RELATED LINKS</span></span>

[<span data-ttu-id="6aa0f-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6aa0f-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6aa0f-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6aa0f-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6aa0f-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6aa0f-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


