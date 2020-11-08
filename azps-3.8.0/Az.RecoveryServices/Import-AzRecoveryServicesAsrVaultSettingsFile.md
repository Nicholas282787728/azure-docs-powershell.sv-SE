---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092438"
---
# <span data-ttu-id="337ff-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="337ff-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="337ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="337ff-102">SYNOPSIS</span></span>
<span data-ttu-id="337ff-103">Importerar den angivna inställnings filen för ASR-valvet för att ange valv kontexten (PowerShell-arbetspass) för efterföljande ASR-åtgärder i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="337ff-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="337ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="337ff-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="337ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="337ff-105">DESCRIPTION</span></span>
<span data-ttu-id="337ff-106">Cmdleten **import-AzRecoveryServicesAsrVaultSettingsFile** importerar inställnings filen för Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="337ff-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="337ff-107">Valv inställnings filen används för att ange valv kontexten för efterföljande Azure Site Recovery-operationer i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="337ff-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="337ff-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="337ff-108">EXAMPLES</span></span>

### <span data-ttu-id="337ff-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="337ff-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="337ff-110">Importerar den angivna inställnings filen för Recovery Services-valvet och returnerar inställningarna för det importerade valvet.</span><span class="sxs-lookup"><span data-stu-id="337ff-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="337ff-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="337ff-111">PARAMETERS</span></span>

### <span data-ttu-id="337ff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337ff-112">-DefaultProfile</span></span>
<span data-ttu-id="337ff-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="337ff-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="337ff-114">-Path</span><span class="sxs-lookup"><span data-stu-id="337ff-114">-Path</span></span>
<span data-ttu-id="337ff-115">Anger mappsökvägen för filen ASR valv inställningar.</span><span class="sxs-lookup"><span data-stu-id="337ff-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="337ff-116">Den här filen kan hämtas från återställnings tjänstens valv Portal och lagras lokalt.</span><span class="sxs-lookup"><span data-stu-id="337ff-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="337ff-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="337ff-117">-Confirm</span></span>
<span data-ttu-id="337ff-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="337ff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="337ff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337ff-119">-WhatIf</span></span>
<span data-ttu-id="337ff-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="337ff-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="337ff-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="337ff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="337ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337ff-122">CommonParameters</span></span>
<span data-ttu-id="337ff-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337ff-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="337ff-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337ff-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="337ff-125">INPUTS</span></span>

### <span data-ttu-id="337ff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="337ff-126">System.String</span></span>

## <span data-ttu-id="337ff-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="337ff-127">OUTPUTS</span></span>

### <span data-ttu-id="337ff-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="337ff-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="337ff-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="337ff-129">NOTES</span></span>

## <span data-ttu-id="337ff-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="337ff-130">RELATED LINKS</span></span>

[<span data-ttu-id="337ff-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="337ff-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
