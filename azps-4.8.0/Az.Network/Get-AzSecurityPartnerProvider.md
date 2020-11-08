---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258264"
---
# <span data-ttu-id="b4afe-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4afe-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="b4afe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4afe-102">SYNOPSIS</span></span>
<span data-ttu-id="b4afe-103">Skaffa en Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4afe-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="b4afe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4afe-104">SYNTAX</span></span>

### <span data-ttu-id="b4afe-105">SecurityPartnerProviderNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b4afe-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4afe-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4afe-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4afe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4afe-107">DESCRIPTION</span></span>
<span data-ttu-id="b4afe-108">Cmdleten **Get-AzSecurityPartnerProvider** får ett Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4afe-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="b4afe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4afe-109">EXAMPLES</span></span>

### <span data-ttu-id="b4afe-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4afe-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="b4afe-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b4afe-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="b4afe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4afe-112">PARAMETERS</span></span>

### <span data-ttu-id="b4afe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4afe-113">-DefaultProfile</span></span>
<span data-ttu-id="b4afe-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4afe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4afe-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4afe-115">-Name</span></span>
<span data-ttu-id="b4afe-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b4afe-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4afe-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4afe-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b4afe-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4afe-119">-ResourceId</span></span>
<span data-ttu-id="b4afe-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b4afe-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4afe-121">CommonParameters</span></span>
<span data-ttu-id="b4afe-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4afe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4afe-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4afe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4afe-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4afe-124">INPUTS</span></span>

### <span data-ttu-id="b4afe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b4afe-125">System.String</span></span>

## <span data-ttu-id="b4afe-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4afe-126">OUTPUTS</span></span>

### <span data-ttu-id="b4afe-127">Microsoft. Azure. commands. Networks. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b4afe-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="b4afe-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4afe-128">NOTES</span></span>

## <span data-ttu-id="b4afe-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4afe-129">RELATED LINKS</span></span>
