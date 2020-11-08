---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259284"
---
# <span data-ttu-id="ed901-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ed901-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="ed901-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed901-102">SYNOPSIS</span></span>
<span data-ttu-id="ed901-103">Skapa en webbplats som är ansluten till en virtuell nätverks apparat.</span><span class="sxs-lookup"><span data-stu-id="ed901-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="ed901-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed901-104">SYNTAX</span></span>

### <span data-ttu-id="ed901-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ed901-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed901-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed901-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed901-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed901-107">DESCRIPTION</span></span>
<span data-ttu-id="ed901-108">Med kommandot New-AzVirtualApplianceSite skapas en virtuell enhets webbplats som är ansluten till en resurs för virtuella nätverk enheter.</span><span class="sxs-lookup"><span data-stu-id="ed901-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ed901-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed901-109">EXAMPLES</span></span>

### <span data-ttu-id="ed901-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed901-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="ed901-111">Skapa en ny virtuell apparat-webbplats i resurs gruppen: testrg.</span><span class="sxs-lookup"><span data-stu-id="ed901-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="ed901-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed901-112">PARAMETERS</span></span>

### <span data-ttu-id="ed901-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ed901-113">-AddressPrefix</span></span>
<span data-ttu-id="ed901-114">Webbplatsens adressprefix.</span><span class="sxs-lookup"><span data-stu-id="ed901-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="ed901-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed901-115">-AsJob</span></span>
<span data-ttu-id="ed901-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ed901-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed901-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed901-117">-DefaultProfile</span></span>
<span data-ttu-id="ed901-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed901-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed901-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ed901-119">-Force</span></span>
<span data-ttu-id="ed901-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="ed901-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ed901-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed901-121">-Name</span></span>
<span data-ttu-id="ed901-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ed901-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="ed901-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="ed901-124">Den virtuella nätverks enhet som den här webbplatsen är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="ed901-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="ed901-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="ed901-125">-O365Policy</span></span>
<span data-ttu-id="ed901-126">Office 365-översikten policy.</span><span class="sxs-lookup"><span data-stu-id="ed901-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed901-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed901-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ed901-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed901-129">-ResourceId</span></span>
<span data-ttu-id="ed901-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ed901-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ed901-131">-Tag</span></span>
<span data-ttu-id="ed901-132">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ed901-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed901-133">-Confirm</span></span>
<span data-ttu-id="ed901-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed901-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed901-135">-WhatIf</span></span>
<span data-ttu-id="ed901-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed901-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed901-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed901-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed901-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed901-138">CommonParameters</span></span>
<span data-ttu-id="ed901-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed901-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed901-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed901-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed901-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed901-141">INPUTS</span></span>

### <span data-ttu-id="ed901-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ed901-142">System.String</span></span>

### <span data-ttu-id="ed901-143">Microsoft. Azure. commands. Networks. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="ed901-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="ed901-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ed901-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ed901-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed901-145">OUTPUTS</span></span>

### <span data-ttu-id="ed901-146">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ed901-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="ed901-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed901-147">NOTES</span></span>

## <span data-ttu-id="ed901-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed901-148">RELATED LINKS</span></span>
