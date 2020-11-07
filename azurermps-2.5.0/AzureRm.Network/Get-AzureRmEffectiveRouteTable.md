---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929397"
---
# <span data-ttu-id="a1564-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a1564-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="a1564-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1564-102">SYNOPSIS</span></span>
<span data-ttu-id="a1564-103">Hämtar tabellen med giltighets vägar för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a1564-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1564-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1564-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1564-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1564-105">DESCRIPTION</span></span>
<span data-ttu-id="a1564-106">Cmdleten **Get-AzureRmEffectiveRouteTable** returnerar den giltiga routningstabellen som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a1564-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="a1564-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1564-107">EXAMPLES</span></span>

### <span data-ttu-id="a1564-108">Exempel 1: Hämta tabellen med effektiva vägar i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="a1564-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a1564-109">Det här kommandot hämtar den giltiga routningstabellen som är associerad med nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1564-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a1564-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1564-110">PARAMETERS</span></span>

### <span data-ttu-id="a1564-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1564-111">-AsJob</span></span>
<span data-ttu-id="a1564-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a1564-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1564-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1564-113">-DefaultProfile</span></span>
<span data-ttu-id="a1564-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1564-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1564-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a1564-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="a1564-116">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a1564-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="a1564-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1564-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1564-118">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a1564-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1564-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1564-119">CommonParameters</span></span>
<span data-ttu-id="a1564-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1564-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1564-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1564-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1564-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1564-122">INPUTS</span></span>

## <span data-ttu-id="a1564-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1564-123">OUTPUTS</span></span>

### <span data-ttu-id="a1564-124">Microsoft. Azure. commands. Networks. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="a1564-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="a1564-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1564-125">NOTES</span></span>

## <span data-ttu-id="a1564-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1564-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1564-127">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1564-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


