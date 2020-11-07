---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756782"
---
# <span data-ttu-id="28ede-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="28ede-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="28ede-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28ede-102">SYNOPSIS</span></span>
<span data-ttu-id="28ede-103">Hämtar princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="28ede-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28ede-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28ede-104">SYNTAX</span></span>

### <span data-ttu-id="28ede-105">GetAllPolicyAssignments (standard)</span><span class="sxs-lookup"><span data-stu-id="28ede-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="28ede-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="28ede-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="28ede-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="28ede-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="28ede-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28ede-108">DESCRIPTION</span></span>
<span data-ttu-id="28ede-109">Cmdleten **Get-AzureRmPolicyAssignment** hämtar alla princip tilldelningar eller särskilda uppgifter.</span><span class="sxs-lookup"><span data-stu-id="28ede-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="28ede-110">Identifiera en princip tilldelning för att få namn och räckvidd eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="28ede-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="28ede-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28ede-111">EXAMPLES</span></span>

### <span data-ttu-id="28ede-112">Exempel 1: Hämta alla princip tilldelningar</span><span class="sxs-lookup"><span data-stu-id="28ede-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="28ede-113">Det här kommandot får alla princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="28ede-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="28ede-114">Exempel 2: Hämta en specifik princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="28ede-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="28ede-115">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28ede-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="28ede-116">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="28ede-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="28ede-117">Det andra kommandot Hämta princip tilldelningen med namnet PolicyAssignment07 för omfattningen som egenskapen **ResourceID** för $ResourceGroup identifierar.</span><span class="sxs-lookup"><span data-stu-id="28ede-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="28ede-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28ede-118">PARAMETERS</span></span>

### <span data-ttu-id="28ede-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="28ede-119">-ApiVersion</span></span>
<span data-ttu-id="28ede-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="28ede-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="28ede-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="28ede-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="28ede-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ede-122">-DefaultProfile</span></span>
<span data-ttu-id="28ede-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="28ede-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28ede-124">-ID</span><span class="sxs-lookup"><span data-stu-id="28ede-124">-Id</span></span>
<span data-ttu-id="28ede-125">Anger det fullständigt kvalificerade resurs-ID för princip tilldelningen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="28ede-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ede-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="28ede-126">-InformationAction</span></span>
<span data-ttu-id="28ede-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="28ede-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="28ede-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="28ede-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28ede-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="28ede-129">Continue</span></span>
- <span data-ttu-id="28ede-130">Över</span><span class="sxs-lookup"><span data-stu-id="28ede-130">Ignore</span></span>
- <span data-ttu-id="28ede-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="28ede-131">Inquire</span></span>
- <span data-ttu-id="28ede-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="28ede-132">SilentlyContinue</span></span>
- <span data-ttu-id="28ede-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="28ede-133">Stop</span></span>
- <span data-ttu-id="28ede-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="28ede-134">Suspend</span></span>

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

### <span data-ttu-id="28ede-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="28ede-135">-InformationVariable</span></span>
<span data-ttu-id="28ede-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="28ede-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="28ede-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="28ede-137">-Name</span></span>
<span data-ttu-id="28ede-138">Anger namnet på den princip tilldelning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="28ede-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ede-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="28ede-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="28ede-140">Anger ID för princip definitionen för de princip tilldelningar som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="28ede-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ede-141">-För</span><span class="sxs-lookup"><span data-stu-id="28ede-141">-Pre</span></span>
<span data-ttu-id="28ede-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="28ede-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="28ede-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="28ede-143">-Scope</span></span>
<span data-ttu-id="28ede-144">Anger det område där principen tillämpas för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="28ede-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ede-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ede-145">CommonParameters</span></span>
<span data-ttu-id="28ede-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ede-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ede-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ede-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ede-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28ede-148">INPUTS</span></span>

### <span data-ttu-id="28ede-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="28ede-149">None</span></span>
<span data-ttu-id="28ede-150">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="28ede-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28ede-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28ede-151">OUTPUTS</span></span>

### <span data-ttu-id="28ede-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="28ede-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="28ede-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28ede-153">NOTES</span></span>

## <span data-ttu-id="28ede-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28ede-154">RELATED LINKS</span></span>

[<span data-ttu-id="28ede-155">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="28ede-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="28ede-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="28ede-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="28ede-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="28ede-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


