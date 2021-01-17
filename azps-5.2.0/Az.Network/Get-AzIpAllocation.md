---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406963"
---
# <span data-ttu-id="22a4c-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="22a4c-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="22a4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="22a4c-103">Får ett Azure-IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="22a4c-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="22a4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22a4c-104">SYNTAX</span></span>

### <span data-ttu-id="22a4c-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22a4c-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22a4c-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="22a4c-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22a4c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22a4c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a4c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22a4c-108">DESCRIPTION</span></span>
<span data-ttu-id="22a4c-109">Cmdleten **Get-AzIpAllocation** får ett Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="22a4c-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="22a4c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22a4c-110">EXAMPLES</span></span>

### <span data-ttu-id="22a4c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22a4c-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="22a4c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22a4c-112">PARAMETERS</span></span>

### <span data-ttu-id="22a4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a4c-113">-DefaultProfile</span></span>
<span data-ttu-id="22a4c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22a4c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22a4c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="22a4c-115">-Name</span></span>
<span data-ttu-id="22a4c-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="22a4c-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="22a4c-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="22a4c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a4c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22a4c-119">-ResourceId</span></span>
<span data-ttu-id="22a4c-120">IpAllocation-ID</span><span class="sxs-lookup"><span data-stu-id="22a4c-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a4c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a4c-121">CommonParameters</span></span>
<span data-ttu-id="22a4c-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a4c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a4c-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22a4c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a4c-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22a4c-124">INPUTS</span></span>

### <span data-ttu-id="22a4c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="22a4c-125">System.String</span></span>

## <span data-ttu-id="22a4c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22a4c-126">OUTPUTS</span></span>

### <span data-ttu-id="22a4c-127">Microsoft. Azure. commands. Networks. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="22a4c-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="22a4c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22a4c-128">NOTES</span></span>

## <span data-ttu-id="22a4c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22a4c-129">RELATED LINKS</span></span>
