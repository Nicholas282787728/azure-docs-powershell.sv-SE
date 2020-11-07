---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756244"
---
# <span data-ttu-id="d2e18-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2e18-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="d2e18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2e18-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e18-103">Hämtar den effektiva nätverks säkerhets gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d2e18-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2e18-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e18-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2e18-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e18-106">Cmdleten **Get-AzureRmEffectiveNetworkSecurityGroup** returnerar den effektiva nätverks säkerhets grupp som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d2e18-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="d2e18-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2e18-107">EXAMPLES</span></span>

### <span data-ttu-id="d2e18-108">Exempel 1: hämta den effektiva nätverks säkerhets gruppen i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d2e18-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d2e18-109">Det här kommandot får alla gällande nätverks säkerhets regler som är kopplade till nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d2e18-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="d2e18-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2e18-110">PARAMETERS</span></span>

### <span data-ttu-id="d2e18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e18-111">-DefaultProfile</span></span>
<span data-ttu-id="d2e18-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e18-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="d2e18-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="d2e18-114">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d2e18-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="d2e18-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e18-115">-ResourceGroupName</span></span>
<span data-ttu-id="d2e18-116">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d2e18-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="d2e18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e18-117">CommonParameters</span></span>
<span data-ttu-id="d2e18-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e18-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e18-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e18-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2e18-120">INPUTS</span></span>

### <span data-ttu-id="d2e18-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="d2e18-121">None</span></span>
<span data-ttu-id="d2e18-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d2e18-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2e18-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2e18-123">OUTPUTS</span></span>

### <span data-ttu-id="d2e18-124">Microsoft. Azure. commands. Networks. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2e18-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="d2e18-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2e18-125">NOTES</span></span>

## <span data-ttu-id="d2e18-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2e18-126">RELATED LINKS</span></span>

[<span data-ttu-id="d2e18-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2e18-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


