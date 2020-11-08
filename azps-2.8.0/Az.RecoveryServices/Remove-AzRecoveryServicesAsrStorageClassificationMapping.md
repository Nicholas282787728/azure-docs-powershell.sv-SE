---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920199"
---
# <span data-ttu-id="04a35-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="04a35-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="04a35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04a35-102">SYNOPSIS</span></span>
<span data-ttu-id="04a35-103">Tar bort den angivna mappningen för ASR-lagringsenheten.</span><span class="sxs-lookup"><span data-stu-id="04a35-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="04a35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04a35-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a35-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04a35-105">DESCRIPTION</span></span>
<span data-ttu-id="04a35-106">Cmdleten **Remove-AzRecoveryServicesAsrStorageClassificationMapping** tar bort den angivna klassificerings mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04a35-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="04a35-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04a35-107">EXAMPLES</span></span>

### <span data-ttu-id="04a35-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04a35-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="04a35-109">Påbörjar borttagning av angiven mappning av lagrings klassificering och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="04a35-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="04a35-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04a35-110">PARAMETERS</span></span>

### <span data-ttu-id="04a35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a35-111">-DefaultProfile</span></span>
<span data-ttu-id="04a35-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04a35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="04a35-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04a35-113">-InputObject</span></span>
<span data-ttu-id="04a35-114">Indatavärdet till cmdleten: mappnings objekt för ASR-filklassificering som motsvarar mappnings klassificeringen för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="04a35-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04a35-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04a35-115">-Confirm</span></span>
<span data-ttu-id="04a35-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04a35-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a35-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a35-117">-WhatIf</span></span>
<span data-ttu-id="04a35-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04a35-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04a35-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04a35-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a35-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a35-120">CommonParameters</span></span>
<span data-ttu-id="04a35-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a35-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a35-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a35-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a35-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04a35-123">INPUTS</span></span>

### <span data-ttu-id="04a35-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="04a35-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="04a35-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04a35-125">OUTPUTS</span></span>

### <span data-ttu-id="04a35-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="04a35-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="04a35-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04a35-127">NOTES</span></span>

## <span data-ttu-id="04a35-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04a35-128">RELATED LINKS</span></span>

[<span data-ttu-id="04a35-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="04a35-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="04a35-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="04a35-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)