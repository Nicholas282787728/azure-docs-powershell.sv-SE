---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756476"
---
# <span data-ttu-id="dce03-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="dce03-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="dce03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dce03-102">SYNOPSIS</span></span>
<span data-ttu-id="dce03-103">Hämtar de tillgängliga (upptäckta) ASR-säkerhetsfunktionerna i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="dce03-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dce03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dce03-104">SYNTAX</span></span>

### <span data-ttu-id="dce03-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="dce03-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dce03-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="dce03-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dce03-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dce03-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce03-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dce03-108">DESCRIPTION</span></span>
<span data-ttu-id="dce03-109">Cmdleten **Get-AzureRmRecoveryServicesAsrStorageClassification** hämtar information om de UPPTÄCKta ASR-lagrings klassificeringarna i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="dce03-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="dce03-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dce03-110">EXAMPLES</span></span>

### <span data-ttu-id="dce03-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dce03-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="dce03-112">Lista över upptäckta lagrings klassificeringar som motsvarar den angivna ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="dce03-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="dce03-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dce03-113">PARAMETERS</span></span>

### <span data-ttu-id="dce03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce03-114">-DefaultProfile</span></span>
<span data-ttu-id="dce03-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dce03-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="dce03-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="dce03-116">-Fabric</span></span>
<span data-ttu-id="dce03-117">Anger ett ASR-Fabric-objekt.</span><span class="sxs-lookup"><span data-stu-id="dce03-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="dce03-118">Cmdleten får information om upptäckta lagrings klassificeringar motsvarande den angivna ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="dce03-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="dce03-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dce03-119">-FriendlyName</span></span>
<span data-ttu-id="dce03-120">Anger det egna namnet på det lagrings klassificerings objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dce03-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce03-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="dce03-121">-Name</span></span>
<span data-ttu-id="dce03-122">Anger namnet på det lagrings klassificerings objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dce03-122">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce03-123">CommonParameters</span></span>
<span data-ttu-id="dce03-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce03-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce03-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce03-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dce03-126">INPUTS</span></span>

### <span data-ttu-id="dce03-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="dce03-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="dce03-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dce03-128">OUTPUTS</span></span>

### <span data-ttu-id="dce03-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dce03-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dce03-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dce03-130">NOTES</span></span>

## <span data-ttu-id="dce03-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dce03-131">RELATED LINKS</span></span>