---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582980"
---
# <span data-ttu-id="d8e6b-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d8e6b-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="d8e6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e6b-103">Hämtar information om Azure Site Recovery-leverantörer i valvet.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8e6b-104">SYNTAX</span></span>

### <span data-ttu-id="d8e6b-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d8e6b-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e6b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d8e6b-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8e6b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8e6b-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8e6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8e6b-108">DESCRIPTION</span></span>
<span data-ttu-id="d8e6b-109">Cmdleten **Get-AzureRmSiteRecoveryServicesProvider** hämtar information om Azure Site Recovery-leverantörer i valvet.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="d8e6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8e6b-110">EXAMPLES</span></span>

## <span data-ttu-id="d8e6b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8e6b-111">PARAMETERS</span></span>

### <span data-ttu-id="d8e6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e6b-112">-DefaultProfile</span></span>
<span data-ttu-id="d8e6b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e6b-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="d8e6b-114">-Fabric</span></span>
<span data-ttu-id="d8e6b-115">Anger ett Fabric-objekt för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e6b-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8e6b-116">-FriendlyName</span></span>
<span data-ttu-id="d8e6b-117">Anger det egna namnet på Azure Site Recovery-providern som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d8e6b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8e6b-118">-Name</span></span>
<span data-ttu-id="d8e6b-119">Anger namnet på Azure Site Recovery-providern som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d8e6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e6b-120">CommonParameters</span></span>
<span data-ttu-id="d8e6b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e6b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e6b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e6b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8e6b-123">INPUTS</span></span>

### <span data-ttu-id="d8e6b-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d8e6b-124">ASRFabric</span></span>
<span data-ttu-id="d8e6b-125">Parametern ' Fabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8e6b-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="d8e6b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8e6b-126">OUTPUTS</span></span>

### <span data-ttu-id="d8e6b-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. commands. SiteRecovery, version = 2.0.1.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8e6b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8e6b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8e6b-128">NOTES</span></span>

## <span data-ttu-id="d8e6b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8e6b-129">RELATED LINKS</span></span>

[<span data-ttu-id="d8e6b-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d8e6b-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="d8e6b-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d8e6b-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)