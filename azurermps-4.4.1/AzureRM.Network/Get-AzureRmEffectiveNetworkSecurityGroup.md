---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: d479c66b899637f2dc12061b7499fc65b7d59d66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578400"
---
# <span data-ttu-id="91665-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91665-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="91665-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91665-102">SYNOPSIS</span></span>
<span data-ttu-id="91665-103">Hämtar den effektiva nätverks säkerhets gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="91665-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91665-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91665-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91665-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91665-105">DESCRIPTION</span></span>
<span data-ttu-id="91665-106">Cmdleten **Get-AzureRmEffectiveNetworkSecurityGroup** returnerar den effektiva nätverks säkerhets grupp som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="91665-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="91665-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91665-107">EXAMPLES</span></span>

### <span data-ttu-id="91665-108">Exempel 1: hämta den effektiva nätverks säkerhets gruppen i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="91665-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="91665-109">Det här kommandot får alla gällande nätverks säkerhets regler som är kopplade till nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91665-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="91665-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91665-110">PARAMETERS</span></span>

### <span data-ttu-id="91665-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="91665-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="91665-112">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="91665-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="91665-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91665-113">-ResourceGroupName</span></span>
<span data-ttu-id="91665-114">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="91665-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="91665-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91665-115">-DefaultProfile</span></span>
<span data-ttu-id="91665-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91665-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91665-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91665-117">CommonParameters</span></span>
<span data-ttu-id="91665-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91665-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91665-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91665-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91665-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91665-120">INPUTS</span></span>

## <span data-ttu-id="91665-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91665-121">OUTPUTS</span></span>

### <span data-ttu-id="91665-122">Microsoft. Azure. commands. Networks. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91665-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="91665-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91665-123">NOTES</span></span>

## <span data-ttu-id="91665-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91665-124">RELATED LINKS</span></span>

[<span data-ttu-id="91665-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="91665-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


