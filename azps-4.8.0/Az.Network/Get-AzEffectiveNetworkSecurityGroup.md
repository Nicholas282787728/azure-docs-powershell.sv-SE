---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102169"
---
# <span data-ttu-id="4241e-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4241e-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="4241e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4241e-102">SYNOPSIS</span></span>
<span data-ttu-id="4241e-103">Hämtar den effektiva nätverks säkerhets gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4241e-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="4241e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4241e-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4241e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4241e-105">DESCRIPTION</span></span>
<span data-ttu-id="4241e-106">Cmdleten **Get-AzEffectiveNetworkSecurityGroup** returnerar den effektiva nätverks säkerhets grupp som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4241e-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="4241e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4241e-107">EXAMPLES</span></span>

### <span data-ttu-id="4241e-108">Exempel 1: hämta den effektiva nätverks säkerhets gruppen i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="4241e-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="4241e-109">Det här kommandot får alla gällande nätverks säkerhets regler som är kopplade till nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4241e-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="4241e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4241e-110">PARAMETERS</span></span>

### <span data-ttu-id="4241e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4241e-111">-DefaultProfile</span></span>
<span data-ttu-id="4241e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4241e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4241e-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="4241e-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="4241e-114">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4241e-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="4241e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4241e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4241e-116">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4241e-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="4241e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4241e-117">CommonParameters</span></span>
<span data-ttu-id="4241e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4241e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4241e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4241e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4241e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4241e-120">INPUTS</span></span>

### <span data-ttu-id="4241e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4241e-121">System.String</span></span>

## <span data-ttu-id="4241e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4241e-122">OUTPUTS</span></span>

### <span data-ttu-id="4241e-123">Microsoft. Azure. commands. Networks. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4241e-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="4241e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4241e-124">NOTES</span></span>

## <span data-ttu-id="4241e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4241e-125">RELATED LINKS</span></span>

[<span data-ttu-id="4241e-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4241e-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


