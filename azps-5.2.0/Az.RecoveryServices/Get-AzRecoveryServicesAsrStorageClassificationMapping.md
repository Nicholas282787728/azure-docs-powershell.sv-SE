---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406163"
---
# <span data-ttu-id="ba623-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ba623-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ba623-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba623-102">SYNOPSIS</span></span>
<span data-ttu-id="ba623-103">Hämtar klassificeringar av lagrings plats för automatisk förvaring.</span><span class="sxs-lookup"><span data-stu-id="ba623-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="ba623-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba623-104">SYNTAX</span></span>

### <span data-ttu-id="ba623-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="ba623-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba623-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ba623-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba623-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba623-107">DESCRIPTION</span></span>
<span data-ttu-id="ba623-108">Cmdleten **Get-AzRecoveryServicesAsrStorageClassificationMapping** innehåller information om en klassificerings mappning för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="ba623-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="ba623-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba623-109">EXAMPLES</span></span>

### <span data-ttu-id="ba623-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ba623-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="ba623-111">Visa alla lagrings klassificerings mappningar som motsvarar den angivna lagrings klassificeringen.</span><span class="sxs-lookup"><span data-stu-id="ba623-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="ba623-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba623-112">PARAMETERS</span></span>

### <span data-ttu-id="ba623-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba623-113">-DefaultProfile</span></span>
<span data-ttu-id="ba623-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba623-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ba623-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba623-115">-Name</span></span>
<span data-ttu-id="ba623-116">Anger namnet på den mappning för lagrings klassificering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ba623-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="ba623-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="ba623-117">-StorageClassification</span></span>
<span data-ttu-id="ba623-118">Anger ett objekt för lagrings klassificering för ASR.</span><span class="sxs-lookup"><span data-stu-id="ba623-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="ba623-119">Cmdleten hämtar klassificerings mappningar för automatisk lagring som motsvarar den angivna lagrings klassificeringen</span><span class="sxs-lookup"><span data-stu-id="ba623-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="ba623-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba623-120">CommonParameters</span></span>
<span data-ttu-id="ba623-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba623-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba623-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba623-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba623-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba623-123">INPUTS</span></span>

### <span data-ttu-id="ba623-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ba623-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="ba623-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba623-125">OUTPUTS</span></span>

### <span data-ttu-id="ba623-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ba623-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="ba623-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba623-127">NOTES</span></span>

## <span data-ttu-id="ba623-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba623-128">RELATED LINKS</span></span>

[<span data-ttu-id="ba623-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ba623-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ba623-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ba623-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
