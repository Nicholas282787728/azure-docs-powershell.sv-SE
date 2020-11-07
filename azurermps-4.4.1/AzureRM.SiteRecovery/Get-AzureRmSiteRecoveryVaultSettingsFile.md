---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757743"
---
# <span data-ttu-id="45780-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="45780-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="45780-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45780-102">SYNOPSIS</span></span>
<span data-ttu-id="45780-103">Hämtar inställnings filen för valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="45780-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45780-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45780-104">SYNTAX</span></span>

### <span data-ttu-id="45780-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="45780-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45780-106">Vis</span><span class="sxs-lookup"><span data-stu-id="45780-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45780-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="45780-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45780-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45780-108">DESCRIPTION</span></span>
<span data-ttu-id="45780-109">Cmdleten **Get-AzureRmSiteRecoveryVaultSettingsFile** hämtar inställnings filen för ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="45780-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="45780-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45780-110">EXAMPLES</span></span>

## <span data-ttu-id="45780-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45780-111">PARAMETERS</span></span>

### <span data-ttu-id="45780-112">-Path</span><span class="sxs-lookup"><span data-stu-id="45780-112">-Path</span></span>
<span data-ttu-id="45780-113">Anger sökvägen till filen inställningar för valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="45780-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="45780-114">Om du vill lagra den här filen lokalt kan du hämta den från webbplatsen Site Recovery-valv när kommandot är slutfört.</span><span class="sxs-lookup"><span data-stu-id="45780-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45780-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="45780-115">-SiteFriendlyName</span></span>
<span data-ttu-id="45780-116">Anger det användarvänliga namnet för valvet när webbplatsen är en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="45780-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45780-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="45780-117">-SiteIdentifier</span></span>
<span data-ttu-id="45780-118">Anger plats identifieraren för valvet när webbplatsen är en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="45780-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45780-119">-Valv</span><span class="sxs-lookup"><span data-stu-id="45780-119">-Vault</span></span>
<span data-ttu-id="45780-120">Anger valv objekt för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="45780-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45780-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45780-121">-DefaultProfile</span></span>
<span data-ttu-id="45780-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45780-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45780-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45780-123">CommonParameters</span></span>
<span data-ttu-id="45780-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45780-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45780-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45780-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45780-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45780-126">INPUTS</span></span>

### <span data-ttu-id="45780-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="45780-127">ASRVault</span></span>
<span data-ttu-id="45780-128">Parametern ' valv ' godkänner värdet av typen ' ASRVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="45780-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="45780-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45780-129">OUTPUTS</span></span>

### <span data-ttu-id="45780-130">Microsoft. Azure. commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="45780-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="45780-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45780-131">NOTES</span></span>

## <span data-ttu-id="45780-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45780-132">RELATED LINKS</span></span>

[<span data-ttu-id="45780-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="45780-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="45780-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="45780-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
