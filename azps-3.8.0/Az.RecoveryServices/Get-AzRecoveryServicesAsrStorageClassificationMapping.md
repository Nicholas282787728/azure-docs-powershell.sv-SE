---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088331"
---
# <span data-ttu-id="ef87d-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ef87d-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ef87d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef87d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef87d-103">Hämtar klassificeringar av lagrings plats för automatisk förvaring.</span><span class="sxs-lookup"><span data-stu-id="ef87d-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="ef87d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef87d-104">SYNTAX</span></span>

### <span data-ttu-id="ef87d-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="ef87d-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef87d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ef87d-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef87d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef87d-107">DESCRIPTION</span></span>
<span data-ttu-id="ef87d-108">Cmdleten **Get-AzRecoveryServicesAsrStorageClassificationMapping** innehåller information om en klassificerings mappning för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="ef87d-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="ef87d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef87d-109">EXAMPLES</span></span>

### <span data-ttu-id="ef87d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef87d-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="ef87d-111">Visa alla lagrings klassificerings mappningar som motsvarar den angivna lagrings klassificeringen.</span><span class="sxs-lookup"><span data-stu-id="ef87d-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="ef87d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef87d-112">PARAMETERS</span></span>

### <span data-ttu-id="ef87d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef87d-113">-DefaultProfile</span></span>
<span data-ttu-id="ef87d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef87d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ef87d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef87d-115">-Name</span></span>
<span data-ttu-id="ef87d-116">Anger namnet på den mappning för lagrings klassificering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ef87d-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="ef87d-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="ef87d-117">-StorageClassification</span></span>
<span data-ttu-id="ef87d-118">Anger ett objekt för lagrings klassificering för ASR.</span><span class="sxs-lookup"><span data-stu-id="ef87d-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="ef87d-119">Cmdleten hämtar klassificerings mappningar för automatisk lagring som motsvarar den angivna lagrings klassificeringen</span><span class="sxs-lookup"><span data-stu-id="ef87d-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef87d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef87d-120">CommonParameters</span></span>
<span data-ttu-id="ef87d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef87d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef87d-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef87d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef87d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef87d-123">INPUTS</span></span>

### <span data-ttu-id="ef87d-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ef87d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="ef87d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef87d-125">OUTPUTS</span></span>

### <span data-ttu-id="ef87d-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ef87d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="ef87d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef87d-127">NOTES</span></span>

## <span data-ttu-id="ef87d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef87d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ef87d-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ef87d-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ef87d-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ef87d-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
