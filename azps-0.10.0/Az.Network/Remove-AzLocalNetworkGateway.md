---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922022"
---
# <span data-ttu-id="02fbd-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02fbd-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="02fbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="02fbd-103">Tar bort en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="02fbd-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="02fbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02fbd-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02fbd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="02fbd-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="02fbd-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="02fbd-107">Cmdleten **Remove-AzLocalNetworkGateway** tar bort objektet som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="02fbd-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="02fbd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02fbd-108">EXAMPLES</span></span>

### <span data-ttu-id="02fbd-109">1: ta bort en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="02fbd-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="02fbd-110">Tar bort objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="02fbd-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="02fbd-111">Obs! Du måste först ta bort alla anslutningar till den lokala Nätverksgatewayen med cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="02fbd-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="02fbd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02fbd-112">PARAMETERS</span></span>

### <span data-ttu-id="02fbd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02fbd-113">-AsJob</span></span>
<span data-ttu-id="02fbd-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="02fbd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02fbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fbd-115">-DefaultProfile</span></span>
<span data-ttu-id="02fbd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02fbd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02fbd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="02fbd-117">-Force</span></span>
<span data-ttu-id="02fbd-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="02fbd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02fbd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="02fbd-119">-Name</span></span>
<span data-ttu-id="02fbd-120">Anger namnet på den lokala nätverksgateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="02fbd-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02fbd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02fbd-121">-PassThru</span></span>
<span data-ttu-id="02fbd-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="02fbd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02fbd-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="02fbd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02fbd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02fbd-124">-ResourceGroupName</span></span>
<span data-ttu-id="02fbd-125">Anger namnet på den resurs grupp som innehåller den lokala Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="02fbd-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02fbd-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02fbd-126">-Confirm</span></span>
<span data-ttu-id="02fbd-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02fbd-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02fbd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fbd-128">-WhatIf</span></span>
<span data-ttu-id="02fbd-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02fbd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02fbd-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02fbd-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02fbd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fbd-131">CommonParameters</span></span>
<span data-ttu-id="02fbd-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02fbd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fbd-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02fbd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fbd-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02fbd-134">INPUTS</span></span>

## <span data-ttu-id="02fbd-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02fbd-135">OUTPUTS</span></span>

## <span data-ttu-id="02fbd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02fbd-136">NOTES</span></span>

## <span data-ttu-id="02fbd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02fbd-137">RELATED LINKS</span></span>

[<span data-ttu-id="02fbd-138">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02fbd-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="02fbd-139">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02fbd-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="02fbd-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="02fbd-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


