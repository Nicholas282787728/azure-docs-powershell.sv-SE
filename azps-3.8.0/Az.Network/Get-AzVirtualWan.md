---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090991"
---
# <span data-ttu-id="516ad-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="516ad-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="516ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="516ad-102">SYNOPSIS</span></span>
<span data-ttu-id="516ad-103">Hämtar en virtuell WAN-eller alla virtuella WAN-nätverk i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="516ad-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="516ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="516ad-104">SYNTAX</span></span>

### <span data-ttu-id="516ad-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="516ad-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="516ad-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516ad-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="516ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="516ad-107">DESCRIPTION</span></span>
<span data-ttu-id="516ad-108">Hämtar en virtuell WAN-eller alla virtuella WAN-nätverk i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="516ad-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="516ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="516ad-109">EXAMPLES</span></span>

### <span data-ttu-id="516ad-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="516ad-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="516ad-111">Det här kommandot får den virtuella WAN-myVirtualWAN i testRG för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="516ad-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="516ad-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="516ad-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="516ad-113">Det här kommandot får alla virtuella WAN-nätbörjar med "test".</span><span class="sxs-lookup"><span data-stu-id="516ad-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="516ad-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="516ad-114">PARAMETERS</span></span>

### <span data-ttu-id="516ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516ad-115">-DefaultProfile</span></span>
<span data-ttu-id="516ad-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="516ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="516ad-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="516ad-117">-Name</span></span>
<span data-ttu-id="516ad-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="516ad-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="516ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="516ad-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="516ad-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="516ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516ad-121">CommonParameters</span></span>
<span data-ttu-id="516ad-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516ad-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="516ad-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516ad-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="516ad-124">INPUTS</span></span>

### <span data-ttu-id="516ad-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="516ad-125">None</span></span>

## <span data-ttu-id="516ad-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="516ad-126">OUTPUTS</span></span>

### <span data-ttu-id="516ad-127">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="516ad-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="516ad-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="516ad-128">NOTES</span></span>

## <span data-ttu-id="516ad-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="516ad-129">RELATED LINKS</span></span>

[<span data-ttu-id="516ad-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="516ad-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="516ad-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="516ad-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="516ad-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="516ad-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
