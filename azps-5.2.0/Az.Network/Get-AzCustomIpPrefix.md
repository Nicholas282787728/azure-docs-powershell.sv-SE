---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387663"
---
# <span data-ttu-id="2a3a0-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a3a0-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="2a3a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3a0-103">Får en CustomIpPrefix-resurs</span><span class="sxs-lookup"><span data-stu-id="2a3a0-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="2a3a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a3a0-104">SYNTAX</span></span>

### <span data-ttu-id="2a3a0-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2a3a0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a3a0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a3a0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a3a0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a3a0-107">DESCRIPTION</span></span>
<span data-ttu-id="2a3a0-108">Cmdleten **Get-AzCustomIpPrefix** hämtar en eller flera CustomIpPrefixes med angiven parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="2a3a0-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="2a3a0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a3a0-109">EXAMPLES</span></span>

### <span data-ttu-id="2a3a0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a3a0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="2a3a0-111">Det här kommandot får en CustomIpPrefix-resurs som heter myCustomIpPrefix i resurs gruppen myRg</span><span class="sxs-lookup"><span data-stu-id="2a3a0-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="2a3a0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a3a0-112">PARAMETERS</span></span>

### <span data-ttu-id="2a3a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3a0-113">-DefaultProfile</span></span>
<span data-ttu-id="2a3a0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a3a0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a3a0-115">-Name</span></span>
<span data-ttu-id="2a3a0-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2a3a0-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a3a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a3a0-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2a3a0-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3a0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a3a0-119">-ResourceId</span></span>
<span data-ttu-id="2a3a0-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2a3a0-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3a0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3a0-121">CommonParameters</span></span>
<span data-ttu-id="2a3a0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3a0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3a0-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a3a0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3a0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a3a0-124">INPUTS</span></span>

### <span data-ttu-id="2a3a0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2a3a0-125">System.String</span></span>

## <span data-ttu-id="2a3a0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a3a0-126">OUTPUTS</span></span>

### <span data-ttu-id="2a3a0-127">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a3a0-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="2a3a0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a3a0-128">NOTES</span></span>

## <span data-ttu-id="2a3a0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a3a0-129">RELATED LINKS</span></span>

[<span data-ttu-id="2a3a0-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a3a0-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="2a3a0-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a3a0-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="2a3a0-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2a3a0-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)