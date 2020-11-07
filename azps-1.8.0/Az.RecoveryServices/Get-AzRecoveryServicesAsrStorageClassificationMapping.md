---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: a341e634c9c426843b5eb217c2f13102abc30ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747444"
---
# <span data-ttu-id="5945a-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5945a-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="5945a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5945a-102">SYNOPSIS</span></span>
<span data-ttu-id="5945a-103">Hämtar klassificeringar av lagrings plats för automatisk förvaring.</span><span class="sxs-lookup"><span data-stu-id="5945a-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="5945a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5945a-104">SYNTAX</span></span>

### <span data-ttu-id="5945a-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="5945a-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5945a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="5945a-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5945a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5945a-107">DESCRIPTION</span></span>
<span data-ttu-id="5945a-108">Cmdleten **Get-AzRecoveryServicesAsrStorageClassificationMapping** innehåller information om en klassificerings mappning för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="5945a-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="5945a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5945a-109">EXAMPLES</span></span>

### <span data-ttu-id="5945a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5945a-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="5945a-111">Visa alla lagrings klassificerings mappningar som motsvarar den angivna lagrings klassificeringen.</span><span class="sxs-lookup"><span data-stu-id="5945a-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="5945a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5945a-112">PARAMETERS</span></span>

### <span data-ttu-id="5945a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5945a-113">-DefaultProfile</span></span>
<span data-ttu-id="5945a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5945a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5945a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5945a-115">-Name</span></span>
<span data-ttu-id="5945a-116">Anger namnet på den mappning för lagrings klassificering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5945a-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="5945a-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="5945a-117">-StorageClassification</span></span>
<span data-ttu-id="5945a-118">Anger ett objekt för lagrings klassificering för ASR.</span><span class="sxs-lookup"><span data-stu-id="5945a-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="5945a-119">Cmdleten hämtar klassificerings mappningar för automatisk lagring som motsvarar den angivna lagrings klassificeringen</span><span class="sxs-lookup"><span data-stu-id="5945a-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="5945a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5945a-120">CommonParameters</span></span>
<span data-ttu-id="5945a-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5945a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5945a-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5945a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5945a-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5945a-123">INPUTS</span></span>

### <span data-ttu-id="5945a-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5945a-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="5945a-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5945a-125">OUTPUTS</span></span>

### <span data-ttu-id="5945a-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5945a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="5945a-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5945a-127">NOTES</span></span>

## <span data-ttu-id="5945a-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5945a-128">RELATED LINKS</span></span>

[<span data-ttu-id="5945a-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5945a-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="5945a-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5945a-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
