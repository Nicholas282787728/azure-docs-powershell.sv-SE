---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930102"
---
# <span data-ttu-id="c39f7-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c39f7-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="c39f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c39f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c39f7-103">Hämtar princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="c39f7-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c39f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c39f7-104">SYNTAX</span></span>

### <span data-ttu-id="c39f7-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c39f7-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c39f7-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c39f7-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c39f7-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="c39f7-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c39f7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c39f7-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c39f7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c39f7-109">DESCRIPTION</span></span>
<span data-ttu-id="c39f7-110">Cmdleten **Get-AzureRmPolicyAssignment** hämtar alla princip tilldelningar eller särskilda uppgifter.</span><span class="sxs-lookup"><span data-stu-id="c39f7-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="c39f7-111">Identifiera en princip tilldelning för att få namn och räckvidd eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="c39f7-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="c39f7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c39f7-112">EXAMPLES</span></span>

### <span data-ttu-id="c39f7-113">Exempel 1: Hämta alla princip tilldelningar</span><span class="sxs-lookup"><span data-stu-id="c39f7-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="c39f7-114">Det här kommandot får alla princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="c39f7-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="c39f7-115">Exempel 2: Hämta en specifik princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="c39f7-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c39f7-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 genom att använda Get-AzureRMResourceGroup cmdletand lagrar den i $ResourceGroup variabeln.</span><span class="sxs-lookup"><span data-stu-id="c39f7-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c39f7-117">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment07 för omfattningen som egenskapen **ResourceID** för $ResourceGroup identifierar.</span><span class="sxs-lookup"><span data-stu-id="c39f7-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="c39f7-118">Exempel 3: Hämta alla princip tilldelningar till en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="c39f7-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="c39f7-119">Det första kommandot anger ID för hanterings gruppen som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="c39f7-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="c39f7-120">Det andra kommandot får alla princip tilldelningar som har tilldelats hanterings gruppen med ID ' myManagementGroup '.</span><span class="sxs-lookup"><span data-stu-id="c39f7-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="c39f7-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c39f7-121">PARAMETERS</span></span>

### <span data-ttu-id="c39f7-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c39f7-122">-ApiVersion</span></span>
<span data-ttu-id="c39f7-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c39f7-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c39f7-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="c39f7-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c39f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39f7-125">-DefaultProfile</span></span>
<span data-ttu-id="c39f7-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c39f7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c39f7-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c39f7-127">-Id</span></span>
<span data-ttu-id="c39f7-128">Anger det fullständigt kvalificerade resurs-ID för princip tilldelningen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="c39f7-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c39f7-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="c39f7-129">-IncludeDescendent</span></span>
<span data-ttu-id="c39f7-130">Gör att listan med principernas princip tilldelningar omfattar alla uppgifter som är relaterade till den givna omfattningen, inklusive dem från överordnade omfattningar och från underordnade omfattningar.</span><span class="sxs-lookup"><span data-stu-id="c39f7-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39f7-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c39f7-131">-InformationAction</span></span>
<span data-ttu-id="c39f7-132">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c39f7-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="c39f7-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c39f7-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c39f7-134">Vidare</span><span class="sxs-lookup"><span data-stu-id="c39f7-134">Continue</span></span>
- <span data-ttu-id="c39f7-135">Över</span><span class="sxs-lookup"><span data-stu-id="c39f7-135">Ignore</span></span>
- <span data-ttu-id="c39f7-136">Inquire</span><span class="sxs-lookup"><span data-stu-id="c39f7-136">Inquire</span></span>
- <span data-ttu-id="c39f7-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c39f7-137">SilentlyContinue</span></span>
- <span data-ttu-id="c39f7-138">Stanna</span><span class="sxs-lookup"><span data-stu-id="c39f7-138">Stop</span></span>
- <span data-ttu-id="c39f7-139">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c39f7-139">Suspend</span></span>

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

### <span data-ttu-id="c39f7-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c39f7-140">-InformationVariable</span></span>
<span data-ttu-id="c39f7-141">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c39f7-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c39f7-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="c39f7-142">-Name</span></span>
<span data-ttu-id="c39f7-143">Anger namnet på den princip tilldelning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c39f7-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39f7-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c39f7-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="c39f7-145">Anger ID för princip definitionen för de princip tilldelningar som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="c39f7-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39f7-146">-För</span><span class="sxs-lookup"><span data-stu-id="c39f7-146">-Pre</span></span>
<span data-ttu-id="c39f7-147">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c39f7-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c39f7-148">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c39f7-148">-Scope</span></span>
<span data-ttu-id="c39f7-149">Anger det område där principen tillämpas för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c39f7-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39f7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39f7-150">CommonParameters</span></span>
<span data-ttu-id="c39f7-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c39f7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39f7-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39f7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39f7-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c39f7-153">INPUTS</span></span>

## <span data-ttu-id="c39f7-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c39f7-154">OUTPUTS</span></span>

## <span data-ttu-id="c39f7-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c39f7-155">NOTES</span></span>

## <span data-ttu-id="c39f7-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c39f7-156">RELATED LINKS</span></span>

[<span data-ttu-id="c39f7-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c39f7-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c39f7-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c39f7-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c39f7-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c39f7-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


