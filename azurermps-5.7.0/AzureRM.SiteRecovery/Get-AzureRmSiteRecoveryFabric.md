---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 63d28696370f5219a4c2a21c6fb3097441a11433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579364"
---
# <span data-ttu-id="e4bdd-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="e4bdd-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="e4bdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bdd-103">Skaffa egenskaperna för en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4bdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4bdd-104">SYNTAX</span></span>

### <span data-ttu-id="e4bdd-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="e4bdd-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4bdd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e4bdd-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4bdd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e4bdd-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4bdd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4bdd-108">DESCRIPTION</span></span>
<span data-ttu-id="e4bdd-109">Cmdleten **Get-AzureRmSiteRecoveryFabric** hämtar egenskaperna för en angiven Azure Site Recovery-infrastruktur eller alla Azure Site Recovery-Fabric i ett valv för återhämtnings tjänst.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="e4bdd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4bdd-110">EXAMPLES</span></span>

## <span data-ttu-id="e4bdd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4bdd-111">PARAMETERS</span></span>

### <span data-ttu-id="e4bdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bdd-112">-DefaultProfile</span></span>
<span data-ttu-id="e4bdd-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4bdd-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e4bdd-114">-FriendlyName</span></span>
<span data-ttu-id="e4bdd-115">Anger det egna namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-115">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bdd-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4bdd-116">-Name</span></span>
<span data-ttu-id="e4bdd-117">Anger namnet på Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-117">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bdd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bdd-118">CommonParameters</span></span>
<span data-ttu-id="e4bdd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bdd-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bdd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bdd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4bdd-121">INPUTS</span></span>

### <span data-ttu-id="e4bdd-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="e4bdd-122">None</span></span>
<span data-ttu-id="e4bdd-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e4bdd-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4bdd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4bdd-124">OUTPUTS</span></span>

### <span data-ttu-id="e4bdd-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRFabric, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e4bdd-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e4bdd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4bdd-126">NOTES</span></span>

## <span data-ttu-id="e4bdd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4bdd-127">RELATED LINKS</span></span>

[<span data-ttu-id="e4bdd-128">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="e4bdd-128">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="e4bdd-129">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="e4bdd-129">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
