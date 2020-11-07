---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755702"
---
# <span data-ttu-id="dcf4c-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="dcf4c-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="dcf4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf4c-103">Hämtar ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="dcf4c-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcf4c-104">SYNTAX</span></span>

### <span data-ttu-id="dcf4c-105">Vis</span><span class="sxs-lookup"><span data-stu-id="dcf4c-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf4c-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcf4c-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf4c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcf4c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcf4c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcf4c-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf4c-109">Cmdleten **Get-AzureRmPublicIpPrefix** får ett eller flera offentliga IP-prefix i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="dcf4c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcf4c-110">EXAMPLES</span></span>

### <span data-ttu-id="dcf4c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dcf4c-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="dcf4c-112">Det här kommandot får en offentlig IP-prefixlängd med $prefixName i resurs gruppen $rgName</span><span class="sxs-lookup"><span data-stu-id="dcf4c-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="dcf4c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcf4c-113">PARAMETERS</span></span>

### <span data-ttu-id="dcf4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf4c-114">-DefaultProfile</span></span>
<span data-ttu-id="dcf4c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf4c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcf4c-116">-Name</span></span>
<span data-ttu-id="dcf4c-117">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-117">The resource name.</span></span>

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

### <span data-ttu-id="dcf4c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf4c-118">-ResourceGroupName</span></span>
<span data-ttu-id="dcf4c-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf4c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf4c-120">-ResourceId</span></span>
<span data-ttu-id="dcf4c-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-121">The resource Id.</span></span>

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

### <span data-ttu-id="dcf4c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf4c-122">CommonParameters</span></span>
<span data-ttu-id="dcf4c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dcf4c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf4c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf4c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcf4c-125">INPUTS</span></span>

### <span data-ttu-id="dcf4c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf4c-126">System.String</span></span>


## <span data-ttu-id="dcf4c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcf4c-127">OUTPUTS</span></span>

### <span data-ttu-id="dcf4c-128">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="dcf4c-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="dcf4c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcf4c-129">NOTES</span></span>

## <span data-ttu-id="dcf4c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcf4c-130">RELATED LINKS</span></span>
