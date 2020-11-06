---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582975"
---
# <span data-ttu-id="07e42-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="07e42-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="07e42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07e42-102">SYNOPSIS</span></span>
<span data-ttu-id="07e42-103">Hämtar lagrings klassificeringar i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="07e42-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07e42-104">SYNTAX</span></span>

### <span data-ttu-id="07e42-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="07e42-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e42-106">ByName</span><span class="sxs-lookup"><span data-stu-id="07e42-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07e42-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="07e42-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07e42-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="07e42-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07e42-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="07e42-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07e42-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07e42-110">DESCRIPTION</span></span>
<span data-ttu-id="07e42-111">Cmdleten **Get-AzureRmSiteRecoveryStorageClassification** hämtar lagrings klassificeringar i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="07e42-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="07e42-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07e42-112">EXAMPLES</span></span>

## <span data-ttu-id="07e42-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07e42-113">PARAMETERS</span></span>

### <span data-ttu-id="07e42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e42-114">-DefaultProfile</span></span>
<span data-ttu-id="07e42-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07e42-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e42-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="07e42-116">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e42-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="07e42-117">-FriendlyName</span></span>
<span data-ttu-id="07e42-118">Anger det egna namnet på den lagrings klassificering som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="07e42-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07e42-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="07e42-119">-Name</span></span>
<span data-ttu-id="07e42-120">Anger namnet på den lagrings klassificering som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="07e42-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07e42-121">-Server</span><span class="sxs-lookup"><span data-stu-id="07e42-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e42-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e42-122">CommonParameters</span></span>
<span data-ttu-id="07e42-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e42-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e42-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e42-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e42-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07e42-125">INPUTS</span></span>

### <span data-ttu-id="07e42-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="07e42-126">ASRFabric</span></span>
<span data-ttu-id="07e42-127">Parametern ' Fabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="07e42-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="07e42-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="07e42-128">ASRServer</span></span>
<span data-ttu-id="07e42-129">Parametern ' Server ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="07e42-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="07e42-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07e42-130">OUTPUTS</span></span>

### <span data-ttu-id="07e42-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="07e42-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="07e42-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07e42-132">NOTES</span></span>

## <span data-ttu-id="07e42-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07e42-133">RELATED LINKS</span></span>

