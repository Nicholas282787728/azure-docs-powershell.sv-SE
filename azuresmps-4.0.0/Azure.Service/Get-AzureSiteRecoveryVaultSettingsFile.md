---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099794"
---
# <span data-ttu-id="fce34-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fce34-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="fce34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fce34-102">SYNOPSIS</span></span>
<span data-ttu-id="fce34-103">Hämtar inställnings filen för valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="fce34-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="fce34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fce34-104">SYNTAX</span></span>

### <span data-ttu-id="fce34-105">ByParam (standard)</span><span class="sxs-lookup"><span data-stu-id="fce34-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fce34-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="fce34-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fce34-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fce34-107">DESCRIPTION</span></span>
<span data-ttu-id="fce34-108">Cmdleten **Get-AzureSiteRecoveryVaultSettingsFile** hämtar inställnings filen för ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="fce34-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fce34-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fce34-109">EXAMPLES</span></span>

### <span data-ttu-id="fce34-110">Exempel 1: Hämta inställnings filen för ett valv</span><span class="sxs-lookup"><span data-stu-id="fce34-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="fce34-111">Det första kommandot får det aktiva Azure Site Recovery-valvet med namnet ContosoVault med hjälp av cmdleten **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="fce34-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="fce34-112">Kommandot lagrar valvet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="fce34-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="fce34-113">Det andra kommandot hämtar inställnings filen för valvet som lagras i $Vault.</span><span class="sxs-lookup"><span data-stu-id="fce34-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="fce34-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fce34-114">PARAMETERS</span></span>

### <span data-ttu-id="fce34-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="fce34-115">-Location</span></span>
<span data-ttu-id="fce34-116">Anger den geografiska plats som valvet tillhör.</span><span class="sxs-lookup"><span data-stu-id="fce34-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="fce34-117">-Name</span></span>
<span data-ttu-id="fce34-118">Anger namnet på ett valv.</span><span class="sxs-lookup"><span data-stu-id="fce34-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-119">-Path</span><span class="sxs-lookup"><span data-stu-id="fce34-119">-Path</span></span>
<span data-ttu-id="fce34-120">Anger sökvägen till filen inställningar för valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="fce34-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="fce34-121">Om du vill lagra den här filen lokalt kan du hämta den från webbplatsen Site Recovery Vault när kommandot har körts klart.</span><span class="sxs-lookup"><span data-stu-id="fce34-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="fce34-122">-Profile</span></span>
<span data-ttu-id="fce34-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fce34-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fce34-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fce34-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fce34-125">-Site</span><span class="sxs-lookup"><span data-stu-id="fce34-125">-Site</span></span>
<span data-ttu-id="fce34-126">Anger en webbplats där en inställnings fil ska visas.</span><span class="sxs-lookup"><span data-stu-id="fce34-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="fce34-127">Använd cmdleten **Get-AzureSiteRecoverySite** för att få ett **plats** objekt.</span><span class="sxs-lookup"><span data-stu-id="fce34-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-128">-ID</span><span class="sxs-lookup"><span data-stu-id="fce34-128">-SiteId</span></span>
<span data-ttu-id="fce34-129">Anger ID för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="fce34-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-130">-Plats namn</span><span class="sxs-lookup"><span data-stu-id="fce34-130">-SiteName</span></span>
<span data-ttu-id="fce34-131">Anger namnet på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="fce34-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-132">-Valv</span><span class="sxs-lookup"><span data-stu-id="fce34-132">-Vault</span></span>
<span data-ttu-id="fce34-133">Anger valv för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="fce34-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fce34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce34-134">CommonParameters</span></span>
<span data-ttu-id="fce34-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce34-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce34-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce34-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fce34-137">INPUTS</span></span>

## <span data-ttu-id="fce34-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fce34-138">OUTPUTS</span></span>

## <span data-ttu-id="fce34-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fce34-139">NOTES</span></span>

## <span data-ttu-id="fce34-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fce34-140">RELATED LINKS</span></span>

[<span data-ttu-id="fce34-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fce34-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="fce34-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fce34-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="fce34-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="fce34-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="fce34-144">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fce34-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


