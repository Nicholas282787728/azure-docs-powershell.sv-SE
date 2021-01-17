---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397731"
---
# <span data-ttu-id="25a3a-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="25a3a-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="25a3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="25a3a-103">Sparar en ändrad IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="25a3a-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="25a3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25a3a-104">SYNTAX</span></span>

### <span data-ttu-id="25a3a-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25a3a-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a3a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25a3a-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a3a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25a3a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25a3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25a3a-108">DESCRIPTION</span></span>
<span data-ttu-id="25a3a-109">Cmdleten **set-AzIpAllocation** uppdaterar en Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="25a3a-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="25a3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25a3a-110">EXAMPLES</span></span>

### <span data-ttu-id="25a3a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25a3a-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="25a3a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25a3a-112">PARAMETERS</span></span>

### <span data-ttu-id="25a3a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25a3a-113">-AsJob</span></span>
<span data-ttu-id="25a3a-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="25a3a-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a3a-115">-DefaultProfile</span></span>
<span data-ttu-id="25a3a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25a3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a3a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25a3a-117">-InputObject</span></span>
<span data-ttu-id="25a3a-118">IpAllocation</span><span class="sxs-lookup"><span data-stu-id="25a3a-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="25a3a-119">-IpAllocationTag</span></span>
<span data-ttu-id="25a3a-120">Tilldelnings flaggorna för IP-tilldelningen</span><span class="sxs-lookup"><span data-stu-id="25a3a-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="25a3a-121">-Name</span></span>
<span data-ttu-id="25a3a-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="25a3a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a3a-123">-ResourceGroupName</span></span>
<span data-ttu-id="25a3a-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="25a3a-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25a3a-125">-ResourceId</span></span>
<span data-ttu-id="25a3a-126">IpAllocation-ID</span><span class="sxs-lookup"><span data-stu-id="25a3a-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="25a3a-127">-Tag</span></span>
<span data-ttu-id="25a3a-128">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="25a3a-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a3a-129">CommonParameters</span></span>
<span data-ttu-id="25a3a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a3a-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25a3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a3a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25a3a-132">INPUTS</span></span>

### <span data-ttu-id="25a3a-133">Microsoft. Azure. commands. Networks. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="25a3a-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="25a3a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25a3a-134">OUTPUTS</span></span>

### <span data-ttu-id="25a3a-135">Microsoft. Azure. commands. Networks. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="25a3a-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="25a3a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25a3a-136">NOTES</span></span>

## <span data-ttu-id="25a3a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25a3a-137">RELATED LINKS</span></span>
