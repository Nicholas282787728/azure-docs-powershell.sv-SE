---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 2e2474b784d66c3c3c34bc9ea9abc2b0959ea500
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916678"
---
# <span data-ttu-id="1983f-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="1983f-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="1983f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1983f-102">SYNOPSIS</span></span>
<span data-ttu-id="1983f-103">Hämtar status historik för gäst konfigurations principer för ett initiativ av typen "gäst konfiguration" som är tilldelad en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1983f-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="1983f-104">Ett initiativ är en policy för definitions typen "initiativ".</span><span class="sxs-lookup"><span data-stu-id="1983f-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="1983f-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1983f-105">SYNTAX</span></span>

### <span data-ttu-id="1983f-106">InitiativeNameScope (standard)</span><span class="sxs-lookup"><span data-stu-id="1983f-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1983f-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="1983f-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1983f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1983f-108">DESCRIPTION</span></span>
<span data-ttu-id="1983f-109">Den Get-AzVMGuestPolicyStatusHistory cmdleten hämtar status historik för principer för gäst konfiguration för ett initiativ av typen "gäst konfiguration" som är tilldelad en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1983f-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="1983f-110">Ett initiativ är en policy för definitions typen "initiativ".</span><span class="sxs-lookup"><span data-stu-id="1983f-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="1983f-111">Använd Get-AzVMGuestPolicyStatus cmdlet för att få information om en enskild kompatibilitetsstatus med hjälp av ReportId som finns i utdata från Get-AzVMGuestPolicyStatusHistory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1983f-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="1983f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1983f-112">EXAMPLES</span></span>

### <span data-ttu-id="1983f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1983f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="1983f-114">Hämtar status historik för regelefterlevnad efter initiativ-ID. ShowOnlyChange-växeln visar endast historik för historisk status.</span><span class="sxs-lookup"><span data-stu-id="1983f-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="1983f-115">Hoppar över status som inte har ändrats mellan två kontroll kontroller.</span><span class="sxs-lookup"><span data-stu-id="1983f-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="1983f-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1983f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="1983f-117">Hämtar status historik för regelefterlevnad efter initiativ namn.</span><span class="sxs-lookup"><span data-stu-id="1983f-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="1983f-118">ShowOnlyChange-växeln visar endast historik för historisk status.</span><span class="sxs-lookup"><span data-stu-id="1983f-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="1983f-119">Hoppar över status som inte har ändrats mellan två kontroll kontroller.</span><span class="sxs-lookup"><span data-stu-id="1983f-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="1983f-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1983f-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="1983f-121">Status historik för alla principer för gäst konfiguration som tilldelats den virtuella datorn hämtas.</span><span class="sxs-lookup"><span data-stu-id="1983f-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="1983f-122">ShowOnlyChange-växeln visar endast historik för historisk status.</span><span class="sxs-lookup"><span data-stu-id="1983f-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="1983f-123">Hoppar över status som inte har ändrats mellan två kontroll kontroller.</span><span class="sxs-lookup"><span data-stu-id="1983f-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="1983f-124">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="1983f-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="1983f-125">Hämtar status historik för regelefterlevnad efter initiativ-ID.</span><span class="sxs-lookup"><span data-stu-id="1983f-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="1983f-126">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="1983f-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="1983f-127">Hämtar status historik för regelefterlevnad efter initiativ namn.</span><span class="sxs-lookup"><span data-stu-id="1983f-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="1983f-128">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="1983f-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="1983f-129">Status historik för alla principer för gäst konfiguration som tilldelats den virtuella datorn hämtas.</span><span class="sxs-lookup"><span data-stu-id="1983f-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="1983f-130">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="1983f-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="1983f-131">Hämta status för gäst konfigurations principer via ReportId.</span><span class="sxs-lookup"><span data-stu-id="1983f-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="1983f-132">Egenskapen ReportId är ReportId som finns i resultatet av Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="1983f-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="1983f-133">(se andra exempel)</span><span class="sxs-lookup"><span data-stu-id="1983f-133">(please refer other examples)</span></span>

## <span data-ttu-id="1983f-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1983f-134">PARAMETERS</span></span>

### <span data-ttu-id="1983f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1983f-135">-DefaultProfile</span></span>
<span data-ttu-id="1983f-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1983f-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1983f-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="1983f-137">-InitiativeId</span></span>
<span data-ttu-id="1983f-138">Definitions-ID för en policy där definitions typ är initiativ och kategori är gäst konfiguration</span><span class="sxs-lookup"><span data-stu-id="1983f-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983f-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="1983f-139">-InitiativeName</span></span>
<span data-ttu-id="1983f-140">Namnet på en policy där definitions typen är initiativ och kategori är gäst konfiguration</span><span class="sxs-lookup"><span data-stu-id="1983f-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="1983f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1983f-141">-ResourceGroupName</span></span>
<span data-ttu-id="1983f-142">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1983f-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983f-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="1983f-143">-ShowOnlyChange</span></span>
<span data-ttu-id="1983f-144">Visar historiska status ändringar endast för principer för gäst konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1983f-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="1983f-145">Hoppar över status som inte har ändrats mellan två granskningar för överensstämmelse.</span><span class="sxs-lookup"><span data-stu-id="1983f-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983f-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="1983f-146">-VMName</span></span>
<span data-ttu-id="1983f-147">Namn på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1983f-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1983f-148">CommonParameters</span></span>
<span data-ttu-id="1983f-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1983f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1983f-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1983f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1983f-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1983f-151">INPUTS</span></span>

### <span data-ttu-id="1983f-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="1983f-152">None</span></span>
## <span data-ttu-id="1983f-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1983f-153">OUTPUTS</span></span>

### <span data-ttu-id="1983f-154">Microsoft. Azure. commands. GuestConfiguration. Models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="1983f-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="1983f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1983f-155">NOTES</span></span>

## <span data-ttu-id="1983f-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1983f-156">RELATED LINKS</span></span>
