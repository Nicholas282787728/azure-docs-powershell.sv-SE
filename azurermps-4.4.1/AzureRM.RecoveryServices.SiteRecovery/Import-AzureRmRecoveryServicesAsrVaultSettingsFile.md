---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755655"
---
# <span data-ttu-id="fda4c-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fda4c-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="fda4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fda4c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda4c-103">Importerar den angivna inställnings filen för ASR-valvet för att ange valv kontexten (PowerShell-arbetspass) för efterföljande ASR-åtgärder i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="fda4c-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fda4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fda4c-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fda4c-105">DESCRIPTION</span></span>
<span data-ttu-id="fda4c-106">Cmdleten **import-AzureRmRecoveryServicesAsrVaultSettingsFile** importerar inställnings filen för Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="fda4c-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="fda4c-107">Valv inställnings filen används för att ange valv kontexten för efterföljande Azure Site Recovery-operationer i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="fda4c-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="fda4c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fda4c-108">EXAMPLES</span></span>

### <span data-ttu-id="fda4c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fda4c-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="fda4c-110">Importerar den angivna inställnings filen för Recovery Services-valvet och returnerar inställningarna för det importerade valvet.</span><span class="sxs-lookup"><span data-stu-id="fda4c-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="fda4c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fda4c-111">PARAMETERS</span></span>

### <span data-ttu-id="fda4c-112">-Path</span><span class="sxs-lookup"><span data-stu-id="fda4c-112">-Path</span></span>
<span data-ttu-id="fda4c-113">Anger sökvägen till filen ASR valv inställningar.</span><span class="sxs-lookup"><span data-stu-id="fda4c-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="fda4c-114">Den här filen kan hämtas från återställnings tjänstens valv Portal och lagras lokalt.</span><span class="sxs-lookup"><span data-stu-id="fda4c-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda4c-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fda4c-115">-Confirm</span></span>
<span data-ttu-id="fda4c-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fda4c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda4c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda4c-117">-WhatIf</span></span>
<span data-ttu-id="fda4c-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fda4c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fda4c-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fda4c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda4c-120">CommonParameters</span></span>
<span data-ttu-id="fda4c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda4c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda4c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda4c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fda4c-123">INPUTS</span></span>

### <span data-ttu-id="fda4c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fda4c-124">System.String</span></span>

## <span data-ttu-id="fda4c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fda4c-125">OUTPUTS</span></span>

### <span data-ttu-id="fda4c-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="fda4c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="fda4c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fda4c-127">NOTES</span></span>

## <span data-ttu-id="fda4c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fda4c-128">RELATED LINKS</span></span>

[<span data-ttu-id="fda4c-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fda4c-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
