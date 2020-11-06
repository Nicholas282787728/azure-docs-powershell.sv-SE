---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: bafa671431c617807fa28e2d4fbfed57236fc6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576813"
---
# <span data-ttu-id="28125-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="28125-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="28125-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28125-102">SYNOPSIS</span></span>
<span data-ttu-id="28125-103">Tar bort den angivna mappningen för ASR-lagringsenheten.</span><span class="sxs-lookup"><span data-stu-id="28125-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28125-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28125-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28125-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28125-105">DESCRIPTION</span></span>
<span data-ttu-id="28125-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** tar bort den angivna klassificerings mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="28125-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="28125-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28125-107">EXAMPLES</span></span>

### <span data-ttu-id="28125-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28125-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="28125-109">Påbörjar borttagning av angiven mappning av lagrings klassificering och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="28125-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28125-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28125-110">PARAMETERS</span></span>

### <span data-ttu-id="28125-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28125-111">-DefaultProfile</span></span>
<span data-ttu-id="28125-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28125-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28125-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28125-113">-InputObject</span></span>
<span data-ttu-id="28125-114">Indatavärdet till cmdleten: mappnings objekt för ASR-filklassificering som motsvarar mappnings klassificeringen för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="28125-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="28125-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28125-115">-Confirm</span></span>
<span data-ttu-id="28125-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28125-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28125-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28125-117">-WhatIf</span></span>
<span data-ttu-id="28125-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28125-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28125-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28125-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28125-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28125-120">CommonParameters</span></span>
<span data-ttu-id="28125-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28125-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28125-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28125-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28125-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28125-123">INPUTS</span></span>

### <span data-ttu-id="28125-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="28125-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="28125-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28125-125">OUTPUTS</span></span>

### <span data-ttu-id="28125-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="28125-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28125-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28125-127">NOTES</span></span>

## <span data-ttu-id="28125-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28125-128">RELATED LINKS</span></span>

[<span data-ttu-id="28125-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="28125-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="28125-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="28125-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
