---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258309"
---
# <span data-ttu-id="77f6a-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="77f6a-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="77f6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="77f6a-103">Hämtar tabellen med giltighets vägar för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="77f6a-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="77f6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77f6a-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77f6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="77f6a-106">Cmdleten **Get-AzEffectiveRouteTable** returnerar den giltiga routningstabellen som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="77f6a-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="77f6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77f6a-107">EXAMPLES</span></span>

### <span data-ttu-id="77f6a-108">Exempel 1: Hämta tabellen med effektiva vägar i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="77f6a-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="77f6a-109">Det här kommandot hämtar den giltiga routningstabellen som är associerad med nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77f6a-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="77f6a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77f6a-110">PARAMETERS</span></span>

### <span data-ttu-id="77f6a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f6a-111">-AsJob</span></span>
<span data-ttu-id="77f6a-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="77f6a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77f6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f6a-113">-DefaultProfile</span></span>
<span data-ttu-id="77f6a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77f6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f6a-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="77f6a-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="77f6a-116">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="77f6a-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="77f6a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f6a-117">-ResourceGroupName</span></span>
<span data-ttu-id="77f6a-118">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="77f6a-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="77f6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f6a-119">CommonParameters</span></span>
<span data-ttu-id="77f6a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f6a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77f6a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f6a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77f6a-122">INPUTS</span></span>

### <span data-ttu-id="77f6a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="77f6a-123">System.String</span></span>

## <span data-ttu-id="77f6a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77f6a-124">OUTPUTS</span></span>

### <span data-ttu-id="77f6a-125">Microsoft. Azure. commands. Networks. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="77f6a-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="77f6a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77f6a-126">NOTES</span></span>

## <span data-ttu-id="77f6a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77f6a-127">RELATED LINKS</span></span>

[<span data-ttu-id="77f6a-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="77f6a-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


