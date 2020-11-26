---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325151"
---
# <span data-ttu-id="867e2-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="867e2-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="867e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="867e2-102">SYNOPSIS</span></span>
<span data-ttu-id="867e2-103">Ändra eller ändra en virtuell enhets webbplats som är ansluten till en resurs för virtuella nätverk enheter.</span><span class="sxs-lookup"><span data-stu-id="867e2-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="867e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="867e2-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="867e2-105">DESCRIPTION</span></span>
<span data-ttu-id="867e2-106">Kommandot Update-AzVirtualApplianceSite ändrar en webbplats resurs för en virtuell enhet.</span><span class="sxs-lookup"><span data-stu-id="867e2-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="867e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="867e2-107">EXAMPLES</span></span>

### <span data-ttu-id="867e2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="867e2-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="867e2-109">Ändra adressprefixet för en resurs för en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="867e2-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="867e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="867e2-110">PARAMETERS</span></span>

### <span data-ttu-id="867e2-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="867e2-111">-AddresssPrefix</span></span>
<span data-ttu-id="867e2-112">Webbplatsens adressprefix.</span><span class="sxs-lookup"><span data-stu-id="867e2-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="867e2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="867e2-113">-AsJob</span></span>
<span data-ttu-id="867e2-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="867e2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="867e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867e2-115">-DefaultProfile</span></span>
<span data-ttu-id="867e2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="867e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867e2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="867e2-117">-Force</span></span>
<span data-ttu-id="867e2-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="867e2-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="867e2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="867e2-119">-Name</span></span>
<span data-ttu-id="867e2-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="867e2-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867e2-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="867e2-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="867e2-122">Virtuell nätverks apparat som den här webbplatsen är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="867e2-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="867e2-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="867e2-123">-O365Policy</span></span>
<span data-ttu-id="867e2-124">Office 365-översikten policy.</span><span class="sxs-lookup"><span data-stu-id="867e2-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="867e2-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="867e2-126">The resource group name.</span></span>

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

### <span data-ttu-id="867e2-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="867e2-127">-Tag</span></span>
<span data-ttu-id="867e2-128">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="867e2-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="867e2-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="867e2-129">-Confirm</span></span>
<span data-ttu-id="867e2-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="867e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867e2-131">-WhatIf</span></span>
<span data-ttu-id="867e2-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="867e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="867e2-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="867e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867e2-134">CommonParameters</span></span>
<span data-ttu-id="867e2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867e2-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="867e2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867e2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="867e2-137">INPUTS</span></span>

### <span data-ttu-id="867e2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="867e2-138">System.String</span></span>

### <span data-ttu-id="867e2-139">Microsoft. Azure. commands. Networks. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="867e2-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="867e2-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="867e2-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="867e2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="867e2-141">OUTPUTS</span></span>

### <span data-ttu-id="867e2-142">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="867e2-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="867e2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="867e2-143">NOTES</span></span>

## <span data-ttu-id="867e2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="867e2-144">RELATED LINKS</span></span>