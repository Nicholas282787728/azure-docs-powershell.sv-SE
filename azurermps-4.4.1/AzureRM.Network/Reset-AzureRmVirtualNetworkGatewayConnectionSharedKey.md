---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586467"
---
# <span data-ttu-id="78587-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="78587-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="78587-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78587-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78587-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78587-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78587-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78587-104">DESCRIPTION</span></span>

## <span data-ttu-id="78587-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78587-105">EXAMPLES</span></span>

## <span data-ttu-id="78587-106">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78587-106">PARAMETERS</span></span>

### <span data-ttu-id="78587-107">-Force</span><span class="sxs-lookup"><span data-stu-id="78587-107">-Force</span></span>
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

### <span data-ttu-id="78587-108">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="78587-108">-KeyLength</span></span>
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

### <span data-ttu-id="78587-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="78587-109">-Name</span></span>
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

### <span data-ttu-id="78587-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78587-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="78587-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78587-111">-Confirm</span></span>
<span data-ttu-id="78587-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78587-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78587-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78587-113">-WhatIf</span></span>
<span data-ttu-id="78587-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78587-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78587-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78587-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78587-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78587-116">-DefaultProfile</span></span>
<span data-ttu-id="78587-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78587-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78587-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78587-118">CommonParameters</span></span>
<span data-ttu-id="78587-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78587-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78587-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78587-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78587-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78587-121">INPUTS</span></span>

## <span data-ttu-id="78587-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78587-122">OUTPUTS</span></span>

### <span data-ttu-id="78587-123">System. String</span><span class="sxs-lookup"><span data-stu-id="78587-123">System.String</span></span>

## <span data-ttu-id="78587-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78587-124">NOTES</span></span>

## <span data-ttu-id="78587-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78587-125">RELATED LINKS</span></span>

[<span data-ttu-id="78587-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="78587-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="78587-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="78587-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


