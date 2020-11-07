---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924313"
---
# <span data-ttu-id="c1d06-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c1d06-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c1d06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1d06-102">SYNOPSIS</span></span>

## <span data-ttu-id="c1d06-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1d06-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1d06-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1d06-104">DESCRIPTION</span></span>

## <span data-ttu-id="c1d06-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1d06-105">EXAMPLES</span></span>

### <span data-ttu-id="c1d06-106">9.1</span><span class="sxs-lookup"><span data-stu-id="c1d06-106">1:</span></span>
```

```

## <span data-ttu-id="c1d06-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1d06-107">PARAMETERS</span></span>

### <span data-ttu-id="c1d06-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d06-108">-DefaultProfile</span></span>
<span data-ttu-id="c1d06-109">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d06-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d06-110">-Force</span><span class="sxs-lookup"><span data-stu-id="c1d06-110">-Force</span></span>
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

### <span data-ttu-id="c1d06-111">-Nyckel längd</span><span class="sxs-lookup"><span data-stu-id="c1d06-111">-KeyLength</span></span>
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

### <span data-ttu-id="c1d06-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1d06-112">-Name</span></span>
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

### <span data-ttu-id="c1d06-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d06-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c1d06-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1d06-114">-Confirm</span></span>
<span data-ttu-id="c1d06-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1d06-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d06-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d06-116">-WhatIf</span></span>
<span data-ttu-id="c1d06-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1d06-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1d06-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1d06-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d06-119">CommonParameters</span></span>
<span data-ttu-id="c1d06-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d06-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d06-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d06-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1d06-122">INPUTS</span></span>

## <span data-ttu-id="c1d06-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1d06-123">OUTPUTS</span></span>

### <span data-ttu-id="c1d06-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c1d06-124">System.String</span></span>

## <span data-ttu-id="c1d06-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1d06-125">NOTES</span></span>

## <span data-ttu-id="c1d06-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1d06-126">RELATED LINKS</span></span>

[<span data-ttu-id="c1d06-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c1d06-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c1d06-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c1d06-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


