---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922259"
---
# <span data-ttu-id="e0fa6-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0fa6-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e0fa6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fa6-103">Hämtar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-103">Gets a network security group.</span></span>

## <span data-ttu-id="e0fa6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0fa6-104">SYNTAX</span></span>

### <span data-ttu-id="e0fa6-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="e0fa6-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0fa6-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="e0fa6-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0fa6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0fa6-107">DESCRIPTION</span></span>
<span data-ttu-id="e0fa6-108">Cmdleten **Get-AzNetworkSecurityGroup** får en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="e0fa6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0fa6-109">EXAMPLES</span></span>

### <span data-ttu-id="e0fa6-110">1: Hämta en befintlig nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="e0fa6-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="e0fa6-111">Det här kommandot returnerar innehållet i Azure nätverks säkerhets gruppen "nsg1" i resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="e0fa6-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="e0fa6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0fa6-112">PARAMETERS</span></span>

### <span data-ttu-id="e0fa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fa6-113">-DefaultProfile</span></span>
<span data-ttu-id="e0fa6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0fa6-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e0fa6-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fa6-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0fa6-116">-Name</span></span>
<span data-ttu-id="e0fa6-117">Anger namnet på den nätverks säkerhets grupp som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fa6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0fa6-118">-ResourceGroupName</span></span>
<span data-ttu-id="e0fa6-119">Anger namnet på den resurs grupp som nätverks säkerhets gruppen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fa6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fa6-120">CommonParameters</span></span>
<span data-ttu-id="e0fa6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0fa6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fa6-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0fa6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fa6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0fa6-123">INPUTS</span></span>

## <span data-ttu-id="e0fa6-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0fa6-124">OUTPUTS</span></span>

### <span data-ttu-id="e0fa6-125">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0fa6-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e0fa6-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0fa6-126">NOTES</span></span>

## <span data-ttu-id="e0fa6-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0fa6-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0fa6-128">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0fa6-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e0fa6-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0fa6-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e0fa6-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e0fa6-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


