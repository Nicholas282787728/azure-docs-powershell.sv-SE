---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 175082a90a1a494eb4508bc83d71584326c9eb97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917921"
---
# <span data-ttu-id="78a19-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78a19-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="78a19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78a19-102">SYNOPSIS</span></span>
<span data-ttu-id="78a19-103">Ändrar en ExpressRoute kors koppling.</span><span class="sxs-lookup"><span data-stu-id="78a19-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="78a19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78a19-104">SYNTAX</span></span>

### <span data-ttu-id="78a19-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="78a19-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a19-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="78a19-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a19-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78a19-107">DESCRIPTION</span></span>
<span data-ttu-id="78a19-108">Cmdleten **set-AzExpressRouteCrossConnection** sparar den ändrade ExpressRoute-kors anslutningen till Azure.</span><span class="sxs-lookup"><span data-stu-id="78a19-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="78a19-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78a19-109">EXAMPLES</span></span>

### <span data-ttu-id="78a19-110">Exempel 1: ändra etablerings tillståndet för tjänste leverantören för en ExpressRoute-kors anslutning</span><span class="sxs-lookup"><span data-stu-id="78a19-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="78a19-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78a19-111">PARAMETERS</span></span>

### <span data-ttu-id="78a19-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78a19-112">-AsJob</span></span>
<span data-ttu-id="78a19-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="78a19-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78a19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a19-114">-DefaultProfile</span></span>
<span data-ttu-id="78a19-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78a19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a19-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78a19-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="78a19-117">Anger det **ExpressRouteCrossConnection** -objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="78a19-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a19-118">-Force</span><span class="sxs-lookup"><span data-stu-id="78a19-118">-Force</span></span>
<span data-ttu-id="78a19-119">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="78a19-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78a19-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="78a19-120">-Name</span></span>
<span data-ttu-id="78a19-121">Namnet på snabb vägs kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="78a19-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a19-122">-Peers</span><span class="sxs-lookup"><span data-stu-id="78a19-122">-Peerings</span></span>
<span data-ttu-id="78a19-123">Listan över peers för kors anslutningen</span><span class="sxs-lookup"><span data-stu-id="78a19-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a19-124">-ResourceGroupName</span></span>
<span data-ttu-id="78a19-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78a19-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a19-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="78a19-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="78a19-127">Tjänste leverantören noterar</span><span class="sxs-lookup"><span data-stu-id="78a19-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a19-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="78a19-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="78a19-129">Tjänst leverantörens etablerings tillstånd ska ställas in</span><span class="sxs-lookup"><span data-stu-id="78a19-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a19-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78a19-130">-Confirm</span></span>
<span data-ttu-id="78a19-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78a19-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a19-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a19-132">-WhatIf</span></span>
<span data-ttu-id="78a19-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78a19-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78a19-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78a19-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a19-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a19-135">CommonParameters</span></span>
<span data-ttu-id="78a19-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a19-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a19-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a19-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a19-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78a19-138">INPUTS</span></span>

### <span data-ttu-id="78a19-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78a19-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="78a19-140">Parametern ' ExpressRouteCrossConnection ' godkänner värdet av typen ' PSExpressRouteCrossConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="78a19-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="78a19-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78a19-141">OUTPUTS</span></span>

### <span data-ttu-id="78a19-142">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78a19-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="78a19-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78a19-143">NOTES</span></span>

## <span data-ttu-id="78a19-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78a19-144">RELATED LINKS</span></span>

[<span data-ttu-id="78a19-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78a19-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)