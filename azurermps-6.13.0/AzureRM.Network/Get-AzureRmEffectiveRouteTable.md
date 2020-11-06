---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 8095e2ebd1d9e55e8f5bc847f4a72277363e197a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584127"
---
# <span data-ttu-id="7cfc8-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7cfc8-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="7cfc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cfc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfc8-103">Hämtar tabellen med giltighets vägar för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cfc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cfc8-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cfc8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cfc8-105">DESCRIPTION</span></span>
<span data-ttu-id="7cfc8-106">Cmdleten **Get-AzureRmEffectiveRouteTable** returnerar den giltiga routningstabellen som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="7cfc8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cfc8-107">EXAMPLES</span></span>

### <span data-ttu-id="7cfc8-108">Exempel 1: Hämta tabellen med effektiva vägar i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="7cfc8-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7cfc8-109">Det här kommandot hämtar den giltiga routningstabellen som är associerad med nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7cfc8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cfc8-110">PARAMETERS</span></span>

### <span data-ttu-id="7cfc8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cfc8-111">-AsJob</span></span>
<span data-ttu-id="7cfc8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7cfc8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cfc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfc8-113">-DefaultProfile</span></span>
<span data-ttu-id="7cfc8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cfc8-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7cfc8-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="7cfc8-116">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="7cfc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cfc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cfc8-118">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="7cfc8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfc8-119">CommonParameters</span></span>
<span data-ttu-id="7cfc8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cfc8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfc8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cfc8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfc8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cfc8-122">INPUTS</span></span>

### <span data-ttu-id="7cfc8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7cfc8-123">System.String</span></span>

## <span data-ttu-id="7cfc8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cfc8-124">OUTPUTS</span></span>

### <span data-ttu-id="7cfc8-125">Microsoft. Azure. commands. Networks. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="7cfc8-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="7cfc8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cfc8-126">NOTES</span></span>

## <span data-ttu-id="7cfc8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cfc8-127">RELATED LINKS</span></span>

[<span data-ttu-id="7cfc8-128">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cfc8-128">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


