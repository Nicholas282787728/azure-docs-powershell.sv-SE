---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: e051bd56aa8c5b5da27e2179b8f4d58ec4e4196d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757556"
---
# <span data-ttu-id="a8762-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a8762-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a8762-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8762-102">SYNOPSIS</span></span>
<span data-ttu-id="a8762-103">Återställer den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8762-103">Resets the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8762-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8762-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8762-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8762-105">DESCRIPTION</span></span>
<span data-ttu-id="a8762-106">Återställer den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8762-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="a8762-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8762-107">EXAMPLES</span></span>

### <span data-ttu-id="a8762-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="a8762-108">Example 1:</span></span>
```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="a8762-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8762-109">PARAMETERS</span></span>

### <span data-ttu-id="a8762-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8762-110">-DefaultProfile</span></span>
<span data-ttu-id="a8762-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8762-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8762-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a8762-112">-Force</span></span>
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

### <span data-ttu-id="a8762-113">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="a8762-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8762-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8762-114">-Name</span></span>
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

### <span data-ttu-id="a8762-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8762-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a8762-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8762-116">-Confirm</span></span>
<span data-ttu-id="a8762-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8762-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8762-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8762-118">-WhatIf</span></span>
<span data-ttu-id="a8762-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8762-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8762-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8762-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8762-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8762-121">CommonParameters</span></span>
<span data-ttu-id="a8762-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8762-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8762-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8762-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8762-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8762-124">INPUTS</span></span>

### <span data-ttu-id="a8762-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a8762-125">System.String</span></span>

### <span data-ttu-id="a8762-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="a8762-126">System.UInt32</span></span>

## <span data-ttu-id="a8762-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8762-127">OUTPUTS</span></span>

### <span data-ttu-id="a8762-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a8762-128">System.String</span></span>

## <span data-ttu-id="a8762-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8762-129">NOTES</span></span>

## <span data-ttu-id="a8762-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8762-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8762-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a8762-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a8762-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a8762-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


