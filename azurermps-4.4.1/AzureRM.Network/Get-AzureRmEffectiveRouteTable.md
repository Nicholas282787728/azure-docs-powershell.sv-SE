---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578403"
---
# <span data-ttu-id="53be0-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="53be0-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="53be0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53be0-102">SYNOPSIS</span></span>
<span data-ttu-id="53be0-103">Hämtar tabellen med giltighets vägar för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53be0-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53be0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53be0-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53be0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53be0-105">DESCRIPTION</span></span>
<span data-ttu-id="53be0-106">Cmdleten **Get-AzureRmEffectiveRouteTable** returnerar den giltiga routningstabellen som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53be0-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="53be0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53be0-107">EXAMPLES</span></span>

### <span data-ttu-id="53be0-108">Exempel 1: Hämta tabellen med effektiva vägar i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="53be0-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="53be0-109">Det här kommandot hämtar den giltiga routningstabellen som är associerad med nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="53be0-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="53be0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53be0-110">PARAMETERS</span></span>

### <span data-ttu-id="53be0-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="53be0-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="53be0-112">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53be0-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="53be0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53be0-113">-ResourceGroupName</span></span>
<span data-ttu-id="53be0-114">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="53be0-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="53be0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53be0-115">-DefaultProfile</span></span>
<span data-ttu-id="53be0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53be0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53be0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53be0-117">CommonParameters</span></span>
<span data-ttu-id="53be0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53be0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53be0-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53be0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53be0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53be0-120">INPUTS</span></span>

## <span data-ttu-id="53be0-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53be0-121">OUTPUTS</span></span>

### <span data-ttu-id="53be0-122">Microsoft. Azure. commands. Networks. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="53be0-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="53be0-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53be0-123">NOTES</span></span>

## <span data-ttu-id="53be0-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53be0-124">RELATED LINKS</span></span>

[<span data-ttu-id="53be0-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53be0-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)

