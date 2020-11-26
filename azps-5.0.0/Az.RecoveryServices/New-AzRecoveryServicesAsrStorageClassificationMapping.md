---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270917"
---
# <span data-ttu-id="ddc05-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ddc05-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ddc05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddc05-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc05-103">Skapar en mappnings klassificering för automatisk lagring i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ddc05-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="ddc05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddc05-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddc05-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc05-106">Cmdleten **New-AzRecoveryServicesAsrStorageClassificationMapping** skapar en mappning för lagrings klassificering till Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ddc05-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="ddc05-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddc05-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc05-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddc05-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="ddc05-109">Startar åtgärden för att skapa lagrings klassificering med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ddc05-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ddc05-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddc05-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc05-111">-DefaultProfile</span></span>
<span data-ttu-id="ddc05-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc05-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ddc05-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddc05-113">-Name</span></span>
<span data-ttu-id="ddc05-114">Anger ett namn för mappning av lagrings klassificering för automatisk återställning.</span><span class="sxs-lookup"><span data-stu-id="ddc05-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc05-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ddc05-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="ddc05-116">Anger primärt objekt för automatisk ASR för mappningen.</span><span class="sxs-lookup"><span data-stu-id="ddc05-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="ddc05-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ddc05-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="ddc05-118">Anger det omställnings objekt för automatisk återställning för mappningen.</span><span class="sxs-lookup"><span data-stu-id="ddc05-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc05-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddc05-119">-Confirm</span></span>
<span data-ttu-id="ddc05-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddc05-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc05-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc05-121">-WhatIf</span></span>
<span data-ttu-id="ddc05-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddc05-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddc05-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddc05-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc05-124">CommonParameters</span></span>
<span data-ttu-id="ddc05-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc05-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddc05-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc05-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddc05-127">INPUTS</span></span>

### <span data-ttu-id="ddc05-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ddc05-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="ddc05-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddc05-129">OUTPUTS</span></span>

### <span data-ttu-id="ddc05-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ddc05-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ddc05-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddc05-131">NOTES</span></span>

## <span data-ttu-id="ddc05-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddc05-132">RELATED LINKS</span></span>

[<span data-ttu-id="ddc05-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ddc05-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ddc05-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ddc05-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)