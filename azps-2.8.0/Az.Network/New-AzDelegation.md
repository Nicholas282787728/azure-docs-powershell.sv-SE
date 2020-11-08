---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 32398b235ef28872730f5839cef52023fe0f4ee9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918638"
---
# <span data-ttu-id="26992-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="26992-101">New-AzDelegation</span></span>

## <span data-ttu-id="26992-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26992-102">SYNOPSIS</span></span>
<span data-ttu-id="26992-103">Skapar en tjänst delegering.</span><span class="sxs-lookup"><span data-stu-id="26992-103">Creates a service delegation.</span></span>

## <span data-ttu-id="26992-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26992-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26992-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26992-105">DESCRIPTION</span></span>
<span data-ttu-id="26992-106">Cmdleten **New-AzDelegation** skapar en tjänst delegering som kan läggas till i ett undernät.</span><span class="sxs-lookup"><span data-stu-id="26992-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="26992-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26992-107">EXAMPLES</span></span>

### <span data-ttu-id="26992-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26992-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="26992-109">Den första cmdleten skapar en delegering som kan läggas till i ett undernät och det lagrar den i $delegation variabeln.</span><span class="sxs-lookup"><span data-stu-id="26992-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="26992-110">Den andra och tredje cmdleten hämtar under nätet som ska delegeras.</span><span class="sxs-lookup"><span data-stu-id="26992-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="26992-111">Den fjärde cmdleten lägger till den skapade delegeringen till under nätet av intresse och den sista cmdleten skickar den uppdaterade konfigurationen till servern.</span><span class="sxs-lookup"><span data-stu-id="26992-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="26992-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26992-112">PARAMETERS</span></span>

### <span data-ttu-id="26992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26992-113">-DefaultProfile</span></span>
<span data-ttu-id="26992-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26992-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26992-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="26992-115">-Name</span></span>
<span data-ttu-id="26992-116">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="26992-116">The name of the delegation</span></span>

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

### <span data-ttu-id="26992-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="26992-117">-ServiceName</span></span>
<span data-ttu-id="26992-118">Namnet på tjänsten som under nätet ska delegeras till</span><span class="sxs-lookup"><span data-stu-id="26992-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="26992-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26992-119">CommonParameters</span></span>
<span data-ttu-id="26992-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26992-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26992-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26992-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26992-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26992-122">INPUTS</span></span>

### <span data-ttu-id="26992-123">System. String</span><span class="sxs-lookup"><span data-stu-id="26992-123">System.String</span></span>

## <span data-ttu-id="26992-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26992-124">OUTPUTS</span></span>

### <span data-ttu-id="26992-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="26992-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="26992-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26992-126">NOTES</span></span>

## <span data-ttu-id="26992-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26992-127">RELATED LINKS</span></span>

<span data-ttu-id="26992-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="26992-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>