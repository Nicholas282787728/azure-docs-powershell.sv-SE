---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416123"
---
# <span data-ttu-id="71ae3-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="71ae3-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="71ae3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="71ae3-103">Hämtar den effektiva nätverks säkerhets gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="71ae3-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="71ae3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71ae3-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71ae3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="71ae3-106">Cmdleten **Get-AzEffectiveNetworkSecurityGroup** returnerar den effektiva nätverks säkerhets grupp som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="71ae3-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="71ae3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="71ae3-108">Exempel 1: hämta den effektiva nätverks säkerhets gruppen i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="71ae3-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="71ae3-109">Det här kommandot får alla gällande nätverks säkerhets regler som är kopplade till nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71ae3-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="71ae3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71ae3-110">PARAMETERS</span></span>

### <span data-ttu-id="71ae3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ae3-111">-DefaultProfile</span></span>
<span data-ttu-id="71ae3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71ae3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ae3-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="71ae3-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="71ae3-114">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="71ae3-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="71ae3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ae3-115">-ResourceGroupName</span></span>
<span data-ttu-id="71ae3-116">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="71ae3-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="71ae3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ae3-117">CommonParameters</span></span>
<span data-ttu-id="71ae3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71ae3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ae3-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71ae3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ae3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71ae3-120">INPUTS</span></span>

### <span data-ttu-id="71ae3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="71ae3-121">System.String</span></span>

## <span data-ttu-id="71ae3-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71ae3-122">OUTPUTS</span></span>

### <span data-ttu-id="71ae3-123">Microsoft. Azure. commands. Networks. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="71ae3-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="71ae3-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71ae3-124">NOTES</span></span>

## <span data-ttu-id="71ae3-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71ae3-125">RELATED LINKS</span></span>

[<span data-ttu-id="71ae3-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="71ae3-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


