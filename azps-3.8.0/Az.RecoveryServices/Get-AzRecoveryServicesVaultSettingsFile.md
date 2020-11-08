---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: ac293211c332d8e99a592eedf96bbc179be99912
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092439"
---
# <span data-ttu-id="112cd-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="112cd-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="112cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="112cd-102">SYNOPSIS</span></span>
<span data-ttu-id="112cd-103">Hämtar inställningar för Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="112cd-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="112cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="112cd-104">SYNTAX</span></span>

### <span data-ttu-id="112cd-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="112cd-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="112cd-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="112cd-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112cd-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="112cd-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="112cd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="112cd-108">DESCRIPTION</span></span>
<span data-ttu-id="112cd-109">Cmdleten **Get-AzRecoveryServicesVaultSettingsFile** hämtar inställnings filen för ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="112cd-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="112cd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="112cd-110">EXAMPLES</span></span>

### <span data-ttu-id="112cd-111">Exempel 1: registrera en Windows Server eller DPM-dator för Azure-säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="112cd-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="112cd-112">Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="112cd-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="112cd-113">Det andra kommandot anger $CredsPath variabeln till C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="112cd-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="112cd-114">Det sista kommandot får valv filen för autentiseringsuppgifter för $Vault 01 genom att använda autentiseringsuppgifterna i $CredsPath för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="112cd-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="112cd-115">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="112cd-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="112cd-116">Kommandot hämtar valvets autentiseringsinformation för $Vault 01 siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="112cd-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="112cd-117">Exempel 3: registrera en Windows Server eller DPM-dator för Azure-säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="112cd-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="112cd-118">Kommandot hämtar valv filen för autentiseringsuppgifter för $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="112cd-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="112cd-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="112cd-119">PARAMETERS</span></span>

### <span data-ttu-id="112cd-120">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="112cd-120">-Backup</span></span>
<span data-ttu-id="112cd-121">Anger att valvets autentiseringsinformation är tillämpbar för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="112cd-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112cd-122">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="112cd-122">-Certificate</span></span>
<span data-ttu-id="112cd-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="112cd-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="112cd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112cd-124">-DefaultProfile</span></span>
<span data-ttu-id="112cd-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="112cd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112cd-126">-Path</span><span class="sxs-lookup"><span data-stu-id="112cd-126">-Path</span></span>
<span data-ttu-id="112cd-127">Anger sökvägen till inställnings filen för Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="112cd-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="112cd-128">Du kan ladda ned filen från portalen för Azure Site Recovery Vault och lagra den lokalt.</span><span class="sxs-lookup"><span data-stu-id="112cd-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112cd-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="112cd-129">-SiteFriendlyName</span></span>
<span data-ttu-id="112cd-130">Anger det eget namn för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="112cd-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="112cd-131">Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="112cd-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112cd-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="112cd-132">-SiteIdentifier</span></span>
<span data-ttu-id="112cd-133">Anger webbplats-ID.</span><span class="sxs-lookup"><span data-stu-id="112cd-133">Specifies the site identifier.</span></span>
<span data-ttu-id="112cd-134">Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="112cd-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112cd-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="112cd-135">-SiteRecovery</span></span>
<span data-ttu-id="112cd-136">Anger att valv filen för valvet är tillämplig på Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="112cd-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112cd-137">-Valv</span><span class="sxs-lookup"><span data-stu-id="112cd-137">-Vault</span></span>
<span data-ttu-id="112cd-138">Anger Azure Site Recovery-valv objekt.</span><span class="sxs-lookup"><span data-stu-id="112cd-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="112cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112cd-139">CommonParameters</span></span>
<span data-ttu-id="112cd-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="112cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112cd-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="112cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112cd-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="112cd-142">INPUTS</span></span>

### <span data-ttu-id="112cd-143">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="112cd-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="112cd-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="112cd-144">OUTPUTS</span></span>

### <span data-ttu-id="112cd-145">Microsoft. Azure. commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="112cd-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="112cd-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="112cd-146">NOTES</span></span>

## <span data-ttu-id="112cd-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="112cd-147">RELATED LINKS</span></span>

[<span data-ttu-id="112cd-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="112cd-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="112cd-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="112cd-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="112cd-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="112cd-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)

