---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576231"
---
# <span data-ttu-id="d105c-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d105c-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="d105c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d105c-102">SYNOPSIS</span></span>
<span data-ttu-id="d105c-103">Hämtar en virtuell WAN-eller alla virtuella WAN-nätverk i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d105c-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d105c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d105c-104">SYNTAX</span></span>

### <span data-ttu-id="d105c-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="d105c-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d105c-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d105c-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d105c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d105c-107">DESCRIPTION</span></span>
<span data-ttu-id="d105c-108">Hämtar en virtuell WAN-eller alla virtuella WAN-nätverk i en resurs grupp eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d105c-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="d105c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d105c-109">EXAMPLES</span></span>

### <span data-ttu-id="d105c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d105c-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="d105c-111">Det här kommandot får den virtuella WAN-myVirtualWAN i testRG för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d105c-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="d105c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d105c-112">PARAMETERS</span></span>

### <span data-ttu-id="d105c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d105c-113">-DefaultProfile</span></span>
<span data-ttu-id="d105c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d105c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d105c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d105c-115">-Name</span></span>
<span data-ttu-id="d105c-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d105c-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d105c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d105c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d105c-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d105c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d105c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d105c-119">CommonParameters</span></span>
<span data-ttu-id="d105c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d105c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d105c-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d105c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d105c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d105c-122">INPUTS</span></span>

### <span data-ttu-id="d105c-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="d105c-123">None</span></span>

## <span data-ttu-id="d105c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d105c-124">OUTPUTS</span></span>

### <span data-ttu-id="d105c-125">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d105c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="d105c-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d105c-126">NOTES</span></span>

## <span data-ttu-id="d105c-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d105c-127">RELATED LINKS</span></span>
