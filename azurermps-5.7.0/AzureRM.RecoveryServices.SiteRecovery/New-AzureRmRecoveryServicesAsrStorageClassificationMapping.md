---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e313b3dd9df76185c1eeaf289e918e1d47ace58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755244"
---
# <span data-ttu-id="8f70d-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f70d-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="8f70d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f70d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f70d-103">Skapar en mappnings klassificering för automatisk lagring i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8f70d-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f70d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f70d-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f70d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f70d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f70d-106">Cmdleten **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** skapar en mappning för lagrings klassificering till Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8f70d-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="8f70d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f70d-107">EXAMPLES</span></span>

### <span data-ttu-id="8f70d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8f70d-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="8f70d-109">Startar åtgärden för att skapa lagrings klassificering med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="8f70d-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8f70d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f70d-110">PARAMETERS</span></span>

### <span data-ttu-id="8f70d-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f70d-111">-Confirm</span></span>
<span data-ttu-id="8f70d-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f70d-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f70d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f70d-113">-DefaultProfile</span></span>
<span data-ttu-id="8f70d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f70d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8f70d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f70d-115">-Name</span></span>
<span data-ttu-id="8f70d-116">Anger ett namn för mappning av lagrings klassificering för automatisk återställning.</span><span class="sxs-lookup"><span data-stu-id="8f70d-116">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f70d-117">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8f70d-117">-PrimaryStorageClassification</span></span>
<span data-ttu-id="8f70d-118">Anger primärt objekt för automatisk ASR för mappningen.</span><span class="sxs-lookup"><span data-stu-id="8f70d-118">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f70d-119">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8f70d-119">-RecoveryStorageClassification</span></span>
<span data-ttu-id="8f70d-120">Anger det omställnings objekt för automatisk återställning för mappningen.</span><span class="sxs-lookup"><span data-stu-id="8f70d-120">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f70d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f70d-121">-WhatIf</span></span>
<span data-ttu-id="8f70d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f70d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f70d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f70d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f70d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f70d-124">CommonParameters</span></span>
<span data-ttu-id="8f70d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f70d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f70d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f70d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f70d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f70d-127">INPUTS</span></span>

### <span data-ttu-id="8f70d-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8f70d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="8f70d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f70d-129">OUTPUTS</span></span>

### <span data-ttu-id="8f70d-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8f70d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8f70d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f70d-131">NOTES</span></span>

## <span data-ttu-id="8f70d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f70d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8f70d-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f70d-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="8f70d-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f70d-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
