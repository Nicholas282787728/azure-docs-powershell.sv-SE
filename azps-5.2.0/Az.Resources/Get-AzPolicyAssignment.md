---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397920"
---
# <span data-ttu-id="10265-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="10265-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="10265-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10265-102">SYNOPSIS</span></span>
<span data-ttu-id="10265-103">Hämtar princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="10265-103">Gets policy assignments.</span></span>

## <span data-ttu-id="10265-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10265-104">SYNTAX</span></span>

### <span data-ttu-id="10265-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="10265-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10265-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10265-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10265-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="10265-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10265-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10265-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10265-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10265-109">DESCRIPTION</span></span>
<span data-ttu-id="10265-110">Cmdleten **Get-AzPolicyAssignment** hämtar alla princip tilldelningar eller särskilda uppgifter.</span><span class="sxs-lookup"><span data-stu-id="10265-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="10265-111">Identifiera en princip tilldelning för att få namn och räckvidd eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="10265-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="10265-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10265-112">EXAMPLES</span></span>

### <span data-ttu-id="10265-113">Exempel 1: Hämta alla princip tilldelningar</span><span class="sxs-lookup"><span data-stu-id="10265-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="10265-114">Det här kommandot får alla princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="10265-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="10265-115">Exempel 2: Hämta en specifik princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="10265-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="10265-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet och lagrar den i $ResourceGroup-variabeln.</span><span class="sxs-lookup"><span data-stu-id="10265-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="10265-117">Det andra kommandot får princip tilldelningen med namnet PolicyAssignment07 för omfattningen som egenskapen **ResourceID** för $ResourceGroup identifierar.</span><span class="sxs-lookup"><span data-stu-id="10265-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="10265-118">Exempel 3: Hämta alla princip tilldelningar till en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="10265-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="10265-119">Det första kommandot anger ID för hanterings gruppen som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="10265-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="10265-120">Det andra kommandot får alla princip tilldelningar som har tilldelats hanterings gruppen med ID ' myManagementGroup '.</span><span class="sxs-lookup"><span data-stu-id="10265-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="10265-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10265-121">PARAMETERS</span></span>

### <span data-ttu-id="10265-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="10265-122">-ApiVersion</span></span>
<span data-ttu-id="10265-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="10265-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="10265-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="10265-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="10265-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10265-125">-DefaultProfile</span></span>
<span data-ttu-id="10265-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="10265-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10265-127">-ID</span><span class="sxs-lookup"><span data-stu-id="10265-127">-Id</span></span>
<span data-ttu-id="10265-128">Anger det fullständigt kvalificerade resurs-ID för princip tilldelningen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="10265-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10265-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="10265-129">-IncludeDescendent</span></span>
<span data-ttu-id="10265-130">Gör att listan med principernas princip tilldelningar omfattar alla uppgifter som är relaterade till den givna omfattningen, inklusive dem från överordnade omfattningar och från underordnade omfattningar.</span><span class="sxs-lookup"><span data-stu-id="10265-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="10265-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="10265-131">-Name</span></span>
<span data-ttu-id="10265-132">Anger namnet på den princip tilldelning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="10265-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10265-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="10265-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="10265-134">Anger ID för princip definitionen för de princip tilldelningar som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="10265-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10265-135">-För</span><span class="sxs-lookup"><span data-stu-id="10265-135">-Pre</span></span>
<span data-ttu-id="10265-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="10265-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="10265-137">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="10265-137">-Scope</span></span>
<span data-ttu-id="10265-138">Anger det område där principen tillämpas för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="10265-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10265-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10265-139">CommonParameters</span></span>
<span data-ttu-id="10265-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10265-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10265-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10265-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10265-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10265-142">INPUTS</span></span>

### <span data-ttu-id="10265-143">System. String</span><span class="sxs-lookup"><span data-stu-id="10265-143">System.String</span></span>

### <span data-ttu-id="10265-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10265-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10265-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10265-145">OUTPUTS</span></span>

### <span data-ttu-id="10265-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="10265-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="10265-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10265-147">NOTES</span></span>

## <span data-ttu-id="10265-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10265-148">RELATED LINKS</span></span>

[<span data-ttu-id="10265-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="10265-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="10265-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="10265-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="10265-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="10265-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


