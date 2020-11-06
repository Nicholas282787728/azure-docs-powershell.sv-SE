---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: dc9934aaee7706e3577039bdb77c5a6a54c29c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581111"
---
# <span data-ttu-id="06fcc-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="06fcc-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="06fcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="06fcc-103">Hämtar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="06fcc-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06fcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06fcc-104">SYNTAX</span></span>

### <span data-ttu-id="06fcc-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="06fcc-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06fcc-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="06fcc-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06fcc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="06fcc-108">Cmdleten **Get-AzureRmNetworkSecurityGroup** får en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="06fcc-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="06fcc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="06fcc-110">1: Hämta en befintlig nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="06fcc-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="06fcc-111">Det här kommandot returnerar innehållet i Azure nätverks säkerhets gruppen "nsg1" i resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="06fcc-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="06fcc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06fcc-112">PARAMETERS</span></span>

### <span data-ttu-id="06fcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fcc-113">-DefaultProfile</span></span>
<span data-ttu-id="06fcc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06fcc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06fcc-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="06fcc-115">-ExpandResource</span></span>
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

### <span data-ttu-id="06fcc-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="06fcc-116">-Name</span></span>
<span data-ttu-id="06fcc-117">Anger namnet på den nätverks säkerhets grupp som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="06fcc-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06fcc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fcc-118">-ResourceGroupName</span></span>
<span data-ttu-id="06fcc-119">Anger namnet på den resurs grupp som nätverks säkerhets gruppen tillhör.</span><span class="sxs-lookup"><span data-stu-id="06fcc-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="06fcc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fcc-120">CommonParameters</span></span>
<span data-ttu-id="06fcc-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fcc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fcc-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fcc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fcc-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06fcc-123">INPUTS</span></span>

### <span data-ttu-id="06fcc-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="06fcc-124">None</span></span>
<span data-ttu-id="06fcc-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="06fcc-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06fcc-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06fcc-126">OUTPUTS</span></span>

### <span data-ttu-id="06fcc-127">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="06fcc-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="06fcc-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06fcc-128">NOTES</span></span>

## <span data-ttu-id="06fcc-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06fcc-129">RELATED LINKS</span></span>

[<span data-ttu-id="06fcc-130">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="06fcc-130">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="06fcc-131">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="06fcc-131">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="06fcc-132">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="06fcc-132">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


