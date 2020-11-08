---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258052"
---
# <span data-ttu-id="8fc68-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8fc68-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="8fc68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fc68-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc68-103">Hämtar de tillgängliga (upptäckta) ASR-säkerhetsfunktionerna i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8fc68-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="8fc68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fc68-104">SYNTAX</span></span>

### <span data-ttu-id="8fc68-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="8fc68-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fc68-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8fc68-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fc68-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8fc68-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fc68-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fc68-108">DESCRIPTION</span></span>
<span data-ttu-id="8fc68-109">Cmdleten **Get-AzRecoveryServicesAsrStorageClassification** hämtar information om de UPPTÄCKta ASR-lagrings klassificeringarna i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8fc68-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="8fc68-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fc68-110">EXAMPLES</span></span>

### <span data-ttu-id="8fc68-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8fc68-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="8fc68-112">Lista över upptäckta lagrings klassificeringar som motsvarar den angivna ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="8fc68-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="8fc68-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fc68-113">PARAMETERS</span></span>

### <span data-ttu-id="8fc68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc68-114">-DefaultProfile</span></span>
<span data-ttu-id="8fc68-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc68-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8fc68-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="8fc68-116">-Fabric</span></span>
<span data-ttu-id="8fc68-117">Anger ett ASR-Fabric-objekt.</span><span class="sxs-lookup"><span data-stu-id="8fc68-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="8fc68-118">Cmdleten får information om upptäckta lagrings klassificeringar motsvarande den angivna ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="8fc68-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc68-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8fc68-119">-FriendlyName</span></span>
<span data-ttu-id="8fc68-120">Anger det egna namnet på det lagrings klassificerings objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="8fc68-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc68-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8fc68-121">-Name</span></span>
<span data-ttu-id="8fc68-122">Anger namnet på det lagrings klassificerings objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="8fc68-122">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc68-123">CommonParameters</span></span>
<span data-ttu-id="8fc68-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc68-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fc68-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc68-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fc68-126">INPUTS</span></span>

### <span data-ttu-id="8fc68-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8fc68-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8fc68-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fc68-128">OUTPUTS</span></span>

### <span data-ttu-id="8fc68-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8fc68-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="8fc68-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fc68-130">NOTES</span></span>

## <span data-ttu-id="8fc68-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fc68-131">RELATED LINKS</span></span>
