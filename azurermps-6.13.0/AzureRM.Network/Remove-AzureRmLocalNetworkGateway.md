---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c09e812762867dc6aa89945f50d9658bb61bf5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574784"
---
# <span data-ttu-id="66614-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="66614-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="66614-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66614-102">SYNOPSIS</span></span>
<span data-ttu-id="66614-103">Tar bort en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="66614-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66614-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66614-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66614-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66614-105">DESCRIPTION</span></span>
<span data-ttu-id="66614-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="66614-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="66614-107">Cmdleten **Remove-AzureRmLocalNetworkGateway** tar bort objektet som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="66614-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="66614-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66614-108">EXAMPLES</span></span>

### <span data-ttu-id="66614-109">1: ta bort en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="66614-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="66614-110">Tar bort objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG" Obs! Du måste först ta bort alla anslutningar till den lokala Nätverksgatewayen med cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="66614-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="66614-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66614-111">PARAMETERS</span></span>

### <span data-ttu-id="66614-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66614-112">-AsJob</span></span>
<span data-ttu-id="66614-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="66614-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66614-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66614-114">-DefaultProfile</span></span>
<span data-ttu-id="66614-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66614-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66614-116">-Force</span><span class="sxs-lookup"><span data-stu-id="66614-116">-Force</span></span>
<span data-ttu-id="66614-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="66614-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66614-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="66614-118">-Name</span></span>
<span data-ttu-id="66614-119">Anger namnet på den lokala nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="66614-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66614-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66614-120">-PassThru</span></span>
<span data-ttu-id="66614-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="66614-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66614-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="66614-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66614-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66614-123">-ResourceGroupName</span></span>
<span data-ttu-id="66614-124">Anger namnet på den resurs grupp som innehåller den lokala Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="66614-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="66614-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66614-125">-Confirm</span></span>
<span data-ttu-id="66614-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66614-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66614-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66614-127">-WhatIf</span></span>
<span data-ttu-id="66614-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66614-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66614-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66614-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66614-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66614-130">CommonParameters</span></span>
<span data-ttu-id="66614-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66614-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66614-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66614-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66614-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66614-133">INPUTS</span></span>

### <span data-ttu-id="66614-134">System. String</span><span class="sxs-lookup"><span data-stu-id="66614-134">System.String</span></span>

## <span data-ttu-id="66614-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66614-135">OUTPUTS</span></span>

### <span data-ttu-id="66614-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66614-136">System.Boolean</span></span>

## <span data-ttu-id="66614-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66614-137">NOTES</span></span>

## <span data-ttu-id="66614-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66614-138">RELATED LINKS</span></span>

[<span data-ttu-id="66614-139">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="66614-139">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="66614-140">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="66614-140">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="66614-141">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="66614-141">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


