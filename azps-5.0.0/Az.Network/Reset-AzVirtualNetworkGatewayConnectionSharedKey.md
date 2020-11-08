---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269184"
---
# <span data-ttu-id="d485e-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d485e-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="d485e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d485e-102">SYNOPSIS</span></span>
<span data-ttu-id="d485e-103">Återställer den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d485e-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="d485e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d485e-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d485e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d485e-105">DESCRIPTION</span></span>
<span data-ttu-id="d485e-106">Återställer den delade nyckeln för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d485e-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="d485e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d485e-107">EXAMPLES</span></span>

### <span data-ttu-id="d485e-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="d485e-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="d485e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d485e-109">PARAMETERS</span></span>

### <span data-ttu-id="d485e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d485e-110">-DefaultProfile</span></span>
<span data-ttu-id="d485e-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d485e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d485e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d485e-112">-Force</span></span>
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

### <span data-ttu-id="d485e-113">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="d485e-113">-KeyLength</span></span>
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

### <span data-ttu-id="d485e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d485e-114">-Name</span></span>
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

### <span data-ttu-id="d485e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d485e-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d485e-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d485e-116">-Confirm</span></span>
<span data-ttu-id="d485e-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d485e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d485e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d485e-118">-WhatIf</span></span>
<span data-ttu-id="d485e-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d485e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d485e-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d485e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d485e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d485e-121">CommonParameters</span></span>
<span data-ttu-id="d485e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d485e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d485e-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d485e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d485e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d485e-124">INPUTS</span></span>

### <span data-ttu-id="d485e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d485e-125">System.String</span></span>

### <span data-ttu-id="d485e-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="d485e-126">System.UInt32</span></span>

## <span data-ttu-id="d485e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d485e-127">OUTPUTS</span></span>

### <span data-ttu-id="d485e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d485e-128">System.String</span></span>

## <span data-ttu-id="d485e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d485e-129">NOTES</span></span>

## <span data-ttu-id="d485e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d485e-130">RELATED LINKS</span></span>

[<span data-ttu-id="d485e-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d485e-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="d485e-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d485e-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
