---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101496"
---
# <span data-ttu-id="76c63-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="76c63-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="76c63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76c63-102">SYNOPSIS</span></span>
<span data-ttu-id="76c63-103">Hämtar status för gäst konfigurations principer (detaljerade) för ett initiativ av typen "gäst konfiguration" som är tilldelad en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="76c63-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="76c63-104">Ett initiativ är en policy för definitions typen "initiativ".</span><span class="sxs-lookup"><span data-stu-id="76c63-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="76c63-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76c63-105">SYNTAX</span></span>

### <span data-ttu-id="76c63-106">VmScope (standard)</span><span class="sxs-lookup"><span data-stu-id="76c63-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c63-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="76c63-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c63-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="76c63-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c63-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="76c63-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c63-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76c63-110">DESCRIPTION</span></span>
<span data-ttu-id="76c63-111">Get-AzVMGuestPolicyStatus-cmdleten får status för gäst konfigurations principer för ett initiativ av typen "gäst konfiguration" som är tilldelad en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="76c63-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="76c63-112">Ett initiativ är en policy för definitions typen "initiativ".</span><span class="sxs-lookup"><span data-stu-id="76c63-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="76c63-113">Denna cmdlet tar emot efterlevnad för den virtuella datorn och gör varför den inte är kompatibel för de enskilda principerna i initiativet.</span><span class="sxs-lookup"><span data-stu-id="76c63-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="76c63-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76c63-114">EXAMPLES</span></span>

### <span data-ttu-id="76c63-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76c63-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="76c63-116">Få alla senaste status för gäst konfigurations principer för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="76c63-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="76c63-117">Statusen innehåller överensstämmelse status för VM för varje princip i alla initiativ av typen "gäst konfiguration", krav på efterlevnad, tid för kompatibilitetskontrollen, resursinformation som kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="76c63-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="76c63-118">Resultaten inkluderar senaste status, inkluderar inte tidigare historik status.</span><span class="sxs-lookup"><span data-stu-id="76c63-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="76c63-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="76c63-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="76c63-120">Få den senaste statusen för princip för gäst konfiguration efter initiativ-ID. Statusen innehåller överensstämmelse status för den virtuella datorn för varje princip i initiativet, förvalda krav, tiden för kontrollen av efterlevnad, resursinformation som kontrol leras efter efterlevnad.</span><span class="sxs-lookup"><span data-stu-id="76c63-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="76c63-121">Resultaten inkluderar inte tidigare genererade status värden, det inkluderar bara den senaste statusen för varje policy i initiativet.</span><span class="sxs-lookup"><span data-stu-id="76c63-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="76c63-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="76c63-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="76c63-123">Skaffa den senaste statusen för gäst konfigurations principen per initiativ namn.</span><span class="sxs-lookup"><span data-stu-id="76c63-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="76c63-124">Statusen innehåller överensstämmelse status för den virtuella datorn för varje princip i initiativet, förvalda krav, tiden för kontrollen av efterlevnad, resursinformation som kontrol leras efter efterlevnad.</span><span class="sxs-lookup"><span data-stu-id="76c63-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="76c63-125">Resultaten inkluderar inte tidigare genererade status värden, det inkluderar bara den senaste statusen för varje policy i initiativet.</span><span class="sxs-lookup"><span data-stu-id="76c63-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="76c63-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="76c63-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="76c63-127">Hämta status för gäst konfigurations principer via ReportId.</span><span class="sxs-lookup"><span data-stu-id="76c63-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="76c63-128">Egenskapen ReportId är den ReportId-egenskap som finns i resultatet av Get-AzVMGuestPolicyStatus efter initiativeId eller initiativ namn (se andra exempel)</span><span class="sxs-lookup"><span data-stu-id="76c63-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="76c63-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76c63-129">PARAMETERS</span></span>

### <span data-ttu-id="76c63-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c63-130">-DefaultProfile</span></span>
<span data-ttu-id="76c63-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76c63-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c63-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="76c63-132">-InitiativeId</span></span>
<span data-ttu-id="76c63-133">Definitions-ID för en policy där definitions typ är initiativ och kategori är gäst konfiguration</span><span class="sxs-lookup"><span data-stu-id="76c63-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c63-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="76c63-134">-InitiativeName</span></span>
<span data-ttu-id="76c63-135">Namnet på en policy där definitions typen är initiativ och kategori är gäst konfiguration</span><span class="sxs-lookup"><span data-stu-id="76c63-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c63-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="76c63-136">-ReportId</span></span>
<span data-ttu-id="76c63-137">ID för statusen för en gäst konfigurations princip.</span><span class="sxs-lookup"><span data-stu-id="76c63-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="76c63-138">En policy där definitions typ är initiativ och kategori är gäst konfiguration måste tilldelas ett scope för att få status.</span><span class="sxs-lookup"><span data-stu-id="76c63-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c63-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c63-139">-ResourceGroupName</span></span>
<span data-ttu-id="76c63-140">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="76c63-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c63-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="76c63-141">-VMName</span></span>
<span data-ttu-id="76c63-142">Namn på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="76c63-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c63-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c63-143">CommonParameters</span></span>
<span data-ttu-id="76c63-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c63-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c63-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c63-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c63-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76c63-146">INPUTS</span></span>

### <span data-ttu-id="76c63-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="76c63-147">None</span></span>
## <span data-ttu-id="76c63-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76c63-148">OUTPUTS</span></span>

### <span data-ttu-id="76c63-149">Microsoft. Azure. commands. GuestConfiguration. Models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="76c63-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="76c63-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76c63-150">NOTES</span></span>

## <span data-ttu-id="76c63-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76c63-151">RELATED LINKS</span></span>
