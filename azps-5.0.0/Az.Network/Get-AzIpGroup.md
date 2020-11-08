---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272728"
---
# <span data-ttu-id="06485-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="06485-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="06485-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06485-102">SYNOPSIS</span></span>
<span data-ttu-id="06485-103">Skaffa en Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="06485-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="06485-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06485-104">SYNTAX</span></span>

### <span data-ttu-id="06485-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06485-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06485-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06485-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06485-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06485-107">DESCRIPTION</span></span>
<span data-ttu-id="06485-108">Cmdleten **Get-AzIpGroup** får ett Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="06485-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="06485-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06485-109">EXAMPLES</span></span>

### <span data-ttu-id="06485-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06485-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="06485-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="06485-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="06485-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06485-112">PARAMETERS</span></span>

### <span data-ttu-id="06485-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06485-113">-DefaultProfile</span></span>
<span data-ttu-id="06485-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06485-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06485-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="06485-115">-Name</span></span>
<span data-ttu-id="06485-116">Namnet på ipgroup.</span><span class="sxs-lookup"><span data-stu-id="06485-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06485-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06485-117">-ResourceGroupName</span></span>
<span data-ttu-id="06485-118">Resurs grupps namnet för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="06485-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06485-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06485-119">-ResourceId</span></span>
<span data-ttu-id="06485-120">ResourceId för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="06485-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06485-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06485-121">CommonParameters</span></span>
<span data-ttu-id="06485-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06485-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06485-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06485-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06485-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06485-124">INPUTS</span></span>

### <span data-ttu-id="06485-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06485-125">System.String</span></span>

## <span data-ttu-id="06485-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06485-126">OUTPUTS</span></span>

### <span data-ttu-id="06485-127">Microsoft. Azure. commands. Networks. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="06485-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="06485-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06485-128">NOTES</span></span>

## <span data-ttu-id="06485-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06485-129">RELATED LINKS</span></span>
