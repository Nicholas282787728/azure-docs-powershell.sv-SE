---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929398"
---
# <span data-ttu-id="75d9e-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="75d9e-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="75d9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="75d9e-103">Hämtar den effektiva nätverks säkerhets gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="75d9e-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75d9e-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="75d9e-106">Cmdleten **Get-AzureRmEffectiveNetworkSecurityGroup** returnerar den effektiva nätverks säkerhets grupp som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="75d9e-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="75d9e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="75d9e-108">Exempel 1: hämta den effektiva nätverks säkerhets gruppen i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="75d9e-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="75d9e-109">Det här kommandot får alla gällande nätverks säkerhets regler som är kopplade till nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="75d9e-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="75d9e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="75d9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d9e-111">-DefaultProfile</span></span>
<span data-ttu-id="75d9e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75d9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d9e-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="75d9e-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="75d9e-114">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="75d9e-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="75d9e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d9e-115">-ResourceGroupName</span></span>
<span data-ttu-id="75d9e-116">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="75d9e-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="75d9e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d9e-117">CommonParameters</span></span>
<span data-ttu-id="75d9e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d9e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d9e-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d9e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d9e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75d9e-120">INPUTS</span></span>

## <span data-ttu-id="75d9e-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75d9e-121">OUTPUTS</span></span>

### <span data-ttu-id="75d9e-122">Microsoft. Azure. commands. Networks. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="75d9e-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="75d9e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75d9e-123">NOTES</span></span>

## <span data-ttu-id="75d9e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75d9e-124">RELATED LINKS</span></span>

[<span data-ttu-id="75d9e-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="75d9e-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


