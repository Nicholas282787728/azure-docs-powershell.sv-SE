---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585099"
---
# <span data-ttu-id="59492-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="59492-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="59492-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59492-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59492-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59492-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59492-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59492-104">DESCRIPTION</span></span>

## <span data-ttu-id="59492-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59492-105">EXAMPLES</span></span>

## <span data-ttu-id="59492-106">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59492-106">PARAMETERS</span></span>

### <span data-ttu-id="59492-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59492-107">-DefaultProfile</span></span>
<span data-ttu-id="59492-108">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59492-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59492-109">-Force</span><span class="sxs-lookup"><span data-stu-id="59492-109">-Force</span></span>
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

### <span data-ttu-id="59492-110">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="59492-110">-KeyLength</span></span>
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

### <span data-ttu-id="59492-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="59492-111">-Name</span></span>
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

### <span data-ttu-id="59492-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59492-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="59492-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59492-113">-Confirm</span></span>
<span data-ttu-id="59492-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59492-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59492-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59492-115">-WhatIf</span></span>
<span data-ttu-id="59492-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59492-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59492-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59492-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59492-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59492-118">CommonParameters</span></span>
<span data-ttu-id="59492-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59492-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59492-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59492-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59492-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59492-121">INPUTS</span></span>

### <span data-ttu-id="59492-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="59492-122">None</span></span>
<span data-ttu-id="59492-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="59492-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59492-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59492-124">OUTPUTS</span></span>

### <span data-ttu-id="59492-125">System. String</span><span class="sxs-lookup"><span data-stu-id="59492-125">System.String</span></span>

## <span data-ttu-id="59492-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59492-126">NOTES</span></span>

## <span data-ttu-id="59492-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59492-127">RELATED LINKS</span></span>

[<span data-ttu-id="59492-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="59492-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="59492-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="59492-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


