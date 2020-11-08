---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099490"
---
# <span data-ttu-id="8b0c9-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8b0c9-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="8b0c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b0c9-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0c9-103">Importerar en inställnings fil för en webbplats återställnings valv.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="8b0c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b0c9-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8b0c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b0c9-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0c9-106">Cmdleten **import-AzureSiteRecoveryVaultSettingsFile** importerar en Azure Site Recovery-inställnings fil för att ange valv kontexten för efterföljande webbplats återställnings åtgärder i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="8b0c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b0c9-107">EXAMPLES</span></span>

### <span data-ttu-id="8b0c9-108">Exempel 1: importera en fil för valv inställningar</span><span class="sxs-lookup"><span data-stu-id="8b0c9-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="8b0c9-109">Det här kommandot importerar filen för valv inställningar på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="8b0c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b0c9-110">PARAMETERS</span></span>

### <span data-ttu-id="8b0c9-111">-Path</span><span class="sxs-lookup"><span data-stu-id="8b0c9-111">-Path</span></span>
<span data-ttu-id="8b0c9-112">Anger sökvägen till filen inställningar för valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="8b0c9-113">Den här filen kan hämtas från portalen för webbplats återställnings valv och lagras lokalt.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0c9-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="8b0c9-114">-Profile</span></span>
<span data-ttu-id="8b0c9-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b0c9-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b0c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0c9-117">CommonParameters</span></span>
<span data-ttu-id="8b0c9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0c9-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0c9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0c9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b0c9-120">INPUTS</span></span>

## <span data-ttu-id="8b0c9-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b0c9-121">OUTPUTS</span></span>

## <span data-ttu-id="8b0c9-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b0c9-122">NOTES</span></span>

## <span data-ttu-id="8b0c9-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b0c9-123">RELATED LINKS</span></span>

[<span data-ttu-id="8b0c9-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8b0c9-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="8b0c9-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8b0c9-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


