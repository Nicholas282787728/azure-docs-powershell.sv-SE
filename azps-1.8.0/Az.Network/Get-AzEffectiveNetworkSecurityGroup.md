---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c9dd7695e195386b9dd0921b4a9161a5fb175c6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748335"
---
# <span data-ttu-id="bd755-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bd755-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="bd755-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd755-102">SYNOPSIS</span></span>
<span data-ttu-id="bd755-103">Hämtar den effektiva nätverks säkerhets gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="bd755-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="bd755-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd755-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd755-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd755-105">DESCRIPTION</span></span>
<span data-ttu-id="bd755-106">Cmdleten **Get-AzEffectiveNetworkSecurityGroup** returnerar den effektiva nätverks säkerhets grupp som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="bd755-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="bd755-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd755-107">EXAMPLES</span></span>

### <span data-ttu-id="bd755-108">Exempel 1: hämta den effektiva nätverks säkerhets gruppen i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="bd755-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="bd755-109">Det här kommandot får alla gällande nätverks säkerhets regler som är kopplade till nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bd755-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="bd755-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd755-110">PARAMETERS</span></span>

### <span data-ttu-id="bd755-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd755-111">-DefaultProfile</span></span>
<span data-ttu-id="bd755-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd755-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd755-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="bd755-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="bd755-114">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="bd755-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="bd755-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd755-115">-ResourceGroupName</span></span>
<span data-ttu-id="bd755-116">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="bd755-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="bd755-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd755-117">CommonParameters</span></span>
<span data-ttu-id="bd755-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd755-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd755-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd755-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd755-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd755-120">INPUTS</span></span>

### <span data-ttu-id="bd755-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bd755-121">System.String</span></span>

## <span data-ttu-id="bd755-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd755-122">OUTPUTS</span></span>

### <span data-ttu-id="bd755-123">Microsoft. Azure. commands. Networks. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bd755-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="bd755-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd755-124">NOTES</span></span>

## <span data-ttu-id="bd755-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd755-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd755-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="bd755-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


