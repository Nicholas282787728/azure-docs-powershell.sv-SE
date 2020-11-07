---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931182"
---
# <span data-ttu-id="cb604-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cb604-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="cb604-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb604-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb604-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb604-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb604-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb604-104">DESCRIPTION</span></span>

## <span data-ttu-id="cb604-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb604-105">EXAMPLES</span></span>

### <span data-ttu-id="cb604-106">9.1</span><span class="sxs-lookup"><span data-stu-id="cb604-106">1:</span></span>
```

```

## <span data-ttu-id="cb604-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb604-107">PARAMETERS</span></span>

### <span data-ttu-id="cb604-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb604-108">-DefaultProfile</span></span>
<span data-ttu-id="cb604-109">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb604-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb604-110">-Force</span><span class="sxs-lookup"><span data-stu-id="cb604-110">-Force</span></span>
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

### <span data-ttu-id="cb604-111">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="cb604-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb604-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb604-112">-Name</span></span>
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

### <span data-ttu-id="cb604-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb604-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="cb604-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb604-114">-Confirm</span></span>
<span data-ttu-id="cb604-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb604-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb604-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb604-116">-WhatIf</span></span>
<span data-ttu-id="cb604-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb604-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb604-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb604-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb604-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb604-119">CommonParameters</span></span>
<span data-ttu-id="cb604-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb604-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb604-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb604-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb604-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb604-122">INPUTS</span></span>

## <span data-ttu-id="cb604-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb604-123">OUTPUTS</span></span>

### <span data-ttu-id="cb604-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cb604-124">System.String</span></span>

## <span data-ttu-id="cb604-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb604-125">NOTES</span></span>

## <span data-ttu-id="cb604-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb604-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb604-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cb604-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="cb604-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cb604-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


